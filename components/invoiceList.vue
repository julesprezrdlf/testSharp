<template>
  <div class="containerInvoice mt-5">
    <div class="invoices text-xs font-semibold my-5">INVOICES</div>
    <hr />
    <div v-for="item in output" :key="item.id">
      <div class="billContainer mt-3 flex flex-row grid grid-cols-2">
        <div class="leftInvoice  flex flex-row">
          <p class="text-xs sm:text-lg">{{ item.date }}</p>
          <div
            class="paid text-center text-xs font-semibold rounded-md align-middle ml-4 mt-1"
            v-if="item.paid"
          >
            <h1>PAID</h1>
          </div>

          <div
            class="unpaid text-center text-xs font-semibold rounded-md align-middle ml-5 mt-1"
            v-if="item.paid === false"
          >
            <h1>UNPAID</h1>
          </div>
        </div>

        <div class="rightInvoice flex flex-row ml-0 sm:ml-12">
          <div>
            <p class="text-base sm:text-lg">${{ item.total }}</p>
          </div>
          <div class="-ml-5 sm:ml-0"><DownloadIcon/></div>
          
        </div>
      </div>

      <p class="mb-2 font-normal text-xs">Invoice #{{ item.number }}</p>

      <hr />
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      output: {},
    };
  },
  methods: {
    fetchJson: function () {
      fetch("https://julesprezrdlf.github.io/testSharp/invoices.json")
        .then((res) => {
          return res.json();
        })
        .then(this.setResults);
    },
    setResults(results) {
      this.output = results;
    },
  },

  beforeMount() {
    this.fetchJson();
  },
};
</script>

<style>
.unpaid {
  background-color: #f4541d;
  color: #fff;
  padding: 2.5px;

  width: 59px;
  height: 20px;
}

.paid {
  background-color: #4caf50;
  color: #fff;

  padding: 2.5px;
  width: 59px;
  height: 20px;
}

hr {
  color: #e4e4e4;
  /* color: black; */
  max-width: 600px;
}

.containerInvoice {
  max-width: 600px;
}

.rightInvoice {
  /* margin-left: 80px; */
}

  
</style>
