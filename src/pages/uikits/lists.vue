<template>
  <div>
    <Breadcrumbs main="UI Kits" title="lists" />

    <div class="container-fluid">
      <div class="row">
        <Defaultlist />
        <Linksandbuttons />
        <FlushStyle />
        <Contextualclasses />
        <Withbadges />
        <Customcontent />
        <JavaScriptbehavior />
        <images />

      </div>
    </div>

  </div>
</template>

<script>
import Defaultlist from "./lists/Defaultlist.vue"
import Linksandbuttons from "./lists/Linksandbuttons.vue"
import FlushStyle from "./lists/FlushStyle.vue"
import Contextualclasses from "./lists/Contextualclasses.vue"
import Withbadges from "./lists/Withbadges.vue"
import Customcontent from "./lists/Customcontent.vue"
import JavaScriptbehavior from "./lists/JavaScriptbehavior.vue"
import images from "./lists/images.vue"
export default {
  components: {
    Defaultlist,
    Linksandbuttons,
    FlushStyle,
    Contextualclasses,
    Withbadges,
    Customcontent,
    JavaScriptbehavior,
    images
  }

};
</script>