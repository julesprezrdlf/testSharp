<template>


  <div>

    <h1> iteration </h1>

<div v-for="item in jsonData" :key="item.id">

<p>{{item.date}}</p>
<div class="paid" v-if="item.paid">
<h1>PAID</h1></div>

<div class="unpaid" v-if="item.paid===false">
<h1>UNPAID</h1></div>

<hr/>
</div>




    {{jsonData}}

  </div>
</template>

<script>
import invoices from '../assets/invoices.json';
export default {
 data () {
    return {
      jsonData: invoices
    }
  },
  methods:{
    getJson: function(){
        // fetch("https://api.themoviedb.org/3/movie/550?api_key=9d5bbddde93fb73ec32279ed6f8795c3") 
        fetch("../static/invoices")
        .then(response=>response.json())
        .then(data=>{
            console.log(data)
        })
        alert("hola");
    }
  },
  beforeMount(){
   this.getJson();
  }
}
</script>

<style>
.unpaid{
    background-color: #F4541D;
    color: #fff;
    radius: 5px;
    padding: 2px, 6px, 2px, 6px;
    width: 59px;
    height: 20px;
}

.paid{
    background-color: #4CAF50;
    color: #fff;
    radius: 5px;
    padding: 2px, 6px, 2px, 6px;
    width: 59px;
    height: 20px;
}

hr{
    color: #E4E4E4;
    max-width: 600px;
}
</style>