<template>
	<div class="m_intro">
		<div class="m_intro__background">
			<img src="./assets/Mobile/intro/m_intro_bg.svg" alt="" />
		</div>
			<div class="m_intro__content">
				<div class="m_intro__subtitle">
					Онлайн-школа
				</div>
				<div class="m_intro__text">
					Мы работаем, чтобы сделать образование комфортным, доступным
					и качественным.
				</div>
		</div>
	</div>
</template>
<style>

.m_intro {
	width: 100%;
	position: relative;
}
.m_intro__background img {
	width: 100%;
	object-fit: cover;
}

.m_intro__content {
	top: 0;
    right: 0;
    left: 0;
    bottom: 0;
	position: absolute;
    margin: 125px auto 0;
    text-align: center;
}

.m_intro__subtitle {
	font-weight: normal;
	font-size: 28px;
	line-height: 32px;
	color: #ffffff;
}

.m_intro__text {
    margin: 67px auto 0;
	font-weight: 500;
	font-size: 18px;
	line-height: 150%;
	color: #ffffff;
    max-width: 300px;
}
</style>
