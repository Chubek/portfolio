<template>
  <svg
    version="1.1"
    id="Layer_1"
    xmlns="http://www.w3.org/2000/svg"
    xmlns:xlink="http://www.w3.org/1999/xlink"
    x="0px"
    y="0px"
    width="820"
    height="820"
    viewBox="0 0 320 240"
    style="enable-background:new 0 0 320 240;"
    xml:space="preserve"
  >
    <g fill="transparent">
      <path
        id="PathFive"
        d="m 15 25 q 105 51 263 0 m -265 13 q 105 54 265 0 m -262 15 q 105 51 261 0 m -262
19 q 105 55 264 0 m -268 25"
      />
    </g>
    <g>
      <text
        font-family="Helvetica"
        font-size="6.19"
        fill="rgb(100,200,130)"
        stroke="rgb(0,0,0)"
        stroke-width="0.2"
      >
        <textPath xlink:href="#PathFive">{{ text }}</textPath>
      </text>
    </g>
  </svg>
</template>
<script>
export default {
  name: "PathFive",
  props: {
    text: String
  }
};
</script>
