<template>
    <div class="footer__container">
        <div class="footer__main">
            <div class="title">
                <div class="title__inner">Свяжитесь с нами</div>
            </div>
            <div class="contacts">
                <div class="block">
                    <div class="block__text">Наши соц.сети:</div>
                    <div class="block__content">
                        <a class="icon__wrapper" href="#">
                            <div class="iconBox" id="vk"></div>
                        </a>
                        <a
                            class="icon__wrapper"
                            href="https://www.facebook.com/groups/352779019914924/about"
                        >
                            <div class="iconBox" id="fb"></div>
                        </a>
                        <a
                            class="icon__wrapper"
                            href="https://www.instagram.com/viarunestudy/"
                        >
                            <div class="iconBox" id="inst"></div>
                        </a>
                    </div>
                </div>
                <div class="block">
                    <div class="block__text">По номеру телефона:</div>
                    <div class="block__content">
                        <div>
                            <img src="./assets/icons/icon_call.svg" alt="" />
                        </div>
                        <div>+7 912 013 39-97</div>
                    </div>
                </div>
                <div class="block">
                    <div class="block__text">Наши мессенджеры:</div>
                    <div class="block__content">
                        <a class="icon__wrapper" href="#">
                            <div class="iconBox" id="tg"></div>
                        </a>
                        <a
                            class="icon__wrapper"
                            href="https://wa.me/79120133997"
                        >
                            <div class="iconBox" id="ws"></div>
                        </a>
                        <a class="icon__wrapper" href="#">
                            <div class="iconBox" id="vb"></div>
                        </a>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>
<style scoped>
.footer__main {
    position: relative;

    font-weight: 500;
    color: #30203d;
}

.block {
    font-size: 16px;
}

.block__content {
    display: flex;
    align-items: center;
}

.block__text {
    margin-bottom: 10px;
}

.block__content > * {
    flex-grow: 0;
    flex-shrink: 0;
}

.title {
    font-weight: 800;
    font-size: 44px;
    margin-bottom: 38px;
}
.icon__wrapper {
    display: block;
    border-radius: 3px;
    margin-right: 10px;

    width: 32px;
    height: 32px;
}
.icon__wrapper:last-child {
    margin-right: 0;
}

.icon__wrapper:hover {
    box-shadow: 0 0 0 1px rgba(248, 132, 13, 0.9);
}
.icon__wrapper:focus {
    box-shadow: 0 0 0 1px #30203d, 0 0 0 3px rgba(250, 242, 255),
        0 0 0 4px #30203d;
}

.iconBox {
    width: 32px;
    height: 32px;

    text-decoration: none;
    text-align: center;

    cursor: pointer;
    margin: 0;
    padding: 0;
    border: none;

    display: inline-block;
    vertical-align: top;
}

#vk {
    background: url("./assets/icons/icon_vk.svg") center;
}

#fb {
    background: url("./assets/icons/icon_facebook.svg") center;
}

#inst {
    background: url("./assets/icons/icon_instagram.svg") center;
}

#tg {
    background: url("./assets/icons/icon_telegram.svg") center;
}

#ws {
    background: url("./assets/icons/icon_whatsapp.svg") center;
}

#vb {
    background: url("./assets/icons/icon_viber.svg") center;
}

@media screen and (max-width: 1124px) {
    .block {
        margin-bottom: 16px;
        margin-left: 38px;
    }
    .title {
        font-family: Gilroy;
        font-weight: 800;
        font-style: normal;
        font-size: 36px;
        display: flex;
        justify-content: center;
    }

    .title__inner {
        width: 306px;
        text-align: center;
    }
    .footer__main {
        margin-bottom: 65px;
        margin-top: 30px;
    }
}

@media screen and (min-width: 1123px) {
    .contacts {
        display: inline-flex;
        position: relative;
        right: -19px;
    }
    .footer__main {
        text-align: center;
        margin-bottom: 110px;
        margin-top: 40px;
    }
    .block__content {
        justify-content: center;
    }
    .block {
        margin: 0 35px;
    }
}
</style>
