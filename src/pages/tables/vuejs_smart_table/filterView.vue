<template>
  <div class="col-md-12">
    <div class="card">
      <div class="card-header">
        <h5 class="card-title"> Filter</h5>
      </div>
      <div class="card-body">
        <div class="table-responsive">
          <div id="basic-1_wrapper" class="dataTables_wrapper no-footer">

            <div class="row filter-smart">
              <div class="col-sm-2">
                <input class="form-control" v-model="filters.name.value" placeholder="Name" />
              </div>
              <div class="col-sm-2">
                <input class="form-control" v-model="filters.position.value" placeholder="Position" />
              </div>
              <div class="col-sm-2">
                <input class="form-control" v-model="filters.office.value" placeholder="Office" />
              </div>
              <div class="col-sm-2">
                <input class="form-control" v-model="filters.age.value" placeholder="Age" />
              </div>
              <div class="col-sm-2">
                <input class="form-control" v-model="filters.startdate.value" placeholder="Start Date" />
              </div>
              <div class="col-sm-2">
                <input class="form-control" v-model="filters.salary.value" placeholder="Salary" />
              </div>
            </div>

            <div class="dataTables_length" id="basic-1_length">
              <table class="display dataTable" id="basic-1">
                <thead>
                  <tr>
                    <th>Name</th>
                    <th>Position</th>
                    <th>Office</th>
                    <th>Age</th>
                    <th>Start date</th>
                    <th>Salary</th>
                  </tr>
                </thead>
                <tbody>
                  <tr v-for="row in get_rows()" :key="row" :filters="filters">
                    <td>{{ row.name }}</td>
                    <td>{{ row.position }}</td>
                    <td>{{ row.office }}</td>
                    <td>{{ row.age }}</td>
                    <td>{{ row.startdate }}</td>
                    <td>{{ row.salary }}</td>
                  </tr>
                </tbody>
              </table>
              <ul class="pagination">
                <li class="page-item">
                  <a class="page-link" href="#" aria-label="Previous">
                    <span aria-hidden="true">&laquo;</span>
                  </a>
                </li>
                <li class="page-item" v-for="i in num_pages()" :key="i" v-bind:class="[i == currentPage ? 'active' : '']"
                  v-on:click="change_page(i)"><a class="page-link">{{i}}</a></li>
                <li class="page-item">
                  <a class="page-link" href="#" aria-label="Next">
                    <span aria-hidden="true">&raquo;</span>
                  </a>
                </li>
              </ul>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
import { mapState } from "vuex";
export default {
  data() {
    return {
       elementsPerPage: 10,
         currentPage: 1,
          ascending: false,
          sortColumn: '',
           perPage: 10,
          pageOptions: [ 10, 25,50,100],
         filters: {
          name: { value: '', keys: ['name'] },
          position: { value: '', keys: ['position'] },
          office: { value: '', keys: ['office'] },
          age: { value: '', keys: ['age'] },
          startdate: { value: '', keys: ['startdate'] },
          salary: { value: '', keys: ['salary'] },
        },
    };
  },
   computed: {
    ...mapState({
      tableItems:(state)=>state.table.items,    
    }),
   columns() {
      if (this.tableItems.length == 0) {
        return [];
      }
      return Object.keys(this.tableItems[0])
    }
   },
  methods:{
      num_pages() {
      return Math.ceil(this.tableItems.length / this.elementsPerPage);
    },
     change_page(page) {
      this.currentPage = page;
    },
     get_rows() {
      var start = (this.currentPage-1) * this.elementsPerPage;
      var end = start + this.elementsPerPage;
      return this.tableItems.slice(start, end);
    },
    onFiltered(filteredItems) {

        this.tableItems = filteredItems.length;
        this.currentPage = 1;
      }
  }
};
</script>