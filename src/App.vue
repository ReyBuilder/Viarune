<template>
 <div>
    <header class="header">
            <div class="header__inner">
                  <nav class="nav">
                    <div class="nav__item">
                      <img src="./components/assets/images/intro/Header_logo.svg" alt="Logo">
                    </div>
                    <a class="nav__item" href="#">Услуги</a>
                    <a class="nav__item" href="#">Предметы</a>
                    <a class="nav__item" href="#">Пробный урок</a>
                    <a class="nav__item" href="#">Контакты</a>
                    <a class="nav__item" href="#">+7 912 345-67-89</a>
                </nav>
            </div>
    </header>
    <div class="intro">
          <div class="intro__content">
              
          </div>
      </div>
      <div class="pidorasi_atakuyut">
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Dolorum illum quisquam enim sed numquam nesciunt at blanditiis, necessitatibus, provident optio magnam aperiam? Molestias porro, doloremque necessitatibus reprehenderit distinctio repellendus asperiores? <br>
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Quisquam, ut doloribus. Illo, quia velit perferendis itaque autem id ullam eaque dolore odit temporibus quisquam delectus ut sint, architecto ducimus quo. <br>
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
</style>
<style scoped>
/*Intro*/
.intro{
    width: 100%;
    /* max-width: 1600px; */
    /* height: 110vh; */
    height: 1050px;

    background: url("components/assets/images/intro/Intro_bg.svg") center no-repeat;
    background-size: cover;

    display: flex;
    flex-direction: column;
    justify-content: center;
}

/*Header*/
.header{
    top: 0;
    left: 0;
    right: 0;
    position: absolute;
    border-bottom: 1px solid rgba(255,255,255,0.2);
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
    color: #fff;
    text-decoration: none;
    font-style: normal;
    font-weight: 600;
    line-height: 19px;

    display: inline-block;
    vertical-align: top;

    position: relative;
}


/*Container*/
.container{
    width: 100%;
    margin: 0 auto;
    max-width: 1200px;
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
