<template lang="pug">
include ../../assets/strings/en.pug
div.main-div
    div(v-if="BannerOne").experience-div-one
      div.experience-shape-one
        banner-one
      div.experience-text-one
        |{{experience}}

    div(v-if="BannerTwo").experience-div-two
      div.experience-shape-two
        banner-two
      div.experience-text-two
        |{{exxperience}}


    
</template>

<script>
import BannerOne from "../Shapes/BannerOne";
import BannerTwo from "../Shapes/BannerTwo";
export default {
  name: "Experience",
  props: {
    experience: String,
    BannerOne: Boolean,
    exxperience: String,
    BannerTwo: Boolean
  },
  components: {
    BannerOne,
    BannerTwo
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
  }
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
    left: 28em
    width: 180px
    transform: rotate(0deg)
    overflow-wrap: break-word
  
  .experience-shape-one
    transform: rotate(-10deg)

  .experience-div-two
    position: relative

  .experience-text-two
    position: absolute
    top: 33%
    width: 300px
    left: 16em

</style>
