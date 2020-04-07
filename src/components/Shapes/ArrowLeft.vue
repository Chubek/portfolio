<template>
  <svg
    version="1.1"
    id="Capa_1"
    xmlns="http://www.w3.org/2000/svg"
    xmlns:xlink="http://www.w3.org/1999/xlink"
    x="0px"
    y="0px"
    width="465px"
    height="459px"
    viewBox="0 0 459 459"
    style="enable-background:new 0 0 465 459;"
    xml:space="preserve"
  >
    <g fill="#e65c00">
      <g id="reply">
        <path
          d="M178.5,140.25v-102L0,216.75l178.5,178.5V290.7c127.5,0,216.75,40.8,280.5,130.05C433.5,293.25,357,165.75,178.5,140.25z"
        />
      </g>
    </g>
    <g @mouseover="hoverText" ref="texts" v-for="(text, index) in texts" :key="text">
      <g
        class="text"
        ref="text"
        fill="#000"
        stroke="#fff"
        stroke-width="0.2"
        :transform="`scale(1.8, 1.8) translate(11, ${18 * parseInt(index) + 105})`"
      >
        <text>{{ text }}</text>
      </g>
    </g>
  </svg>
</template>
<script>
export default {
  name: "ArrowLeft",
  props: {
    texts: Array
  },
  methods: {
    hoverText: function() {
      const textsRef = this.$refs["texts"];
      this.$anime({
        targets: textsRef,
        rotate: [-25, 15, 0],
        ease: "easeInOutBounce"
      });
    }
  }
};
</script>
<style lang="sass" scoped>
@import '@/assets/sass/_font'
@include font('IndieFlower', '../../assets/fonts/IndieFlower')

.text
  font-family: 'IndieFlower'

</style>
