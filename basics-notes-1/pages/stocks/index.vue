<template>
  <div>
    <h1>Stocks</h1>
    <input type="text" v-model="ticker" />
    <button @click="onLoadTicker">Load Ticker</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      ticker: "",
    };
  },
  methods: {
    onLoadTicker() {
      this.$router.push("/stocks/" + this.ticker);
    },
  },
  layout: "tickers",
};
</script>
