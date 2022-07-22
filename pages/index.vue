<!-- Crafted by Jvl3s Perez -->


<template>
  <div class ="container">
<div class ="leftSide">
<Sidebar/>
</div>

<div class ="rightSide grid grid-cols-8">
  <div class="panelContainer 
   xl:col-start-4 xl:col-span-7
   lg:col-start-4 lg:col-span-7
   md:col-start-4 md:col-span-7
   sm:col-start-2 sm:col-span-7
   col-start-1
    col-span-7
   ">

    <Panel/>
  </div>


</div>
  </div>
</template>

<script>


export default {
  components: {  },
  name: 'IndexPage',
  data () {
    return {

    }
  },
}


</script>


<style scoped>
.leftSide{
float:left;
}


</style>
