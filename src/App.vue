<template>
  <div>
    <intro></intro>
    <About_school></About_school>
    <div class="our_subjects">
      <div class="rudiment">
        <img src="./components/assets/images/rudiment.svg" alt="">
      </div>
      <div class="subj__container">
        <div class="subj__title">
          Наши предметы
        </div>
        <div class="subj__filters">
          <a class="buttonWrapper" href="#">
            <div class="buttonBoxFilter buttonFilter">
              Все
            </div>
          </a>
          <a class="buttonWrapper" href="#">
            <div class="buttonBoxFilter buttonFilter">
              Программирование
            </div>
          </a>
          <a class="buttonWrapper" href="#">
            <div class="buttonBoxFilter buttonFilter">
              Дизайн
            </div>
          </a>
          <a class="buttonWrapper" href="#">
            <div class="buttonBoxFilter buttonFilter">
              Иностранные языки
            </div>
          </a>
          <a class="buttonWrapper" href="#">
            <div class="buttonBoxFilter buttonFilter">
              Школьные предметы
            </div>
          </a>
        </div>
        <div class="subj_cards"></div>
      </div>
    </div>
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
  created() {
    document.title = "Viarune study";
  },
};
</script>
<style>
@import url(~@/assets/fonts/font_gilroy.css);
@import url(~@/assets/BaseStyles.css);
</style>
<style scoped>
/* Our Subjects */
.our_subjects {
  padding-top: 250px;
  position: relative;
}

.rudiment{
  position: absolute;
  top: -200px;
  z-index: -1;
}
.subj__container {
  width: 100%;
  max-width: 1000px;
  margin: 0 auto;
}

.subj__title {
  text-align: center;
  font-weight: 800;
  font-size: 44px;
  line-height: 54px;

  color: #30203d;

  margin-bottom: 39px;
}

/* Filters */
.subj__filters{
  display: flex;
  justify-content: space-between;
}

.buttonBoxFilter {
  font-family: Roboto;
  font-weight: bold;
  font-size: 14px;
  line-height: 16px;
  text-align: center;
  color: #4E3D95;
  text-decoration: none;
  text-align: center;

  cursor: pointer;
  margin: 0;
  padding: 0;
  border-radius: 50px;
  border: 1px solid #4E3D95;;

  display: inline-block;
  vertical-align: top;

  width: 100%;

  padding: 18px 40px 21px;
  border-radius: 50px;
}

</style>
