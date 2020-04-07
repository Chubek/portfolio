<template lang="pug">
include ../assets/strings/en.pug

div.main-div
  div.header
    gear

  div(v-if="isIe").isIe
    |"Stop using Internet Explorer goddamit! At least use Edge!"
  div.nail-one
    img(src="../assets/img/nail-post.png" width="20" height="20").nail-one-img
  div.nail-two
    img(src="../assets/img/nail-post.png" width="20" height="20").nail-two-img
  
  div.arabesque-div
    arabesque

  div.intro-arrow(id="#intro")
    arrow-left(:texts=[STR_SITE_SUBTITLE_WMD, STR_SITE_SUBTITLE_AI, STR_SITE_SUBTITLE_GD, STR_SITE_SUBTITLE_BOT])

  div.blurbs-intro
    intro(intro=STR_SITE_DESC)

  div.experience-arrow(id="#experience")
    arrow-right(:texts="STR_EXP")

  div.experience-div-one
    experience(experience=STR_EXP_TETRIS :size="{width: 512, height: 512}" BannerOne)

  div.experience-div-two 
    experience(experience=STR_EXP_WORDPRESS :size="{width: 512, height: 512}" BannerTwo)
  
  div.experience-div-three 
    experience(experience=STR_BEDLAM :size="{width: 512, height: 512}" BannerThree)

  div.experience-div-four 
    experience(experience=STR_EXP_EKELAAS :size="{width: 512, height: 512}" BannerFour)

  div.experience-div-four
    experience(experience=STR_EXP_MOODIMEDIA :size="{width: 512, height: 512}" BannerFive)

  div.skills-arrow(id="#skills")
   arrow-down(text=STR_SKILL)

  div.skills-div
    skills(:size="{width: 512, height: 512}" :imageSize="{width: 250, height: 250}")

  div.skills-desc-one
    skills-description(skillDescOne :size="{width: 400, height: 200}" skillDescription=STR_SKILL_AI)

  div.skills-desc-two
    skills-description(skillDescTwo :size="{width: 400, height: 200}" skillDescription=STR_SKILL_APP)

  div.skills-desc-three
    skills-description(skillDescThree :size="{width: 400, height: 200}" skillDescription=STR_SKILL_GAME_DEV)

  div.skills-desc-four
    skills-description(skillDescFour :size="{width: 400, height: 200}" skillDescription=STR_SKILL_BOT)

  div(id="#contact").arrow-contact
    arrow-left-down(text=STR_CONTACT)

  div.contact-div
    q-card(style="background: radial-gradient(circle, #35a2ff 0%, #014a88 100%)")
      q-card-section
        |#{STR_CONTACT_BLURB} and my phone number is:
        div.phone-number
          |#{STR_PHONE_NUBMER}

    div.contact-form
      contact
      


      



</template>

<script>
import Experience from "./Containers/Experience";
import Arabesque from "./Shapes/Arabesque";
import Intro from "./Containers/Intro";
import Gear from "./Shapes/Gear";
import ArrowLeft from "./Shapes/ArrowLeft";
import ArrowRight from "./Shapes/ArrowRight";
import ArrowDown from "./Shapes/ArrowDown";
import Skills from "./Containers/Skills";
import SkillsDescription from "./Containers/SkillsDescription";
import Contact from "./Containers/Contact";
import ArrowLeftDown from "./Shapes/ArrowLeftDown";
export default {
  name: "Home",
  components: {
    Experience,
    Arabesque,
    Intro,
    Gear,
    ArrowLeft,
    ArrowRight,
    ArrowDown,
    ArrowLeftDown,
    Skills,
    SkillsDescription,
    Contact
  },
  data: () => ({
    isIe: false,
    STR_EXP: ["Experiences"]
  }),
  methods: {
    beatlogo: function() {
      console.log(this.$refs);
      //const targets = this.$refs["logo"];
      //const logoPath = this.$anime.path(this.$refs["logo-path"]);
      /*this.$anime
        .timeline({ loop: true, direction: "alternate" })
        .add({
          targets: targets,
          translateX: 50,
          translateY: 40,
          scale: this.$anime.random(72, 180) / 100,
          delay: this.$anime.stagger(100)
        }).add({
          targets: this.$refs["logo"],
          skew: [0, 180],
          rotate: logoPath("angle"),
          translateX: logoPath("x"),
          translateY: logoPath("y"),
          easing: "linear",
          duration: 2000
        })*/
    }
  },
  mounted: function() {
    this.beatlogo();
    const ua = window.navigator.userAgent;
    const isIE = /MSIE|Trident/.test(ua);

    if (isIE) {
      this.isIE = true;
    }
  }
};
</script>

<style lang="sass" scoped>
@import '@/assets/sass/_font'
@include font('Aftaserif', '../assets/fonts/Aftaserif')

.nail-one
  transform: rotate(145deg)
  width: 20px
  height: 20px

.nail-two
  transform: rotate(45deg)
  width: 20px
  height: 20px
  z-index: 1

.isIe
  background-color: white

@media (min-width: 1450px)
  .header
    margin-left: 2em
    margin-top: 2em
  .arabesque-div
    position: absolute
    top: -3%
    right: -2%
  .blurbs-intro
    margin-top: -10em

  .experience-div-one
    position: absolute
    top: 40%
    right: 10%

  .nail-one
    position: absolute
    top: 40em
    left: 25em

  .nail-two
    position: absolute
    top: 78em
    right: 63em
</style>
