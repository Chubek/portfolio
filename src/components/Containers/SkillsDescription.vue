<template lang="pug">
div.main-div
    div(v-if="skillDescOne").skill-desc-one
        div.skill-header-one
            arabesque-header(:size="size")
        div.skill-text-one
            {{ skillDescription }}

    div(v-if="skillDescTwo").skill-desc-two
        div.skill-header-two
            arabesque-header(:size="size")
        div.skill-text-two
            {{ skillDescription }}

    div(v-if="skillDescThree").skill-desc-three
        div.skill-header-three
            arabesque-header(:size="size")
        div.skill-text-three
            {{ skillDescription }}

    div(v-if="skillDescFour").skill-desc-for
        div.skill-header-four
            arabesque-header(:size="size")
        div.skill-text-four
            {{ skillDescription }}

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
    size: Object
  }
};
</script>