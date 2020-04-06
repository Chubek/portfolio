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
        id="PathOne"
        d="m 20 9 a 2 -2 0 0 0 56 0 m 4 0 a 13 11 0 0 0 139 0 m -216 60 l 255 17 m -245 26
c 0 70 62 37 125 -2 m -2 0 q 125 50 91 -17 m -97 42 l 159 53 m -269 -18 c 22 59
41 0 172 6 m 1 0 l 88 56 m -253 -16 c 0 0 0 79 174 -17 m -72 52 h 150 m -270 27
q 128 30 278 0"
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
        <textPath xlink:href="#PathOne">{{ text }}</textPath>
      </text>
    </g>
  </svg>
</template>
<script>
export default {
  name: "PathOne",
  props: {
    text: String
  }
};
</script>