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
                        <a class="icon__wrapper" href="#">
                            <div class="iconBox" id="vk"></div>
                        </a>
                        <a class="icon__wrapper" href="#">
                            <div class="iconBox" id="fb"></div>
                        </a>
                        <a class="icon__wrapper" href="#">
                            <div class="iconBox" id="inst"></div>
                        </a>
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
                        <a class="icon__wrapper" href="#">
                            <div class="iconBox" id="tg"></div>
                        </a>
                        <a class="icon__wrapper" href="#">
                            <div class="iconBox" id="ws"></div>
                        </a>
                        <a class="icon__wrapper" href="#">
                            <div class="iconBox" id="vb"></div>
                        </a>
                    </div>
            </div>
            <div class="right__part">
                <div class="title Docs">
                    Документы
                </div>
                <div class="link__wrapper">
                    <a class="underlined__item" href="#"
                        >Политика конфиденциальности</a
                    >
                </div>
                <div class="link__wrapper">
                    <a class="underlined__item" href="#"
                        >Обработка персональных данных</a
                    >
                </div>
                <div class="link__wrapper">
                    <a class="underlined__item" href="#">Договор-оферта</a>
                </div>
                <div class="company__info">
                    ООО "Онлайн-школа Virion" <br />
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
    margin-bottom: 7px;
}
.socials__text {
    line-height: 19px;
    margin-bottom: 4px;
}

/* Иконки непосредственно */
.icon__wrapper {
    display: block;
    padding: 3px;
    border-radius: 3px;

    margin-right: 10px;
    margin-left: -1px;
    /* max-width: 34px; */
}

.icon__wrapper:hover {
    padding: 2px;
    border: rgba(248, 132, 13, 0.9) 1px solid;
}

.icon__wrapper:focus{
    padding: 0;
    border: #30203d 3px double;
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

#tg{
    background: url("./assets/icons/icon_telegram.svg") center;
}

#ws{
    background: url("./assets/icons/icon_whatsapp.svg") center;
}

#vb{
    background: url("./assets/icons/icon_viber.svg") center;
}

.socials__icon:focus {
    outline: 1px solid rgba(48, 32, 61, 0.9);
    outline-offset: 2px;
    border-radius: 3px;
}


.socials_icons__item:hover {
    padding: 0px;
    border: 1px solid rgba(248, 132, 13, 0.9);
    border-radius: 3px;
}

.socials_icons__item:focus {
    padding: 2px;
    border: 1px solid rgba(48, 32, 61, 0.9);
    border-radius: 3px;
}

.socials__icons {
    position: relative;
    display: flex;
    justify-content: space-between;
    max-width: 116px;
}

/* Phone */
.phone__block {
    line-height: 19px;
}

.phone__number {
    position: relative;
    display: flex;
    align-items: center;
    margin-top: 6px;
}

.phone__icon{
    height: 32px;
}

.phone__digits {
    /* margin-top: 7px; */
    padding-left: 3px;
}

/* Right Part */
.right__part {
    text-align: right;
}
.Docs {
    margin-bottom: 8px;
}

.link__wrapper {
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

.underlined__item:hover {
    color: #f8840d;
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
    background-color: #f8840d;
}

.company__info {
    margin-top: 26px;
    line-height: 19px;
    height: 38px;
}
</style>
