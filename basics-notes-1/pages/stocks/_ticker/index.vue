<template>
  <div>
    <h1>{{ $route.params.ticker }}</h1>
    <ul v-for="mountain in mountains" :key="mountain.slug">
      <li>{{ mountain.title }}</li>
    </ul>
  </div>
</template>

<script>
export default {
  async asyncData({ $axios, $config }) {
    const mountains = await $axios.$get(`https://api.nuxtjs.dev/mountains`);
    return { mountains };
  },
};
</script>
