<template lang="pug">
q-layout
  q-page-container
    Home


</template>

<script>
import Home from "./components/Home.vue";

export default {
  name: "LayoutDefault",
  components: {
    Home
  },
  data: () => ({
    leftDrawerOpen: false
  })
};
</script>

<style lang="sass">
html, body
  background: radial-gradient(#660000, #000)
  max-width: 100%
  overflow-x: hidden




</style>
