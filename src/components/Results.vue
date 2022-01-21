<template>
  <div>
    <p>Reaction time - {{ score }}</p>
    <p class="speed">{{ speed }}</p>
  </div>
</template>

<script>
export default {
  props: ["score"],
  data() {
    return {
      speed: null,
    };
  },
  mounted() {
    console.log(this.score, "ms");
    if (this.score < 250) {
      this.speed = "very fast";
    } else if (this.score >= 250 && this.score < 400) {
      this.speed = "Relatively fast";
    } else {
      this.speed = "Not so fast";
    }
  },
};
</script>

<style>
.speed {
  font-size: 1.4er;
  color: #0faf87;
  font-weight: bold;
}
</style>
