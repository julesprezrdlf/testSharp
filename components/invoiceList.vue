<template>
  <div class="containerInvoice mt-5">
    <div class="invoices text-xs font-semibold my-5">INVOICES</div>
    <hr />
    <div v-for="item in output" :key="item.id">
      <div class="billContainer mt-2 flex flex-row">
        <p>{{ item.date }}</p>
        <div
          class="paid text-center text-xs font-semibold rounded-md align-middle"
          v-if="item.paid"
        >
          <h1>PAID</h1>
        </div>

        <div
          class="unpaid text-center text-xs font-semibold rounded-md align-middle"
          v-if="item.paid === false"
        >
          <h1>UNPAID</h1>
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
  max-width: 600px;
}
</style>
