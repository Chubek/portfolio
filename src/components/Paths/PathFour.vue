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
        id="PathFour"
        d="m 15 25 q 105 -30 263 0 m -265 13 q 105 -31 265 0 m -262 15 q 105 -29 261 0 m
-262 19 q 105 -32 264 0 m -268 25 q 105 -46 275 0 m -279 14 q 105 -40 273 0 m
-265 21 q 105 -46 275 0 m -276 16 q 105 -49 268 0 m -253 13 q 105 -49 268 17 m
-263 15 q 105 -45 268 0"
      />
    </g>
    <g>
      <text
        font-family="Verdana"
        font-size="7"
        fill="rgb(100,200,130)"
        stroke="rgb(0,0,0)"
        stroke-width="0.5"
      >
        <textPath xlink:href="#PathFour">{{ text }}</textPath>
      </text>
    </g>
  </svg>
</template>
<script>
export default {
  name: "PathFour",
  props: {
    text: String
  }
};
</script>
