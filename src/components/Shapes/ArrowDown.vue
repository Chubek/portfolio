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
      <path
        fill="#cc7a00"
        d="M487.31,275.08a11.1,11.1,0,0,0-9.61-5.55H421.54V11.1A11.1,11.1,0,0,0,410.44,0H120a11.11,11.11,0,0,0-9,4.64L25.27,124.51a11.1,11.1,0,0,0,9,17.55H279.47V269.53H223.3a11.1,11.1,0,0,0-9.61,16.65L340.9,506.45a11.1,11.1,0,0,0,19.22,0L487.3,286.18A11.09,11.09,0,0,0,487.31,275.08Z"
      />
      <text @mouseover="hoverText" transform="scale(3, 3) translate(55, 65)" class="text" ref="text" fill="#000" stroke="#fff" stroke-width="0.2">{{ text }}</text>
    </svg>
  </div>
</template>
<script>
export default {
  name: "ArrowDown",
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
