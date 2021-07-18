<template>
    <div class="appointment__main">
        <div class="appointment__bg">
            <img src="./assets/images/appointment/appointment_bg2.svg" alt="appointment__bg">
        </div>
        <div class="container">
            <div class="appointment__content">
                <div class="appointment__header">
                    <div class="appointment__title">
                        Записаться на пробный урок
                    </div>
                    <div class="appointment__text">
                        Приглашаем вас познакомиться с нашими преподавателями
                    </div>
                </div>
                <div class="appointment_input__form">

                </div>
            </div>
        </div>
    </div>
</template>
<style scoped>
/* Main part & background */
.appointment__main{
    position: relative;
    width: 100%;
}

.appointment__bg img {
  width: 100%;
  object-fit: cover;
}

.appointment__content{
    top: 0;  
    bottom: 0;
    position: absolute;
    margin: 0 auto;
}
.appointment__header{
    position: relative;
    margin-top: 200px;
    text-align: center;
    color: #fff;
}
.appointment__title{
    font-weight: 800;
    font-size: 44px;
    line-height: 54px;
    margin-bottom: 28px;
}

.appointment__text{
    max-width: 490px;
    font-weight: 500;
    font-size: 18px;
    line-height: 150%;
    margin: 0 auto;
}
/* Input form */
.appointment_input__form{
    background: #FEFCFF;
    box-shadow: 0px 10px 40px rgba(0, 0, 0, 0.1);
    border-radius: 6px;
    padding: 40px 34px;
    /* margin-left: 337px; */

    height: 408px;
    width: 405px;
    
}

.container {
  width: 100%;
  margin: 0 auto;
  max-width: 1000px;

}
</style>