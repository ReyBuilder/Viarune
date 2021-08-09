<template>
  <div class="about__school" name="about_school">
    <div class="about_school__inner">
      <div class="about_school__title" id="desktop_about_school">
        О школе
      </div>
      <div class="about_school__content">
        <div class="about_school__infoblock">
          <div class="infoblock__item">
            <div class="infoblock_item__ico">
              <img src="./assets/images/about_school/1.svg" alt="" />
            </div>
            <div class="infoblock_item__text">
              Качество уроков всегда на высшем уровне, поскольку каждый урок
              отсматривается и анализируется;
            </div>
          </div>
          <div class="infoblock__item">
            <div class="infoblock_item__ico">
              <img src="./assets/images/about_school/2.svg" alt="" />
            </div>
            <div class="infoblock_item__text">
              Удобная и понятная система для управления <br />
              вашими уроками;
            </div>
          </div>
          <div class="infoblock__item">
            <div class="infoblock_item__ico">
              <img src="./assets/images/about_school/3.svg" alt="" />
            </div>
            <div class="infoblock_item__text">
              Ответы на любые вопросы можно узнать в чате <br />
              с преподавателем;
            </div>
          </div>
          <div class="infoblock__item">
            <div class="infoblock_item__ico">
              <img src="./assets/images/about_school/4.svg" alt="" />
            </div>
            <div class="infoblock_item__text">
              Занятие с опытным преподавателем.
            </div>
          </div>
          <a class="buttonWrapper" href="#desktop_about_subjs" v-smooth-scroll="{ duration: 2000, offset: -50 }">
            <div class="buttonBox buttonOrange">
              Перейти к предметам
            </div>
          </a>
        </div>
        <div class="about_school_man__image">
          <img src="./assets/images/about_school/Man.svg" alt="" />
        </div>
      </div>
    </div>
  </div>
</template>
<style scoped>
/* Button addons */
.buttonWrapper {
  max-width: 236px;
  margin-top: 20px;
  border-radius: 40px;
}
.buttonBox {
  padding: 18px 32px;
  border-radius: 40px;
}
/* About School */
.about__school {
  padding-top: 96px;
  padding-bottom: 172px;
}
.about_school__inner {
  margin: 0 auto;
}
.about_school__title {
  margin-bottom: 38px;

  font-weight: 800;
  font-size: 44px;
  line-height: 54px;

  text-align: center;

  color: #30203d;
}
.about_school__content {
  position: relative;
  max-width: 862px;
  max-height: 636px;
  margin: 0 auto;
}
.about_school_man__image {
  top: 0;
  right: 0;
  margin-right: -100px;
  position: absolute;
}
/* Infoblock */
.about_school__infoblock {
  width: 100%;
  max-width: 660px;

  background: #ffffff;

  box-shadow: 4px 4px 20px rgba(48, 32, 61, 0.1);
  border-radius: 6px;

  margin: 0 auto;
  padding: 30px 92px;
}

.infoblock__item {
  display: flex;
  position: relative;
  align-items: center;
  margin-bottom: 10px;
}

.infoblock_item__text {
  margin-left: 20px;

  font-weight: normal;
  font-size: 16px;
  line-height: 150%;

  color: #30203d;
}
</style>
