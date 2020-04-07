<template>
  <svg
    version="1.1"
    id="Capa_1"
    xmlns="http://www.w3.org/2000/svg"
    xmlns:xlink="http://www.w3.org/1999/xlink"
    x="0px"
    y="0px"
    width="511.633px"
    height="511.633px"
    viewBox="0 0 511.633 511.633"
    style="enable-background: new 0 0 511.633 511.633;"
    xml:space="preserve"
  >
    <g fill="#cc7a00">
      <g>
        <path
          d="M11388 4426 c-26 -17 -48 -34 -48 -39 0 -4 23 -57 50 -117 53 -115
56 -125 40 -115 -6 4 -10 -11 -10 -37 0 -30 15 -74 49 -148 28 -58 46 -106 41
-108 -4 -2 -52 8 -106 22 -534 135 -1061 158 -1629 71 -195 -30 -486 -93 -501
-109 -9 -8 -85 -853 -84 -933 0 -7 10 -13 23 -13 20 0 23 -4 19 -29 -2 -16 5
-49 16 -74 33 -74 56 -77 309 -38 498 75 723 94 1093 94 303 0 454 -12 622
-50 40 -9 83 -16 95 -17 18 -1 19 -4 10 -21 -17 -32 -173 -181 -320 -305
l-136 -114 20 -36 c11 -19 26 -43 33 -53 15 -19 12 -20 121 27 33 14 51 20 40
13 -39 -24 -102 -95 -109 -122 -5 -18 -1 -35 10 -52 29 -45 76 -31 449 134
354 157 592 257 826 348 239 93 269 117 269 211 0 31 -4 64 -10 74 -7 13 -6
19 5 24 23 8 19 34 -25 168 -88 268 -219 481 -459 743 -76 83 -249 250 -541
524 l-115 108 -47 -31z"
        />
      </g>
    </g>
    <g @mouseover="hoverText" ref="texts" v-for="(text, index) in texts" :key="text">
      <g
        class="text"
        ref="text"
        stroke="#fffff0"
        stroke-width="0.2"
        :transform="`scale(2.2, 2.2) translate(78, ${
          48 * parseInt(index) + 90
        })`"
      >
        <text>{{ text }}</text>
      </g>
    </g>
  </svg>
</template>
<script>
export default {
  name: "ArrowRight",
  props: { texts: Array },
  methods: {
    hoverText: function() {
      const textsRef = this.$refs["texts"];
      this.$anime({
        targets: textsRef,
        rotate: [-15, 25, 0],
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
