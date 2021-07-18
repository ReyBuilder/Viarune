<template>
  <div class="appointment__main">
    <div class="appointment__bg">
      <img
        src="./assets/images/appointment/appointment_bg2.svg"
        alt="appointment__bg"
      />
    </div>
    <div class="container">
      <div class="appointment__header">
        <div class="appointment__title">
          Записаться на пробный урок
        </div>
        <div class="appointment__text">
          Приглашаем вас познакомиться с нашими преподавателями
        </div>
      </div>
      <div class="appointment__content">
        <div class="appointment_input__form">
          <div class="form__item">
            <input class="inputWrapper" type="text" />
          </div>
          <div class="form__item">
            <input type="text" />
          </div>
          <div class="form__item">
            <input type="text" />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<style scoped>
/* Main part & background */
.appointment__main {
  position: relative;
  width: 100%;
  max-height: 1046px;
  margin-bottom: 364px;
}

.appointment__bg img {
  width: 100%;
  object-fit: cover;
}

.appointment__content {
  top: 0;
  bottom: 0;
  position: absolute;
  margin: 364px auto 274px;
}

.appointment__header {
  top: 0;
  bottom: 0;
  right: 0;
  left: 0;
  position: absolute;
  margin: 0 auto;

  margin-top: 200px;
  text-align: center;
  color: #fff;
}
.appointment__title {
  font-weight: 800;
  font-size: 44px;
  line-height: 54px;
  margin-bottom: 28px;
}

.appointment__text {
  max-width: 490px;
  font-weight: 500;
  font-size: 18px;
  line-height: 150%;
  margin: 0 auto;
}
/* Input form */
.appointment_input__form {
  background: #fefcff;
  box-shadow: 0px 10px 40px rgba(0, 0, 0, 0.1);
  border-radius: 6px;
  padding: 40px 34px;
  /* margin-left: 337px; */

  /* height: 408px;
    width: 405px; */
}
.form__item {
  margin-bottom: 20px;
}

.container {
  width: 100%;
  margin: 0 auto;
  max-width: 900px;
  /* position: absolute; */
}
/* Input */
.inputWrapper{
    background: #FFFFFF;
    border: 0.5px solid rgba(48, 32, 61, 0.6);
    box-sizing: border-box;
    border-radius: 30px;
    font-weight: normal;
    font-size: 14px;
    line-height: 16px;
    padding: 17px 44px 17px 20px;
    color: rgba(48, 32, 61, 0.6);
}
</style>
