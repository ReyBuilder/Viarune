<template>
    <div class="appointment__main">
        <div class="appointment__bg">
            <img src="./assets/images/appointment/appointment_bg2.svg" alt="appointment__bg">
        </div>
        <div class="appointment__content">
            <div class="appointment__header">
                <div class="appointment__title">
                    Записаться на пробный урок
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
    position: absolute;
}
.appointment__header{
    /* position: relative; */
    margin-top: 200px;
    text-align: center;
}
.appointment__title{
    font-weight: 800;
    font-size: 44px;
    line-height: 54px;
    color: #fff;
}
</style>