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
          d="M4970 5056 l-385 -31 -27 -104 c-76 -295 -118 -613 -125 -959 -9
-437 29 -754 136 -1146 l29 -108 -31 6 c-18 4 -141 59 -274 122 -133 64 -245
114 -250 111 -5 -3 -23 -25 -40 -50 l-32 -44 41 -39 c22 -21 85 -88 141 -149
55 -60 172 -185 258 -276 87 -92 155 -170 151 -174 -4 -3 0 -5 8 -3 8 1 14 -2
13 -9 -3 -13 220 -227 342 -328 229 -190 585 -369 698 -351 82 13 97 35 198
287 104 262 235 571 366 864 156 347 167 405 76 405 -39 0 -97 -50 -213 -183
-36 -42 -66 -74 -68 -72 -3 3 79 192 157 359 28 59 51 112 51 116 0 8 -100 74
-104 68 -1 -2 -65 -77 -143 -168 -139 -163 -248 -275 -310 -318 -29 -20 -32
-21 -31 -5 0 10 -8 81 -18 158 -14 109 -18 202 -18 425 1 361 21 593 95 1083
27 178 30 214 20 248 -17 55 -59 81 -129 77 -61 -4 -60 -8 -37 122 8 47 15 88
15 93 0 13 -166 5 -560 -27z"
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
