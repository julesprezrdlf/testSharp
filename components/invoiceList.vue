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
   <p>hola</p>
    {{output}}

  </div>
</template>

<script>
import invoices from "../assets/invoices.json";
export default {
  data() {
    return {
      jsonData: invoices,
      output:{}
    };
  },
  methods: {

    getJson: function () {
      fetch("https://julesprezrdlf.github.io/testSharp/invoices.json")
    //   fetch("../static/invoices") MANTENER COMENTADO
        .then((response) => response.json())
        .then((data) => {
            console.log("esto es data")
          console.log(data);
        })
        // .then(this.setResults) MANTENER COMENTADO
        ;
        
      
    },
    // ,                           MANTENER COMENTADO
    // setResults(results){        MANTENER COMENTADO
    //     this.output=results;    MANTENER COMENTADO
    // }                           MANTENER COMENTADO
    prueba(){
    console.log("holaaaa");
    },
fetchJson: function () {
      
          fetch("https://julesprezrdlf.github.io/testSharp/invoices.json")
          .then(res=>{
            return res.json();
          }).then(this.setResults);
      
    },
    setResults(results){
      this.output = results;
    },

  },

    

//   fetchJson: function () {
      
//           fetch("https://julesprezrdlf.github.io/testSharp/invoices.json")
//           .then(res=>{
//             return res.json();
//           }).then(this.setResults);
      
//     },
//     setResults(results){
//       this.output = results;
//     },

  beforeMount() {
    this.getJson();
    this.prueba();
    this.fetchJson();
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
