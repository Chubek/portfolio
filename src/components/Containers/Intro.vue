<template>
  <div>
    <div class="blob-svg">
      <svg width="1000" height="1000" viewBox="0 0 600 600" xmlns="http://www.w3.org/2000/svg">
        <g transform="translate(300,300)">
          <path
            d="M110.6,-78C137.4,-17.3,149.2,37.8,128.3,78.2C107.4,118.7,53.7,144.3,-1.2,145C-56,145.7,-112,121.3,-149.5,71.3C-187.1,21.3,-206.1,-54.3,-178.1,-115.7C-150.1,-177,-75.1,-224,-16.6,-214.4C41.9,-204.8,83.7,-138.7,110.6,-78Z"
            fill="#ff8000"
          />
        </g>
      </svg>

      <div class="intro-blurb">{{ intro }}</div>
    </div>
  </div>
</template>
<script>
export default {
  name: "Intro",
  props: {
    intro: String
  }
};
</script>
<style lang="sass" scoped>
@import '@/assets/sass/_font'
@include font('Righteous-Regular', '../../assets/fonts/Righteous-Regular')

.intro-blurb
  font-family: 'Righteous-Regular'
  color: #fff
  text-shadow: -1px -1px 0 #000, 1px -1px 0 #000, -1px 1px 0 #000, 1px 1px 0 #000

@media (min-width: 1450px)
  .blog-svg
    position: relative
    shape-outside: circle(50%)
  .intro-blurb
    position: absolute
    top: 68em
    left: 22em
    width: 20em
    text-align: left    
    text-align: justify
    padding: 2px
    

</style>
