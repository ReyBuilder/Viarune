<template>
    <div class="popup-wrapper" v-if="active" v-on:click="$emit('close')">
        <div class="popup">
            <div class="popup__close"><div class="popup__close__button" v-on:click="$emit('close')"></div></div>
            <div class="popup__content">Спасибо, мы свяжемся с вами в ближайшее время!</div>
            <a class="popup__button">Окей</a>
        </div>
    </div>
</template>
<script>
export default {
    name: "App",
    props: {
        active: Boolean
    }
}
</script>
<style scoped>
    .popup-wrapper {
        width: 100vw;
        height: 100vh;
        background: rgba(62, 58, 68, 0.52);
        display: flex;
        justify-content: center;
        align-items: center;
        position: fixed;
        top: 0;
        left: 0;
        z-index: 20;
    }
    .popup {
        width: 340px;

        background: #FEFCFF;
        box-shadow: 0px 10px 40px rgba(0, 0, 0, 0.1);
        border-radius: 6px;
        text-align: center;
    }
    .popup__button {
        background: linear-gradient(141.18deg, #4E3D95 -8.71%, #413373 104.75%);
        border-radius: 40px;
        padding: 18px 60px;
        display: inline-block;
        color: white;
        margin-bottom: 30px;
        font-weight: bold;
        font-size: 16px;
        text-decoration: none;
        cursor: pointer;
    }
    .popup__content {
        font-weight: 500;
        font-size: 18px;
        padding: 20px 43px 23px;
    }
    .popup__close {
        display: flex;
        padding: 12px;
        justify-content: flex-end;
    }
    .popup__close__button {
        width: 42px;
        height: 42px;
        background: url("./assets/images/PopUp_Close.svg");
        cursor: pointer;
    }
    .popup__close__button:hover {
        background: url("./assets/images/PopUp_CloseHover.svg");
    }
</style>