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
				<div class="phone__block">
					<div class="phone__text">
						По номеру телефона:
					</div>
					<div class="phone__number">
						<div class="phone__icon">
							<img src="./assets/icons/icon_call.svg" alt="" />
						</div>
						<div class="phone__digits">
							+7 912 013 39-97
						</div>
					</div>
				</div>
				<div class="socials__icons">
					<a class="icon__wrapper" href="#">
						<div class="iconBox" id="tg"></div>
					</a>
					<a class="icon__wrapper" href="https://wa.me/79120133997">
						<div class="iconBox" id="ws"></div>
					</a>
					<a class="icon__wrapper" href="#">
						<div class="iconBox" id="vb"></div>
					</a>
				</div>
			</div>
			<div class="center__part">
				<div class="title Docs">
					Документы
				</div>
				<div class="link__wrapper">
					<a class="underlined__item" href="./Dogovor-oferta.docx"
						>Договор-оферта</a
					>
				</div>
			</div>
			<div class="right__part">
				<div class="title Information">
					Информация
				</div>
				<div class="company_info">
					ИП "Семакин Александр Александрович"
				</div>
				<div class="company_info">ОГРН 321183200030713</div>
				<div class="company_info">ИНН 182907717333</div>
			</div>
		</div>
	</div>
</template>
<style scoped>
@media screen and (max-width:344px) {
	.footer__container {
		margin-left: 28px;
		margin-right: 25px;
	}
	.footer__main {
		justify-content: flex-start;
		padding-bottom: 22px;
	}
	.center__part {
		margin: 0;
	}
}
@media screen and (min-width: 345px) {
	.footer__container {
		margin-left: 28px;
		margin-right: 25px;
	}
	.footer__main {
		justify-content: flex-start;
	}
	.center__part, .left__part {
		margin-right: 20px;
	}
}

@media screen and (min-width: 1123px) {
	.footer__container {
		width: 100%;
		max-width: 1001px;
		margin: 0 auto;
	}
	.right__part {
		margin-top: 0;
	}
	.footer__main {
		justify-content: space-between;
		padding-bottom: 54px;
	}
}
.footer__main {
	padding-top: 77px;
	position: relative;
	display: flex;

	font-weight: 500;
	color: #30203d;
	flex-wrap: wrap;
}

.title {
	font-size: 18px;
	line-height: 21px;

	margin-bottom: 10px;
}
/* Left Part */
.left__part {
	margin-bottom: 30px;
}
.socials {
	margin-bottom: 10px;
}
.socials__text {
	line-height: 19px;
	margin-bottom: 7px;
}

/* Иконки непосредственно */
.icon__wrapper {
	display: block;
	border-radius: 3px;
	margin-right: 10px;

	width: 32px;
	height: 32px;
}

.icon__wrapper:hover {
	box-shadow: 0 0 0 1px rgba(248, 132, 13, 0.9);
}

.icon__wrapper:focus {
	/* padding: 0; */
	/* border: #30203d 1px solid; */
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
	margin-bottom: 10px;
}

.phone__number {
	position: relative;
	display: flex;
	align-items: center;
	margin-top: 6px;
}

.phone__icon {
	height: 32px;
}

.phone__digits {
	padding-left: 3px;
}

/* Center Part */
.center__part{
    margin-bottom: 30px;
}

.Docs {
	margin-bottom: 8px;
}

.link__wrapper {
	margin-bottom: 10px;
}

.underlined__item {
	line-height: 150%;
	position: relative;
	text-decoration: none;

	color: #30203d;
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

/* Right Part */
.right__part {
	text-align: left;
}

.Information {
	margin-bottom: 7px;
}

.company_info {
	font-size: 16px;
	line-height: 150%;
	color: #30203d;
	margin-bottom: 10px;
}
</style>
