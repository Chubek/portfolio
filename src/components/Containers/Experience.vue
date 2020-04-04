<template lang="pug">
div.mainDiv
    q-card(ref="exp-container"
     style="background: radial-gradient(circle, #35a2ff 0%, #014a88 100%)"
       ).text-white.exp-container
      q-card-section
        |{{ experience }}

    
</template>

<script>
export default {
  name: "Experience",
  props: {
    experience: String
  },
  data: () => ({
    circleToggle: true,
    squareToggle: true,
    triangleToggle: true,
    trapezoidToggle: true
  }),
  methods: {
    rollCircle: function() {
      console.log(this.$refs);
      const targets = this.$el;      
      console.log(targets);
      this.$anime({
        targets: targets,
        translateX: 270,
        scale: this.$anime.random(72, 180) / 100,
        delay: this.$anime.stagger(100),
        loop: true

      });
    }
  },
  mounted: function() {
    this.rollCircle();
  }
};
</script>

<style lang="sass" scoped>

.exp-container
  max-width: 300px
  text-align: justify
</style>
