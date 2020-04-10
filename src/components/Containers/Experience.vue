<template lang="pug">
include ../../assets/strings/en.pug
div.main-div
    div(v-if="BannerOne").experience-div-one
        div.experience-shape-one
            banner-one(:width="width" :height="height")
        div.experience-text-one
            |{{ experience }}

    div(v-if="BannerTwo").experience-div-two
        div.experience-shape-two
            banner-two(:width="width" :height="height")
        div.experience-text-two
            |{{ experience }}

    div(v-if="BannerThree").experience-div-three
        div.experience-shape-three
            banner-three(:width="width" :height="height")
        div.experience-text-three
            |{{ experience }}


    div(v-if="BannerFour").experience-div-four
        div.experience-shape-four
            banner-four(:width="width" :height="height")
        div.experience-text-four
            |{{ experience }}

    div(v-if="BannerFive").experience-div-five
        div.experience-shape-five
            banner-five(:width="width" :height="height")
        div.experience-text-five
            |{{ experience }}
</template>

<script>
import BannerOne from "../Shapes/BannerOne";
import BannerTwo from "../Shapes/BannerTwo";
import BannerThree from "../Shapes/BannerThree";
import BannerFour from "../Shapes/BannerFour";
import BannerFive from "../Shapes/BannerFive";
export default {
  name: "Experience",
  props: {
    experience: String,
    BannerOne: Boolean,
    BannerTwo: Boolean,
    BannerThree: Boolean,
    BannerFour: Boolean,
    BannerFive: Boolean,
    width: String,
    height: String,
  },
  components: {
    BannerOne,
    BannerTwo,
    BannerThree,
    BannerFour,
    BannerFive,
  },
  data: () => ({}),
  methods: {},
};
</script>

<style lang="sass" scoped>
@import '@/assets/sass/_font', '@/assets/sass/_colors'
@include font('Righteous-Regular', '../../assets/fonts/Righteous-Regular')

*
  font-family: 'Righteous-Regular'
  color: $text
  text-shadow: -1px -1px 0 $stroke, 1px -1px 0 $stroke, -1px 1px 0 $stroke, 1px 1px 0 $stroke


.main-div
  font-family: 'Montserrat-Medium'

.experience-text-one
    position: absolute

.experience-text-two
    position: absolute
 

.experience-text-three
    position: absolute


.experience-text-four
    position: absolute


.experience-text-five
    posiition: absolute

.experience-div-one
    position: relative

.experience-div-two
    position: relative

.experience-div-three
    position: relative

.experience-div-four
    position: relative

.experience-div-five
    position: relative

.main-div
    display: flex
    flex-wrap: wrap
    align-items: center

@media (min-width: 1450px)
    .experience-text-one
        position: absolute
        top: 25em
        left: 30em
        width: 15em
        text-align: justify

    .experience-text-two
        position: absolute
        top: 15em
        right: 26em
        width: 15em
        text-align: justify
 

    .experience-text-three        
        position: absolute
        top: 25em
        left: 20em
        width: 25em
        text-align: justify


    .experience-text-four
        position: absolute
        top: 18em
        left: 30em
        width: 18em
        text-align: justify


    .experience-text-five
        position: absolute
        top: 12em
        right: 15em
        width: 14em
        text-align: justify

    .experience-div-three
        margin-left: 40%

@media (max-width: 1450px)
    .experience-text-one
        position: absolute
        top: 25em
        left: 30em
        width: 15em
        text-align: justify

    .experience-text-two
        position: absolute
        top: 15em
        right: 26em
        width: 15em
        text-align: justify
 

    .experience-text-three        
        position: absolute
        top: 25em
        left: 20em
        width: 25em
        text-align: justify


    .experience-text-four
        position: absolute
        top: 18em
        left: 30em
        width: 18em
        text-align: justify


    .experience-text-five
        position: absolute
        top: 12em
        right: 15em
        width: 14em
        text-align: justify

    .experience-div-three
        margin-left: 40%


</style>
