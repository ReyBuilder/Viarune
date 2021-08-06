<template>
  <div>
	<Intro></Intro>
	<About_school></About_school>
	<About_subj></About_subj>
	<Appointment></Appointment>
	<Footer></Footer>
	<PopUp></PopUp>
  </div>
</template>
<script>
import Intro from "./components/Intro.vue";
import About_school from "./components/Second_part.vue";
import About_subj from "./components/Third_part.vue";
import Appointment from "./components/Fourth_part.vue";
import Footer from "./components/Footer.vue"
import PopUp from "./components/Pop_Up.vue"

export default {
  name: "App",
  components: {
	Intro,
	About_school,
	About_subj,
	Appointment,
	Footer,
	PopUp,
  },
  created() {
	document.title = "Viarune study";
  },
};
</script>
<style>
@import url(~@/assets/fonts/font_gilroy.css);
@import url(~@/assets/BaseStyles.css);
</style>
