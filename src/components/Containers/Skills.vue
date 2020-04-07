<template>
  <div class="skills-div">
    <div v-for="(skill, index) in skills" :key="index">
      <svg
        version="1.1"
        id="Capa_1"
        xmlns="http://www.w3.org/2000/svg"
        xmlns:xlink="http://www.w3.org/1999/xlink"
        x="0px"
        y="0px"
        width="500"
        height="500"
        viewBox="0 0 512 512"
        style="enable-background: new 0 0 512 512;"
        xml:space="preserve"
      >
        <rect
          x="207.37"
          y="377.121"
          style="fill: #aaa8ae;"
          width="97.26"
          height="82.5"
        />
        <rect
          x="256"
          y="377.121"
          style="fill: #808081;"
          width="48.628"
          height="82.5"
        />
        <path style="fill: #666666;" d="M512,392.116H0V37.39h512V392.116z" />
        <path style="fill: #4d4d4d;" d="M512,392.116H256V37.39h256V392.116z" />
        <path style="fill: #ebebec;" d="M512,392.116H0v-74.234h512V392.116z" />
        <g>
          <path
            style="fill: #cbcacd;"
            d="M512,392.116H256v-74.234h256V392.116z"
          />
          <rect
            x="148.85"
            y="444.611"
            style="fill: #cbcacd;"
            width="214.29"
            height="30"
          />
        </g>
        <rect
          x="256"
          y="444.611"
          style="fill: #aaa8ae;"
          width="107.15"
          height="30"
        />

        <text font-size="50" transform="translate(50, 250)">
          {{ skill.name }}
        </text>
        
      </svg>
      <div> <img :src="skill.logo" /> </div>
    </div>
  </div>
</template>

<script>
import EN from "../../assets/strings/en";
import _ from "lodash";
export default {
  data: () => ({
    skills: EN.SKILLS,
    rands: [],
  }),
  mounted: function () {
    this.skills.forEach(() => {
      this.rands.push(_.random(5, 25));
    });
  },
};
</script>
<style lang="sass" scoped>
.skills-div
    margin-left: 20em
</style>
