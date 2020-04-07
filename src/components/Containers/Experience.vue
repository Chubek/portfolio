<template lang="pug">
include ../../assets/strings/en.pug
div.main-div
    div(v-if="BannerOne").experience-div-one
      div.experience-shape-one
        banner-one(:size="size")
      div.experience-text-one
        | {{ experience }}

    div(v-if="BannerTwo").experience-div-two
      div.experience-shape-two
        banner-two(:size="size")
      div.experience-text-two
        | {{ experience }}

    div(v-if="BannerThree").experience-div-three
      div.experience-shape-three
        banner-three(:size="size")
      div.experience-text-three
        | {{ experience }}


    div(v-if="BannerFour").experience-div-four
      div.experience-shape-four
        banner-four(:size="size")
      div.experience-text-four
        | {{ experience }}

    div(v-if="BannerFive").experience-div-five
      div.experience-shape-five
        banner-five(:size="size")
      div.experience-text-five
        |{{ experience }}





    
</template>

<script>
import BannerOne from "../Shapes/BannerOne";
import BannerTwo from "../Shapes/BannerTwo";
import BannerThree from "../Shapes/BannerThree";
import BannerFour from "../Shapes/BannerFour";
import BannerFive from "../Shapes/BannerFive";
import PathOne from "../Paths/PathOne";
import PathTwo from "../Paths/PathTwo";
import PathThree from "../Paths/PathThree";
import PathFour from "../Paths/PathFour";
import PathFive from "../Paths/PathFive";
export default {
  name: "Experience",
  props: {
    experience: String,
    BannerOne: Boolean,
    BannerTwo: Boolean,
    BannerThree: Boolean,
    BannerFour: Boolean,
    BannerFive: Boolean,
    size: Object
  },
  components: {
    BannerOne,
    BannerTwo,
    PathOne,
    PathTwo,
    BannerThree,
    PathThree,
    BannerFour,
    PathFour,
    BannerFive,
    PathFive
  },
  data: () => ({
    circleToggle: true,
    squareToggle: true,
    triangleToggle: true,
    trapezoidToggle: true
  }),
  methods: {}
};
</script>

<style lang="sass" scoped>
@import '@/assets/sass/_font', '@/assets/sass/_colors'
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
