<template>
 <div>
    <header class="header">
            <div class="header__inner">
                  <nav class="nav">
                    <div class="nav__item">
                      <img src="./components/assets/images/intro/Header_logo.svg" alt="Logo">
                    </div>
                    <a class="nav__item" href="#">О школе</a>
                    <a class="nav__item" href="#">Предметы</a>
                    <a class="nav__item" href="#">Пробный урок</a>
                    <div class="nav__phone">
                        <div class="nav_phone__icon">
                            <img src="./components/assets/icons/icon_intro_call.svg" alt="">
                        </div>
                        <div class="nav_phone__number underlined">+7 912 345-67-89</div></div>
                </nav>
            </div>
    </header>
    <div class="intro">
        <div class="intro__background">
            <img src="./components/assets/images/intro/Intro_bg.svg" alt="">
        </div>
            <div class="container">
                <div class="intro__content">
                    <div class="intro-content__inner">
                        <div class="intro-content__state">
                            <div class="intro__subtitle">Онлайн-школа</div>
                            <div class="intro__title">Viarune study</div>
                            <div class="intro__text">Учим делать игры, сайты, компьютерные программы и мобильные приложения.</div>
                            <button class="buttonA">Подобрать курс</button>
                        </div>
                    </div>
                    
                </div>
            </div>
        </div>
    </div>
    
</template>

<script>

export default {
  name: 'App',
  components: {
  }
}

</script>

<style>
@import url(~@/components/assets/fonts/font_gilroy.css);

body {
  background: rgba(250, 242, 255, 0.5);;
  margin: 0;
  font-family: Gilroy;
  font-style: normal;
  font-weight: normal;
  font-size: 16px;
}

*, *:after, *:before {
    box-sizing: border-box;
}

h1, h2, h3, h4{
    margin: 0;
}

p{
    margin: 0;
    padding: 0;
}

button{
    font-family: Gilroy;
    font-style: normal;
    font-weight: normal;
    margin: 0;
    padding: 0;
    border: none;
}


.underlined{
    position: relative;
    color: #eee;
}

.underlined:hover{
    position: relative;
    color: #F8840D;
    cursor: pointer;
}
.underlined:after{
    display: block;
    content: "";
    width: 100%;
    height: 1px;
    background-color: #eee;
    position: absolute;
    top: 18px;
    opacity: 1;
}
.underlined:hover:after{
    background-color: #F8840D;
}

</style>
<style scoped>

/* Button */
.buttonA{
    width: 100%;
    max-width: 250px;

    display: inline-block;
    vertical-align: top;
    padding: 18px 63.5px;

    background: linear-gradient(97.42deg, #FB7A0D 0.1%, #FBAE0D 115.11%);
    box-shadow: 1px 4px 15px rgba(248, 132, 13, 0.35);
    border-radius: 40px;
    margin-top: 34px;

    font-size: 16px;
    font-weight: bold;
    line-height: 19px;
    text-align: center;
    color: #fff;
    text-decoration: none;

    cursor: pointer;
}

/*Intro*/
.intro{
    width: 100%;
    position: relative;
}

.intro__background img{
    width: 100%;
    object-fit: cover;
}

.intro__content{
    top: 0;
    position: absolute;
    margin-top: 20%;

}

.intro-content__inner{
    display: flex;
    align-items: center;
}
.intro-content__state{
    font-family: Gilroy;
    font-style: normal;
    color: #fff;
    width: 100%;
    max-width: 460px;
}

.intro__subtitle{
    font-weight: normal;
    font-size: 28px;
    line-height: 32px
}

.intro__title{
    font-weight: 800;
    font-size: 54px;
    line-height: 66px;
    margin-bottom: 5px;
}

.intro__text{
    font-weight: 500;
    font-size: 18px;
    line-height: 150%;
}


/*Header*/
.header{
    top: 0;
    left: 0;
    right: 0;
    position: absolute;
    /* border-bottom: 1px solid rgba(255,255,255,0.2); */
    z-index: 1000;
    width: 100%;
}


/*Nav*/
.nav{
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

.nav__item{
    color: #eee;
    text-decoration: none;
    font-style: normal;
    font-weight: 600;
    line-height: 19px;

    display: inline-block;
    vertical-align: top;

    position: relative;
}

 .nav__item:hover{
    font-weight: 500;
    color: #F8840D;
}
.nav__item:after{
    display: block;
    content: "";
    opacity: 0;
    width: 100%;
    height: 1px;
    font-weight: 500;
    color: #F8840D;
    background-color: #F8840D;
    position: absolute;
    top: 18px;
    /* transition: opacity .1s linear; */
}

.nav__item:active:after{
    opacity: 1;
}

.nav__phone{
    display: flex;
    align-items: center;
    font-weight: 500;
    line-height: 19px;
}

.nav_phone__number{
    /* padding-top: 2px; */
    padding-bottom: 4px;
}

/*Container*/
.container{
    width: 100%;
    margin: 0 auto;
    max-width: 1100px;
}

.container__intro{
    width: 100%;
    margin: 0 auto;
    max-width: 1100px;
}
.pidorasi_atakuyut{
  margin-top: 20px;
}

/* @import url("components/assets/fonts/stylesheet.css"); */

</style>
