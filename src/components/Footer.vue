<template>
    <div class="footer__container">
        <div class="footer__main">
            <div class="left__part">
                <div class="title">
                    Свяжитесь с нами
                </div>
                <div class="socials">
                    <div class="socials__text">
                        Наши соц.сети:
                    </div>
                    <div class="socials__icons">
                        <div class="socials_icons__item">
                            <img src="./assets/icons/icon_vk.svg" alt="" />
                        </div>
                        <div class="socials_icons__item">
                            <img
                                src="./assets/icons/icon_facebook.svg"
                                alt=""
                            />
                        </div>
                        <div class="socials_icons__item">
                            <img
                                src="./assets/icons/icon_instagram.svg"
                                alt=""
                            />
                        </div>
                    </div>
                </div>
                <div class="phone__block">
                    <div class="phone__text">
                        По номеру телефона:
                    </div>
                    <div class="phone__number">
                        <div class="phone__icon">
                            <img src="./assets/icons/icon_call.svg" alt="" />
                        </div>
                        <div class="phone__digits">
                            +7 912 345-67-89
                        </div>
                    </div>
                </div>
                <div class="socials__icons">
                    <div class="socials_icons__item">
                        <img src="./assets/icons/icon_telegram.svg" alt="" />
                    </div>
                    <div class="socials_icons__item">
                        <img src="./assets/icons/icon_whatsapp.svg" alt="" />
                    </div>
                    <div class="socials_icons__item">
                        <img src="./assets/icons/icon_viber.svg" alt="" />
                    </div>
                </div>
            </div>
            <div class="right__part">
                <div class="title Docs">
                    Документы
                </div>
                <div class="link__wrapper">
                    <a class="underlined__item" href="#">Политика конфиденциальности</a>
                </div>
                <div class="link__wrapper">
                    <a class="underlined__item" href="#">Обработка персональных данных</a>
                </div>
                <div class="link__wrapper">
                    <a class="underlined__item" href="#">Договор-оферта</a>
                </div>
                <div class="company__info">
                    ООО "Онлайн-школа Virion" <br>
                    ОГРН: 54646512146512
                </div>
            </div>
        </div>
    </div>
</template>
<style>
.footer__container {
    width: 100%;
    max-width: 1001px;
    margin: 0 auto;
}

.footer__main {
    padding-top: 77px;
    padding-bottom: 77px;
    position: relative;
    display: flex;
    justify-content: space-between;

    font-weight: 500;
    color: #30203d;
}

.title {
    font-size: 18px;
    line-height: 21px;

    margin-bottom: 10px;
}
/* Left Part */
.socials {
    /* max-width: 116px; */
    margin-bottom: 10px;
}
.socials__text {
    line-height: 19px;
    margin-bottom: 7px;
}
.socials_icons__item {
    margin-right: 10px;

    /* width: 32px;
    height: 32px; */
}

.socials_icons__item:hover {
    border: 1px solid rgba(248, 132, 13, 0.9);
    border-radius: 3px;
}

.socials__icons {
    position: relative;
    display: flex;
    justify-content: space-between;
    max-width: 116px;
}

.phone__block {
    line-height: 19px;
}

.phone__number {
    position: relative;
    display: flex;
    /* align-items: center; */
    margin-top: 6px;
    margin-bottom: 6px;
}

.phone__digits {
    margin-top: 7px;
    padding-left: 3px;
}

/* Right Part */
.right__part {
    text-align: right;
}
.Docs {
    margin-bottom: 8px;
}

.link__wrapper{
    margin-bottom: 10px;
}

.underlined__item {

    /* margin-left: auto; */
    line-height: 150%;
    position: relative;
    text-decoration: none;

    color: #30203d;
    /* text-decoration: underline; */
}

.underlined__item:hover{
    color: #F8840D;
}

.underlined__item:after {
    display: block;
    bottom: 1px;
    right: 0;
    content: "";
    height: 1px;
    color: #30203d;
    width: 100%;
    background-color: #30203d;
    position: absolute;
}

.underlined__item:hover:after {
    background-color: #F8840D;
}

.company__info{
    margin-top: 26px;
    line-height: 19px;
}
</style>
