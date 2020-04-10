<template>
  <div>
    <div class="blob-svg">
      <svg
        width="width"
        height="height"
        viewBox="0 0 600 600"
        xmlns="http://www.w3.org/2000/svg"
      >
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
    intro: String,
    width: String,
    height: String
  },
};
</script>
<style lang="sass" scoped>
@import '@/assets/sass/_font', '@/assets/sass/_colors'
@include font('Righteous-Regular', '../../assets/fonts/Righteous-Regular')

.intro-blurb
  font-family: 'Righteous-Regular'
  color: $text
  text-shadow: -1px -1px 0 $stroke, 1px -1px 0 $stroke, -1px 1px 0 $stroke, 1px 1px 0 $stroke

@media (min-width: 1450px)
  .blog-svg
    position: relative
    shape-outside: circle(50%)
  .intro-blurb
    position: absolute
    top: 98em
    left: 50em
    width: 20em
    text-align: left
    text-align: justify
    padding: 2px
    font-size: 60
    transform: scale(2)

@media (max-width: 1450px)
  .intro-blurb
    position: absolute
    top: 105em
    left: 35em
    width: 20em
    text-align: left
    text-align: justify
    padding: 2px
    font-size: 60
    transform: scale(1.4)

@media (max-width: 968px)
  .intro-blurb
    position: absolute
    top: 93em
    left: 22em
    width: 20em
    text-align: left
    text-align: justify
    padding: 2px
    font-size: 60
    transform: scale(1.0)

@media (max-width: 768px)
  .intro-blurb
    position: absolute
    top: 85em
    left: 15em
    width: 20em
    text-align: left
    text-align: justify
    padding: 2px
    font-size: 60
    transform: scale(0.8)
  .blog-svg
    position: relative
    shape-outside: circle(50%)
    width: 200px
    height: 200px




</style>
