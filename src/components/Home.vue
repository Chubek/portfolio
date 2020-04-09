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
            li
                <a href="https://www.github.com/chubek">My Github</a>

    div.header
        gear
    

    div.arabesque-div-large
        arabesque(width="1200" height="1200")
        
    section(id="intro")
        div.intro-arrow
            arrow-left(:texts=[STR_SITE_SUBTITLE_WMD, STR_SITE_SUBTITLE_AI, STR_SITE_SUBTITLE_GD, STR_SITE_SUBTITLE_BOT])

        div.blurbs-intro
            intro(intro=STR_SITE_DESC)
    hr

    section(id="experience")
        div.experience-arrow
            arrow-right(:texts="STR_EXP")

        div.experiences
            div.experience-div-one
                experience(experience=STR_EXP_TETRIS width="982" height="982" BannerOne)

            div.experience-div-two 
                experience(experience=STR_EXP_WORDPRESS width="782" height="782" BannerTwo)

            div.experience-div-three 
                experience(experience=STR_BEDLAM width="912" height="1012" BannerThree)

            div.experience-div-four 
                experience(experience=STR_EXP_EKELAAS width="1080" height="1080" BannerFour)

            div.experience-div-four
                experience(experience=STR_EXP_MOODIMEDIA width="612" height="612" BannerFive)
    hr
    
    section(id="skills")
        div.skills-arrow
            arrow-down(text=STR_SKILL)

        
        div.skills-and-desc
            div.skills-div
                skills(width="512" height="512" imageWidth="225" imageHeight="218")

            duv.skills-desc-div
                div.skills-desc-one
                    skills-description(skillDescOne width="400" height="200" skillDescription=STR_SKILL_AI)
    
                div.skills-desc-two
                    skills-description(skillDescTwo width="400" height="200" skillDescription=STR_SKILL_APP)

                div.skills-desc-three
                    skills-description(skillDescThree width="400" height="200" skillDescription=STR_SKILL_GAME_DEV)

                div.skills-desc-four
                    skills-description(skillDescFour width="400" height="200" skillDescription=STR_SKILL_BOT)

    hr

    section(id="contact")
        div.arrow-contact
            arrow-left-down(text=STR_CONTACT)
        div.contact-div
            q-card(style="background: radial-gradient(circle, #ff9933 0%, #cc0000 100%)")
                q-card-section
                    |#{STR_CONTACT_BLURB} My phone number and email are:
                    div.phone-number
                        <a href="tel:09385130604">09385130604</a> 
                    div.email
                        <a href="mailto:chubakbidpaa@gmail.com">Chubakbidpaa@gmail.com</a>

    section(id="footer")
        div.footer-div
            |Copyright℗ {{ year }} by Chubak Bidpaa - All Rights Reserved


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
    SkillsDescription
  },
  data: () => ({
    STR_EXP: ["Experiences"],
    year: (new Date().getYear() - 100) + 2000
  })
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

hr
    border: 4px dotted #b30000
    border-radius: 5px

.experiences
    display: flex
    flex-wrap: wrap
    align-items: center
    margin-top: 20em

.skills-and-desc
    display: flex

.footer-div
    background-color: orange
    padding-left: 1em
    opacity: 50%

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
        margin-bottom: -20em

    .intro-arrow
        margin-top: -10%
        margin-left: 28%

    .experience-arrow
        position: absolute
        top: 165em
        left: 25%

    .skills-arrow
        margin-left: 25%

    .skills-desc-div
        margin-left: 20em

    .arrow-contact
        position: relative
        top: -4em
        z-index: 1
        left: 35%

    .contact-div
        width: 700px
        height: 500px
        padding: 2em
        position: relative
        top: -15em
        left: 30%
        text-align: justify
        font-size: 1.6em




</style>
