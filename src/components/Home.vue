<template lang="pug">
include ../assets/strings/en.pug



div.main-div
    div.app-bar
        ul.app-bar-ul
            li
                <a href="#intro">Intro</a>
            li
                <a href="#experience">Experience</a>
            li
                <a href="#skills">Skills</a>
            li
                <a href="#contact">Contact</a>

    div.header
        gear
    

    div.arabesque-div-large
        arabesque(width="1200" height="1200")
        
    section(id="intro")
        div.intro-arrow
            arrow-left(:texts=[STR_SITE_SUBTITLE_WMD, STR_SITE_SUBTITLE_AI, STR_SITE_SUBTITLE_GD, STR_SITE_SUBTITLE_BOT])

        div.blurbs-intro
            intro(intro=STR_SITE_DESC)

    section(id="experience")
        div.experience-arrow()
            arrow-right(:texts="STR_EXP")

        div.experience-div-one
            experience(experience=STR_EXP_TETRIS width="512" height="512" BannerOne)

        div.experience-div-two 
            experience(experience=STR_EXP_WORDPRESS width="512" height="512" BannerTwo)

        div.experience-div-three 
            experience(experience=STR_BEDLAM width="512" height="512" BannerThree)

        div.experience-div-four 
            experience(experience=STR_EXP_EKELAAS width="512" height="512" BannerFour)

        div.experience-div-four
            experience(experience=STR_EXP_MOODIMEDIA width="512" height="512" BannerFive)

    
    section(id="skills")
        div.skills-arrow()
            arrow-down(text=STR_SKILL)

        div.skills-div
            skills(width="512" height="512" imageWidth="250" imageHeight="250")

        div.skills-desc-one
            skills-description(skillDescOne width="400" height="200" skillDescription=STR_SKILL_AI)
    
        div.skills-desc-two
            skills-description(skillDescTwo width="400" height="200" skillDescription=STR_SKILL_APP)

        div.skills-desc-three
            skills-description(skillDescThree width="400" height="200" skillDescription=STR_SKILL_GAME_DEV)

        div.skills-desc-four
            skills-description(skillDescFour width="400" height="200" skillDescription=STR_SKILL_BOT)

    

    section(id="contact")
        div.arrow-contact
            arrow-left-down(text=STR_CONTACT)
        div.contact-div
            q-card(style="background: radial-gradient(circle, #35a2ff 0%, #014a88 100%)")
                q-card-section
                    |#{STR_CONTACT_BLURB} and my phone number is:
                    div.phone-number
                        <a href="tel:09385130604">09385130604</a> 
                    div.email
                        <a href="mailto:chubakbidpaa@gmail.com">Chubakbidpaa@gmail.com</a>

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
  },
  data: () => ({
    STR_EXP: ["Experiences"],
  }),
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

.app-bar a
    color: white
    text-decoration: none

.app-bar a:hover
    color: black


.app-bar-ul
    display: flex
    list-style: none
    background-color: #4d0000
    padding: 3px

.app-bar-ul li
    margin: 2px
    padding: 4px
    background-color: #cc0000
    border: 1px solid
    border-radius: 12px

.app-bar-ul li:hover
    background-color: #ff1a1a
 

@media (min-width: 1450px)
    .header
        margin-left: 2em
        margin-top: 2em
    .arabesque-div-large
        position: absolute
        top: -5em
        right: -4em
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

    .intro-arrow
        margin-top: -10%
        margin-left: 28%
</style>
