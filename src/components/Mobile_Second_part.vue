<template>
	<div class="m_about__school">
		<div class="m_about_school__title">
			О школе
		</div>
		<div class="about_school__infoblock">
			<div class="infoblock__item">
				<div class="infoblock_item__ico">
					<img
						src="./assets/images/about_school/1.svg"
						alt="about_school/1"
					/>
				</div>
				<div class="infoblock_item__text">
					Качество уроков всегда на высшем уровне, поскольку каждый
					урок отсматривается и анализируется;
				</div>
			</div>
			<div class="infoblock__item">
				<div class="infoblock_item__ico">
					<img
						src="./assets/images/about_school/2.svg"
						alt="about_school/2"
					/>
				</div>
				<div class="infoblock_item__text">
					Удобная и понятная система для управления <br />
					вашими уроками;
				</div>
			</div>
			<div class="infoblock__item">
				<div class="infoblock_item__ico">
					<img
						src="./assets/images/about_school/3.svg"
						alt="about_school/3."
					/>
				</div>
				<div class="infoblock_item__text">
					Ответы на любые вопросы можно узнать в чате <br />
					с преподавателем;
				</div>
			</div>
			<div class="infoblock__item">
				<div class="infoblock_item__ico">
					<img
						src="./assets/images/about_school/4.svg"
						alt="about_school/4"
					/>
				</div>
				<div class="infoblock_item__text">
					Занятие с опытным преподавателем.
				</div>
			</div>
			<a
				class="button"
				href="#"
				v-smooth-scroll="{ duration: 2000, offset: -50 }"
			>
				Перейти к предметам
			</a>
		</div>
	</div>
</template>
<style scoped>
.m_about_school__title {
	text-align: center;
	margin: 58px auto 38px;
	font-weight: 800;
	font-size: 44px;
	line-height: 54px;

	color: #30203d;
}
.about_school__infoblock {
	width: 100%;

	background: #ffffff;

	box-shadow: 4px 4px 20px rgba(48, 32, 61, 0.1);
	border-radius: 6px;

	margin: 0 auto;
	padding: 33px 37px 30px 39px;
}

.infoblock__item {
	display: flex;
	position: relative;
	align-items: center;
	margin-bottom: 10px;
}

.infoblock_item__text {
	margin-left: 20px;

	font-weight: normal;
	font-size: 16px;
	line-height: 150%;

	color: #30203d;
}

.button {
	padding-top: 18px;
    padding-bottom: 18px;
	text-decoration: none;
	text-align: center;
	display: block;

	background: linear-gradient(97.42deg, #fb7a0d 0.1%, #fbae0d 115.11%);
	box-shadow: 1px 4px 15px rgba(248, 132, 13, 0.55);
	border-radius: 40px;

	font-weight: bold;
	font-size: 16px;
	line-height: 19px;

	color: #ffffff;
}
</style>
