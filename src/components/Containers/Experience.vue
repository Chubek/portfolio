<template lang="pug">
include ../../assets/strings/en.pug
div.main-div
    div(v-if="BannerOne").experience-div-one
      div.experience-shape-one
        banner-one
      div.experience-text-one
        |{{experience}}


    
</template>

<script>
import BannerOne from "../Shapes/BannerOne"
export default {
  name: "Experience",
  props: {
    experience: String,
    BannerOne: Boolean
  },
  components: {
    BannerOne
  },
  data: () => ({
    circleToggle: true,
    squareToggle: true,
    triangleToggle: true,
    trapezoidToggle: true
  }),
  methods: {
    rollCircle: function() {
      console.log(this.$refs);
      const targets = this.$el;      
      console.log(targets);
      this.$anime({
        targets: targets,
        translateX: 270,
        scale: this.$anime.random(72, 180) / 100,
        delay: this.$anime.stagger(100),
        loop: true

      });
    }
  },
  
};
</script>

<style lang="sass" scoped>
@import '@/assets/sass/_font' 
@include font('Montserrat-Medium', '../../assets/fonts/Montserrat-Medium')

.main-div
  font-family: 'Montserrat-Medium'

@media (min-width: 1450px)
  .experience-text-one
    position: absolute
    top: 32%
    left: 29em
    width: 180px
    transform: rotate(10deg)
    overflow-wrap: break-word

</style>
