<template>
	<div class="m_intro">
		<div class="m_intro__background">
			<img src="./assets/Mobile/intro/m_intro_bg.svg" alt="m_intro_bg" />
		</div>
		<div class="container">
			<div class="m_intro__content">
				<div class="m_intro__logo">
					<img
						src="./assets/Mobile/intro/m_intro_logo.svg"
						alt="m_intro_logo"
					/>
				</div>
				<div class="m_intro__subtitle">
					Онлайн-школа
				</div>
				<div class="m_intro__title">
					<img
						src="./assets/Mobile/intro/m_intro_title.svg"
						alt="m_intro_title"
					/>
				</div>
				<div class="m_intro__text">
					Мы работаем, чтобы сделать образование комфортным, доступным
					и качественным.
				</div>
				<a class="intro__button" href="#">
					Подобрать курс
				</a>
			</div>
		</div>
	</div>
</template>
<style scoped>
.m_intro {
	width: 100%;
	position: relative;
}
.m_intro__background img {
	width: 100%;
	object-fit: cover;
}

.container {
	width: 100%;
	top: 0;
	right: 0;
	left: 0;
	bottom: 0;
	position: absolute;
}

.m_intro__content {
	/* margin-top: 125px; */
	margin: 0 auto;
	text-align: center;
	width: 100%;
	max-width: 300px;
}

.m_intro__logo {
	margin-top: 33px;
}
.m_intro__subtitle {
	font-weight: normal;
	font-size: 28px;
	line-height: 32px;
	color: #ffffff;
	margin-top: 52px;
}

.m_intro__text {
	margin-top: 7px;
	margin-bottom: 52px;
	font-weight: 500;
	font-size: 18px;
	line-height: 150%;
	color: #ffffff;
	/* max-width: 300px; */
}

.intro__button {
	display: block;
	width: 100%;
	text-decoration: none;

	font-weight: bold;
	font-size: 16px;
	line-height: 19px;

	color: #ffffff;

	padding-top: 18px;
	padding-bottom: 18px;

	background: linear-gradient(97.42deg, #fb7a0d 0.1%, #fbae0d 115.11%);
	box-shadow: 1px 4px 15px rgba(248, 132, 13, 0.35);
	border-radius: 40px;
}
</style>
