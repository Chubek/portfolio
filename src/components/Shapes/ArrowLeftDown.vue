<template>
  <div>
    <svg
      id="Layer_1"
      data-name="Layer 1"
      xmlns="http://www.w3.org/2000/svg"
      width="400"
      height="400"
      viewBox="0 0 512 512"
    >
      <title>arrow-right-down-glyph</title>
      <g fill="#cc7a00" transform="rotate(-45)">
        <path
          d="M7215 4882 c-157 -402 -377 -914 -540 -1256 -36 -77 -64 -145 -61
-151 2 -7 25 -24 51 -40 39 -22 49 -25 59 -14 7 8 54 62 105 122 92 106 125
137 78 75 -35 -47 -89 -176 -95 -226 -3 -32 0 -47 13 -62 43 -48 85 -21 241
151 129 142 225 232 264 244 11 3 20 11 20 18 0 7 3 8 10 1 13 -13 37 -160 51
-315 16 -188 6 -650 -20 -899 -24 -221 -61 -490 -97 -693 -13 -76 -24 -142
-24 -148 0 -8 29 -9 96 -4 93 7 95 6 83 -12 -17 -27 -3 -90 25 -118 14 -14 41
-26 67 -30 50 -7 664 40 721 56 44 11 93 50 114 90 19 37 57 208 84 370 85
528 77 1002 -25 1504 -19 93 -35 185 -35 205 0 99 68 106 240 26 64 -30 135
-59 159 -65 110 -24 139 54 57 154 -19 23 -33 45 -29 48 6 7 -464 504 -597
630 -257 245 -502 400 -766 486 -66 21 -131 41 -146 45 -26 6 -27 4 -103 -192z"
        />
      </g>
      <text
        @mouseover="hoverText"
        transform="scale(3, 3) translate(55, 65)"
        class="text"
        ref="text"
        fill="#000"
        stroke="#fff"
        stroke-width="0.2"
      >{{ text }}</text>
    </svg>
  </div>
</template>
<script>
export default {
  name: "ArrowLeftDown",
  props: {
    text: String
  },
  methods: {
    hoverText: function() {
      const textsRef = this.$refs["text"];
      this.$anime({
        targets: textsRef,
        rotate: [15, -25, 0],
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
