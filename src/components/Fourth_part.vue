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
           <input class="inputCustom" href="#">
        </div>
          <div class="form__item">
            <input class="inputCustom" type="text" />
          </div>
          <div class="form__item">
            <input class="inputCustom" type="text" />
          </div>
          <div class="form_item__checkbox form__item">
              <input type="checkbox" id="subscribe" name="subscribe" value="newsletter">
              <label for="subscribe">Я согласен с условиями обработки <br> персональных данных</label>
          </div>
          <div>
              <a class="buttonBox buttonOrange" href="#">Записаться</a>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<style scoped>

.buttonBox {
  padding: 18px 125px;
  border-radius: 30px;
}

.buttonBox:focus{
    outline-offset: 3px;
    outline: 1px solid #30203D;
}
/* Main part & background */
.appointment__main {
  position: relative;
  width: 100%;

  padding-top: 210px;
  padding-bottom: 24%;
  /* max-height: 1046px; */
}

.appointment__bg img {
  width: 100%;
  object-fit: cover;
  position: absolute;
  z-index: -1;
  margin-top: -210px;
  /* max-height: 1046px; */
}

.appointment__content {
  top: 0;
  /* bottom: 0; */
  /* position: absolute; */
  margin-top: 27px;
  /* margin-bottom: 274px; */

  width: 100%;
  max-width: 405px;;
}

.appointment__header {
  margin: 0 auto;

  /* padding-top: 20%; */
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
}
.form__item {
  margin-bottom: 20px;
}

.form_item__checkbox{
    position: relative;
    display: flex;
    align-items: flex-start;

    width: 100%;
    max-width: 338px;
}

.container {
    /* top: 0; */
  width: 100%;
  margin: 0 auto;
  max-width: 950px;
  /* position: relative; */
}

/* Inputs */
.inputCustom{
    background: #FFFFFF;
    border: 0.5px solid rgba(48, 32, 61, 0.6);
    box-sizing: border-box;
    border-radius: 30px;

    font-weight: normal;
    font-size: 14px;
    line-height: 16px;
    padding: 17px 44px 17px 20px;
    color: rgba(48, 32, 61, 0.6);

    width: 100%;
    max-width: 338px;
}

.inputCustom:focus{
    outline-offset: 3px;
    outline: 1px solid #30203D;
}

label {
    font-weight: 500;
    font-size: 14px;
    line-height: 150%;

    color: rgba(48, 32, 61, 0.6);
}
.checkbox{
    background: #FEFFFF;
    border: 0.5px solid rgba(48, 32, 61, 0.6);
    border-radius: 9px;
}

</style>
