<template>
    <div>
        <intro></intro>
        <div class="about__school">
            <div class="about_school__inner">
                <div class="about_school__title">О школе</div>
                <div class="about_school__infoblock">
                    <div class="infoblock__item">
                        <div class="infoblock_item__ico">
                            <img src="./components/assets/images/about_school/1.svg" alt="">
                        </div>
                        <div class="infoblock_item__text">
                            Качество уроков всегда на высшем уровне, поскольку каждый урок отсматривается и анализируется;
                        </div>
                    </div>
                    <div class="infoblock__item">
                        <div class="infoblock_item__ico">
                            <img src="./components/assets/images/about_school/2.svg" alt="">
                        </div>
                        <div class="infoblock_item__text">
                            Удобная и понятная система для управления <br> вашими уроками;
                        </div>
                    </div>
                    <div class="infoblock__item">
                        <div class="infoblock_item__ico">
                            <img src="./components/assets/images/about_school/3.svg" alt="">
                        </div>
                        <div class="infoblock_item__text">
                            Ответы на любые вопросы можно узнать в чате <br> с преподавателем;
                        </div>
                    </div>
                    <div class="infoblock__item">
                        <div class="infoblock_item__ico">
                            <img src="./components/assets/images/about_school/4.svg" alt="">
                        </div>
                        <div class="infoblock_item__text">
                            Занятие с опытным преподавателем.
                        </div>
                    </div>
                    <div class="buttonBox">
                        <button class="buttonOrange">Перейти к предметам</button>
                    </div>
                    
                </div>
            </div>
        </div>
    </div>
</template>
<script>
import Intro from './components/Intro.vue';

export default {
  name: 'App',
  components: {
    Intro,
  }
}

</script>
<style scoped>
/* Button addons */
button{
    padding: 18px 32px;
    border-radius: 40px;
    margin-top: 20px;
}
/* About School */
    .about__school{
        /* height: 500px; */
        padding-top: 96px;
    }

    .about_school__title{
        margin-bottom: 38px;

        font-weight: 800;
        font-size: 44px;
        line-height: 54px;

        text-align: center;

        color: #30203D;
    }
/* Infoblock */
.about_school__infoblock{
    width: 100%;
    max-width: 660px;

    background: #FFFFFF;

    box-shadow: 4px 4px 20px rgba(48, 32, 61, 0.1);
    border-radius: 6px;

    margin: 0 auto;
    padding: 30px 92px;
}

.infoblock__item{
    display: flex;
    position: relative;
    align-items: center;
    margin-bottom: 10px;
}

.infoblock_item__text{
    margin-left: 20px;

    font-weight: normal;
    font-size: 16px;
    line-height: 150%;

    color: #30203D;
}

</style>
<style>
@import url(~@/components/assets/fonts/font_gilroy.css);

body {
  background: rgba(250, 242, 255, 0.5);
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

/* Button */
.buttonOrange{
    padding: 18px 0;
    /* 63.5px */

    background: linear-gradient(97.42deg, #FB7A0D 0.1%, #FBAE0D 115.11%);
    box-shadow: 1px 4px 15px rgba(248, 132, 13, 0.35);
}

button{
    font-family: Gilroy;
    font-size: 16px;
    font-weight: bold;
    line-height: 19px;
    text-align: center;
    color: #fff;
    text-decoration: none;
    text-align: center;

    cursor: pointer;
    margin: 0;
    padding: 0;
    border: none;

    display: inline-block;
    vertical-align: top;
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

