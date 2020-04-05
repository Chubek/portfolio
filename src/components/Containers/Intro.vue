<template>
  <div>
    <div class="blob-svg">
      <svg
        width="1100"
        height="1100"
        viewBox="0 0 620 620"
        xmlns="http://www.w3.org/2000/svg"
      >
        <g transform="translate(300,300)">
          <path
            d="M96.2,-77.9C122,-44.3,138.5,-4.5,132.2,33C125.9,70.4,96.8,105.5,53.7,135.3C10.7,165.2,-46.3,189.8,-77.1,170.8C-107.8,151.9,-112.4,89.3,-131.8,24.3C-151.2,-40.6,-185.5,-107.9,-166,-140C-146.5,-172.1,-73.2,-169.1,-19,-153.9C35.2,-138.7,70.4,-111.4,96.2,-77.9Z"
            fill="#e65c00"
          />
        </g>
      </svg>

      <div class="intro-blurb">
        {{ intro }}
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: "Intro",
  props: {
    intro: String,
  },
};
</script>
<style lang="sass" scoped>
@import '@/assets/sass/_font'
@include font('Montserrat-Medium', '../../assets/fonts/Montserrat-Medium')

.intro-blurb
    font-family: 'Montserrat-Medium'

@media (min-width: 1450px)
    .blog-svg
        position: relative
        shape-outside: circle(50%)
    .intro-blurb
        position: absolute
        top: 30%
        left: 17%
        width: 20em
        transform: rotate(-20deg)
        text-align: left
</style>
