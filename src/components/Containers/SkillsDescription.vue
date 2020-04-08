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
    ArabesqueHeader,
  },
  props: {
    skillDescOne: Boolean,
    skillDescTwo: Boolean,
    skillDescThree: Boolean,
    skillDescFour: Boolean,
    skillDescription: String,
    width: String,
    height: String,
  },
};
</script>
<style lang="sass" scoped>
.main-div > div > div:nth-child(2)
    background-color: #994d00
    width: 200px
    margin-top: -20%
    margin-left: 20%

</style>
