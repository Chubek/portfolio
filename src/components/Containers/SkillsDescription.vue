<template lang="pug">
div.main-div
    div(v-if="skillDescOne").skill-desc-one
        div.skill-header-one
            arabesque-header(:width="width" :height="height")
        div.skill-text-one
            |{{ skillDescription }}

    div(v-if="skillDescTwo").skill-desc-two
        div.skill-header-two
            arabesque-header(:width="width" :height="height")
        div.skill-text-two
            |{{ skillDescription }}

    div(v-if="skillDescThree").skill-desc-three
        div.skill-header-three
            arabesque-header(:width="width" :height="height")
        div.skill-text-three
            |{{ skillDescription }}

    div(v-if="skillDescFour").skill-desc-for
        div.skill-header-four
            arabesque-header(:width="width" :height="height")
        div.skill-text-four
            |{{ skillDescription }}

</template>
<script>
import ArabesqueHeader from "../Shapes/ArabesqueHeader";
export default {
  name: "Skill",
  components: {
    ArabesqueHeader
  },
  props: {
    skillDescOne: Boolean,
    skillDescTwo: Boolean,
    skillDescThree: Boolean,
    skillDescFour: Boolean,
    skillDescription: String,
    width: String,
    height: String
  }
};
</script>
<style lang="sass" scoped>
.main-div > div > div:nth-child(2)
    background-color: #994d00
    width: 300px
    margin-top: -20%
    margin-left: 12%
    text-align: justify
    padding: 2em
    border-radius: 2em
    text-shadow: -1px -1px 0 #000, 1px -1px 0 #000, -1px 1px 0 #000, 1px 1px 0 #000
    font-size: 1.2em
    color: white
    

</style>
