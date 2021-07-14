<template>
  <div>
    <intro></intro>
    <About_school></About_school>
  </div>
</template>
<script>
import Intro from "./components/Intro.vue";
import About_school from "./components/Second_part.vue";

export default {
  name: "App",
  components: {
    Intro,
    About_school,
  },
};
</script>

<style>
@import url(~@/assets/fonts/font_gilroy.css);
@import url(~@/assets/BaseStyles.css);
</style>
