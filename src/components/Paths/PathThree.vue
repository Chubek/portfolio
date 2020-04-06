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
        id="PathThree"
        d="m 12 11 l 261 0 m -224 13 l 222 0 m -191 13 l 188 0 m -213 4 c 0 16 142 0 179 15
m -170 16 c 79 -15 0 0 173 15 m -170 11 l 172 0 m -191 21 c 170 -17 79 67 207 -9
m -231 10 c 0 0 0 66 262 16 m -248 33 h 276"
      />
    </g>
    <g>
      <text
        font-family="Helvetica"
        font-size="5"
        fill="rgb(100,200,130)"
        stroke="rgb(0,0,0)"
        stroke-width="0.2"
      >
        <textPath xlink:href="#PathThree">{{ text }}</textPath>
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
