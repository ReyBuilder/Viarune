<template>
  <div>
    <header class="header">
      <div class="header__inner">
        <nav class="nav">
          <div class="nav__item">
            <img src="./assets/images/intro/Header_logo.svg" alt="Logo" />
          </div>
          <a class="nav__item" href="#">О школе</a>
          <a class="nav__item" href="#">Предметы</a>
          <a class="nav__item" href="#">Пробный урок</a>
          <div class="nav__phone">
            <div class="nav_phone__icon">
              <img src="./assets/icons/icon_intro_call.svg" alt="" />
            </div>
            <div class="nav_phone__number underlined">+7 912 345-67-89</div>
          </div>
        </nav>
      </div>
    </header>
    <div class="intro">
      <div class="intro__background">
        <img src="./assets/images/intro/Intro_bg2.svg" alt="" />
      </div>
      <div class="container">
        <div class="intro__content">
          <div class="intro-content__inner">
            <div class="intro-content__state">
              <div class="intro__subtitle">Онлайн-школа</div>
              <div class="intro__title">Viarune study</div>
              <div class="intro__text">
                Мы работаем чтобы сделать образование комфортным, доступным и
                качественным.
              </div>
              <a class="buttonWrapper" href="#">
                <div class="buttonBox buttonOrange">
                  Подобрать курс
                </div>
              </a>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
/* Button radius&paddings */
.buttonBox {
  padding: 18px 63px;
  border-radius: 40px;
}
.buttonWrapper {
  max-width: 256px;
  border-radius: 40px;
}

/*Intro*/
.intro {
  width: 100%;
  position: relative;
}

.intro__background img {
  width: 100%;
  object-fit: cover;
}

.intro__content {
  top: 0;
  position: absolute;
  margin-top: 20%;
}

.intro-content__inner {
  display: flex;
  align-items: center;
}
.intro-content__state {
  font-family: Gilroy;
  font-style: normal;
  color: #fff;
  width: 100%;
  max-width: 460px;
}

.intro__subtitle {
  font-weight: normal;
  font-size: 28px;
  line-height: 32px;
}

.intro__title {
  font-weight: 800;
  font-size: 54px;
  line-height: 66px;
  margin-bottom: 5px;
}

.intro__text {
  font-weight: 500;
  font-size: 18px;
  line-height: 150%;
  margin-bottom: 34px;
}

/*Header*/
.header {
  top: 0;
  left: 0;
  right: 0;
  position: absolute;
  z-index: 1000;
  width: 100%;
}

/*Nav*/
.nav {
  font-weight: 500;
  line-height: 20px;
  padding-top: 40px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  width: 100%;
  max-width: 1100px;
  margin-left: auto;
  margin-right: auto;
}

.nav__item {
  color: #eee;
  text-decoration: none;
  font-style: normal;
  font-weight: 600;
  line-height: 19px;

  display: inline-block;
  vertical-align: top;

  position: relative;
}

.nav__item:hover {
  font-weight: 500;
  color: #f8840d;
}

.nav__item:after {
  display: block;
  content: "";
  opacity: 0;
  width: 100%;
  height: 1px;
  font-weight: 500;
  color: #f8840d;
  background-color: #f8840d;
  position: absolute;
  top: 18px;
  /* transition: opacity .1s linear; */
}

.nav__item:active:after {
  opacity: 1;
}

.nav__phone {
  display: flex;
  align-items: center;
  font-weight: 500;
  line-height: 19px;
}

.nav_phone__number {
  /* padding-top: 2px; */
  padding-bottom: 4px;
}

/*Container*/
.container {
  width: 100%;
  margin: 0 auto;
  max-width: 1100px;
}

.container__intro {
  width: 100%;
  margin: 0 auto;
  max-width: 1100px;
}
</style>
