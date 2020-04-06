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
        id="PathTwo"
        d="m 12 11 l 261 0 m -224 13 l 222 0 m -191 13 l 188 0 m -164 13 h 164 m -163 9 l
163 14 m -168 -2 l 167 15 m -170 -1 l 173 15"
      />
    </g>
    <g>
      <text
        font-family="Verdana"
        font-size="5"
        fill="rgb(100,200,130)"
        stroke="rgb(0,0,0)"
        stroke-width="0.2"
      >
        <textPath xlink:href="#PathTwo">{{ text }}</textPath>
      </text>
    </g>
  </svg>
</template>
<script>
export default {
  name: 'PathOne',
  props: {
    text: String
  }
}
</script>
