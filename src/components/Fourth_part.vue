<template>
    <div class="appointment__main">
        <div class="appointment__bg">
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
                <form class="appointment_input__form">
                    <div class="form__item">
                        <input class="inputCustom" href="#" />
                    </div>
                    <div class="form__item">
                        <input class="inputCustom" type="text" />
                    </div>
                    <!-- Телефонька -->
                    <div class="form__item">
                        <input v-on:input.prevent="phoneValidation" v-model="phone" class="inputCustom" type="text" maxlength="16"/>
                    </div>
                    <div class="form_item__checkbox form__item">
                        <input
                            type="checkbox"
                            id="subscribe"
                            name="subscribe"
                            value="newsletter"
                        />
                        <label for="subscribe"
                            >Я согласен с условиями обработки <br />
                            персональных данных
                        </label>
                    </div>
                    <div>
                        <a class="buttonBox buttonOrange" href="#">
                            Записаться
                        </a>
                    </div>
                </form>
            </div>
        </div>
    </div>
</template>
<script>

export default ({
    methods:{
        phoneValidation:function(){
            if (this.phone.substring(0,2)!=="+7")
                this.phone = "+7"+this.phone;
            if (!this.phone[2] && this.phone[2]!==' ')
                this.phone=this.phone.substring(0,2)+" "+this.phone.substring(2, this.phone.length);
            if (!this.phone[6] && this.phone[6]!==' ')
                this.phone=this.phone.substring(0,6)+" "+this.phone.substring(6, this.phone.length);
        }
    },
    data() {
        return {
            phone:"+7",
            phoneError:"",
        }
    }
})
</script>

<style scoped>
.buttonBox {
    padding: 18px 125px;
    border-radius: 30px;
}

.buttonBox:focus {
    box-shadow: 0 0 0 2px #FEFCFF,
                0 0 0 3px #30203D;
}
/* Main part & background */
.appointment__main {
    position: relative;
    width: 100%;
    background: url("./assets/images/appointment/appointment_bg2.svg");
    background-size: cover;
    background-position: center center;
    padding-top: 210px;
    padding-bottom: 24%;
}

.appointment__content {
    top: 0;
    margin-top: 27px;
    width: 100%;
    max-width: 405px;
}

.appointment__header {
    margin: 0 auto;

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

.form_item__checkbox {
    position: relative;
    display: flex;
    align-items: flex-start;

    width: 100%;
    max-width: 338px;
}

.container {
    width: 100%;
    margin: 0 auto;
    max-width: 925px;
}

/* Inputs */
.inputCustom {
    background: #ffffff;
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

.inputCustom:focus {
    outline: none;
    box-shadow: 0 0 0 2px #FEFCFF,
                0 0 0 3px #30203D;
}

label {
    font-weight: 500;
    font-size: 14px;
    line-height: 150%;

    color: rgba(48, 32, 61, 0.6);
}
.checkbox {
    background: #feffff;
    border: 0.5px solid rgba(48, 32, 61, 0.6);
    border-radius: 9px;
}
</style>
