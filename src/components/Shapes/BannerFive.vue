<template>
  <svg
    :width="size.width"
    :height="size.height"
    viewBox="0 0 600 600"
    xmlns="http://www.w3.org/2000/svg"
  >
    <g transform="translate(300,300)">
      <path
        d="M116,-163.4C131.8,-125.1,113.2,-70.9,130.5,-16.5C147.9,37.9,201.3,92.4,199.5,133.6C197.7,174.7,140.7,202.5,84.7,215.4C28.6,228.3,-26.6,226.5,-76.9,209.1C-127.2,191.7,-172.7,158.9,-177.2,118.2C-181.6,77.6,-145,29.3,-130.3,-17.7C-115.7,-64.6,-123.1,-110,-105,-148C-87,-186,-43.5,-216.5,3.3,-220.5C50.1,-224.4,100.3,-201.8,116,-163.4Z"
        fill="#ff6900"
      />
    </g>
  </svg>
</template>
<script>
export default {
  name: "BannerFive",
  props: {
    text: String,
    size: Object,
  },
};
</script>
