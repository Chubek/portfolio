<template>
  <div>
    <svg
      id="Layer_1"
      data-name="Layer 1"
      xmlns="http://www.w3.org/2000/svg"
      width="600"
      height="600"
      viewBox="0 0 512 512"
    >
      <title>arrow-right-down-glyph</title>
     
        <g transform="translate(0, -20) scale(0.5, 0.5)" fill="#991f00">
          <polygon
            points="18,531.7234 197.2429,531.7234 98.8884,489.671 98.8884,387.0824 18,387.0824 75.0308,456.1445 	"
          />
          <polygon
            points="102.9077,487.3423 201.2622,529.3947 201.2622,518.1799 201.2622,487.3423 129.1364,487.3423 	"
          />
          <polygon
            points="846,531.7234 666.7571,531.7234 765.1116,489.671 765.1116,387.0824 846,387.0824 788.9692,456.1445 	"
          />
          <polygon
            points="761.0923,487.3423 662.7378,529.3947 662.7378,518.1799 662.7378,487.3423 734.8636,487.3423 	"
          />
          <rect x="116.7475" y="346.116" width="630.5049" height="123.2793" />
          <path
            d="M102.9077,332.2766v11.8306v126.3635v12.7646h658.1846v-12.7646V344.1072v-11.8306H102.9077z M752.2524,474.3953H111.7475
		V341.116h640.5049V474.3953z"
          />
        </g>
    
      <text
        @mouseover="hoverText"
        transform="scale(3, 3) translate(50, 65)"
        class="text"
        ref="text"
        fill="#000"
        stroke="#fff"
        stroke-width="0.2"
      >
        {{ text }}
      </text>
    </svg>
  </div>
</template>
<script>
export default {
  name: "ArrowLeftDown",
  props: {
    text: String,
  },
  methods: {
    hoverText: function() {
      const textsRef = this.$refs["text"];
      this.$anime({
        targets: textsRef,
        rotate: [15, -25, 0],
        ease: "easeInOutBounce",
      });
    },
  },
};
</script>
<style lang="sass" scoped>
@import '@/assets/sass/_font'
@include font('IndieFlower', '../../assets/fonts/IndieFlower')

.text
    font-family: 'IndieFlower'
</style>
