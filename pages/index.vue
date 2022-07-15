<template>
  <div class ="container">
<div class ="leftSide">
<!-- <Sidebar/> -->
</div>
<div class ="rightSide">
<Panel/>
<!-- {{jsonData}} -->
</div>
  </div>
</template>

<script>

import Panel from "../components/panel.vue";
import Sidebar from "~/components/sidebar.vue";

export default {
  components: { Panel, Sidebar },
  name: 'IndexPage',
  data () {
    return {
      // jsonData: invoices
    }
  },
}


</script>


<style scoped>
.leftSide{
float:left;
}


</style>
