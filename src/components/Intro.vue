<template>
	<div>
		<header class="header">
			<div class="header__inner">
				<nav class="nav">
					<div class="nav__item">
						<img
							src="./assets/images/intro/Header_logo.svg"
							alt="Logo"
						/>
					</div>
					<a class="nav__item" href="#desktop_about_school" v-smooth-scroll="{ duration: 2000, offset: -50 }">О школе</a>
					<a class="nav__item" href="#desktop_about_subjs" v-smooth-scroll="{ duration: 2000, offset: -50 }">Предметы</a>
					<a class="nav__item" href="#desktop_appointment" v-smooth-scroll="{ duration: 2000, offset: -50 }">Пробный урок</a>
					<a class="nav__phone" href="tel:+79199118950">
						<div class="nav_phone__icon">
							<!-- <img src="./assets/icons/icon_intro_call.svg" alt="" /> -->
						</div>
						<div class="nav_phone__number underlined">
							+7 919 911-89-50
						</div>
					</a>
				</nav>
			</div>
		</header>
		<div class="intro">
			<div class="intro__background">
				<img src="./assets/images/intro/Intro_bg.svg" alt="" />
			</div>
			<div class="container">
				<div class="intro__content">
					<div class="intro-content__inner">
						<div class="intro-content__state">
							<div class="intro__subtitle">Онлайн-школа</div>
							<div class="intro__title">Viarune study</div>
							<div class="intro__text">
								Мы работаем чтобы сделать образование
								комфортным, доступным и качественным.
							</div>
							<a class="buttonWrapper" href="#desktop_about_subjs" v-smooth-scroll="{ duration: 2000, offset: -50 }">
								<div class="buttonBox buttonOrange">
									Подобрать курс
								</div>
							</a>
						</div>
					</div>
				</div>
			</div>
		</div>
	</div>
</template>

<style scoped>
/* Button radius&paddings */
.buttonBox {
	padding: 18px 63px;
	border-radius: 40px;
}
.buttonWrapper {
	max-width: 256px;
	border-radius: 40px;
}

/*Intro*/
.intro {
	width: 100%;
	position: relative;
}

.intro__background img {
	width: 100%;
	object-fit: cover;
}

.intro__content {
	top: 0;
	position: absolute;
	margin-top: 20%;
}

.intro-content__inner {
	display: flex;
	align-items: center;
}
.intro-content__state {
	font-family: Gilroy;
	font-style: normal;
	color: #fff;
	width: 100%;
	max-width: 460px;
}

.intro__subtitle {
	font-weight: normal;
	font-size: 28px;
	line-height: 32px;
}

.intro__title {
	font-weight: 800;
	font-size: 54px;
	line-height: 66px;
	margin-bottom: 5px;
}

.intro__text {
	font-weight: 500;
	font-size: 18px;
	line-height: 150%;
	margin-bottom: 34px;
}

/*Header*/
.header {
	top: 0;
	left: 0;
	right: 0;
	position: absolute;
	z-index: 1000;
	width: 100%;
}

/*Nav*/
.nav {
	font-weight: 500;
	line-height: 20px;
	padding-top: 40px;
	display: flex;
	justify-content: space-between;
	align-items: center;
	width: 100%;
	max-width: 1100px;
	margin-left: auto;
	margin-right: auto;
}

.nav__item {
	color: #eee;
	text-decoration: none;
	font-style: normal;
	font-weight: 500;
	line-height: 19px;

	display: inline-block;
	vertical-align: top;

	position: relative;

	border-radius: 30px;
	padding: 4px 10px 7px;
}

.nav__item:hover {
	color: #f8840d;
}

.nav__item:active {
	text-decoration: underline;
}

.nav__item:after {
	display: block;
	content: "";
	opacity: 0;
	/* width: 79%; */
	height: 1px;
	font-weight: 500;
	color: #f8840d;
	background-color: #f8840d;
	position: absolute;
	top: 20px;
}

.nav__item:active:after {
	opacity: 1;
}

.nav__item:focus {
	box-shadow: 0 0 0 1px #fff;
}

.nav__phone {
	display: flex;
	align-items: center;
	font-weight: 500;
	line-height: 19px;
	border-radius: 30px;

	padding-right: 12px;
	padding-left: 12px;
	margin-right: -12px;
	margin-left: -12px;
	text-decoration: none;
}
.nav_phone__icon {
	height: 28px;
	width: 28px;
	background: url("./assets/icons/icon_intro_call.svg") center no-repeat;
}
.nav__phone:hover .nav_phone__icon {
	background: url("./assets/icons/icon_intro_call_active.svg") center
		no-repeat;
}
.nav__phone:focus {
	box-shadow: 0 0 0 1px #fff;
}

.nav_phone__number {
	padding-bottom: 4px;
}

/*Container*/
.container {
	width: 100%;
	margin: 0 auto;
	max-width: 1100px;
}

/* underlined */
.underlined {
	position: relative;
	color: #eee;
}

.nav__phone:hover .underlined {
	position: relative;
	color: #f8840d;
	cursor: pointer;
}
.underlined:after {
	display: block;
	content: "";
	width: 100%;
	height: 1px;
	background-color: #eee;
	position: absolute;
	top: 18px;
	opacity: 1;
}
.nav__phone:hover .underlined:after {
	background-color: #f8840d;
}
</style>
