<template>
  <div class="containerInvoice mt-5">
    <div class="invoices text-xs font-semibold my-5">INVOICES</div>
    <hr />
    <div v-for="item in jsonData" :key="item.id">
      <div class="billContainer mt-2 flex flex-row">
             <p>{{ item.date }}</p>
                 <div class="paid text-center text-xs font-semibold rounded-md align-middle" v-if="item.paid">
                  <h1>PAID</h1>
                 </div>

                  <div class="unpaid text-center text-xs font-semibold rounded-md align-middle" v-if="item.paid === false">
                   <h1>UNPAID</h1>
                  </div>
        
             </div>
         <p class="mb-2 font-normal text-xs">Invoice #{{item.number}}</p>
      <hr />
    </div>

    {{ jsonData }}
  </div>
</template>

<script>
import invoices from "../assets/invoices.json";
export default {
  data() {
    return {
      jsonData: invoices,
    };
  },
  methods: {
    getJson: function () {
      // fetch("https://api.themoviedb.org/3/movie/550?api_key=9d5bbddde93fb73ec32279ed6f8795c3")
      fetch("../static/invoices")
        .then((response) => response.json())
        .then((data) => {
          console.log(data);
        });
      alert("hola");
    },
  },
  beforeMount() {
    this.getJson();
  },
};
</script>

<style>
.unpaid {
  background-color: #f4541d;
  color: #fff;
  
  padding: 2px, 6px, 2px, 6px;
  width: 59px;
  height: 20px;
}

.paid {
  background-color: #4caf50;
  color: #fff;

  padding: 2px, 6px, 2px, 6px;
  width: 59px;
  height: 20px;
}

hr {
  color: #e4e4e4;
  max-width: 600px;
}
</style>
