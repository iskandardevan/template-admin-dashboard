<template>
<Breadcrumbs title="Default Style" main="Apps" title1="Default Style" />
<div class="container-fluid">
    <div class="row">
        <div class="col-sm-12">
            <Default />
            <Default2 />
            <Default3 />
        </div>
    </div>
</div>
</template>

<script>
import Default from "./DefaultPage.vue"
import Default2 from "./Default2Page.vue"
import Default3 from "./Default3Page.vue"
export default {
    components: {
        Default,
        Default2,
        Default3
    }
}
</script>
