<template lang="pug">
include ../assets/strings/en.pug

div.main-div
  div.header
    div.logo-div
      svg(ref="heart" width="300" height="230").heart
          polygon(ref="heart-polygon" style="stroke-linejoin:miter; stroke:white; stroke-width:5; fill: red;"
          points="100 100, 150 150, 200 100, 200 75, 185 60, 165 60, 150 75, 135 60, 115 60, 100 75, 100 100")/
      svg(ref="logo" width="250" height="30").logo
        path(d="M 20,20 C 80,60 100,40 120,20" fill="transparent" ref="logo-path").logo-path
        text(ref="logo-text" x=0 y=15 fill="#b38600").logo-text=STR_SITE_TITLE
    div.arabesque-div
      arabesque

    div.blurbs-intro
      intro(intro=STR_SITE_DESC)




</template>

<script>
import Experience from "./Containers/Experience";
import Arabesque from "./Shapes/Arabesque";
import Intro from "./Containers/Intro"
export default {
  name: "Home",
  components: {
    Experience,
    Arabesque,
    Intro
  },
  data: () => ({}),
  methods: {
    beatHeart: function () {
      console.log(this.$refs);
      const targets = this.$refs["heart"];
      const logoPath = this.$anime.path(this.$refs["logo-path"]);
      this.$anime
        .timeline({ loop: true, direction: "alternate" })
        .add({
          targets: targets,
          translateX: 50,
          translateY: 40,
          scale: this.$anime.random(72, 180) / 100,
          delay: this.$anime.stagger(100),
        })
        .add({
          targets: this.$refs["heart-polygon"],
          "stroke-width": [0, 10],
          delay: this.$anime.stagger(100),
        })
        .add({
          targets: this.$refs["logo"],
          skew: [0, 180],
          rotate: logoPath("angle"),
          translateX: logoPath("x"),
          translateY: logoPath("y"),
          easing: "linear",
          duration: 2000,
        })
        .add({
          targets: this.$refs["logo-text"],
          opacity: [100, 0]
          
        });
    },
  },
  mounted: function () {
    this.beatHeart();
  },
};
</script>

<style lang="sass" scoped>
@import '@/assets/sass/_font'
@include font('Aftaserif', '../assets/fonts/Aftaserif')


.logo-text
  text-anchor: right
  font-family: Aftaserif
  font-size: 16px
  letter-spacing: 2px

@media (min-width: 1450px)
  .logo
    position: relative
    top: 2%
    left: -9%
  .arabesque-div
    position: absolute
    top: -5%
    right: -2%
</style>
