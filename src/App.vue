<template>
	<div>
		<div class="desktop_type">
			<Intro></Intro>
			<About_school></About_school>
			<About_subj
				v-bind:courses="courses"
				v-on:click-course="clickCourse"
				v-bind:filters="filters"
				v-bind:showFilters="showFilters"
			></About_subj>
			<Appointment
			></Appointment>
			<Footer></Footer>
			<PopUp
				v-bind:course="coursePopUp"
				v-on:close-popup="closePopup"
			></PopUp>
		</div>
		<div class="mobile_type">
			<MobileIntro></MobileIntro>
			<Mobile_about_school></Mobile_about_school>
			<Mobile_about_subj
				v-bind:courses="courses"
				v-on:click-course="clickCourse"
				v-bind:filters="filters"
				v-bind:showFilters="showFilters"
			></Mobile_about_subj>
			<Mobile_appointment
			></Mobile_appointment>
			<Footer></Footer>
			<Mobile_PopUp
				v-bind:course="coursePopUp"
				v-on:close-popup="closePopup"
			></Mobile_PopUp>
		</div>
	</div>
</template>
<script>
import Intro from "./components/Intro.vue";
import About_school from "./components/Second_part.vue";
import About_subj from "./components/Third_part.vue";
import Appointment from "./components/Fourth_part.vue";
import Footer from "./components/Footer.vue";
import PopUp from "./components/Pop_Up.vue";
import MobileIntro from "./components/Mobile_Intro.vue";
import Mobile_about_school from "./components/Mobile_Second_part.vue";
import Mobile_about_subj from "./components/Mobile_Third_part.vue";
import Mobile_appointment from "./components/Mobile_Fourth_part.vue";
import Mobile_PopUp from "./components/Mobile_PopUp.vue";

export default {
	name: "App",
	methods: {
		clickCourse(event) {
			this.currentCourseIndex = event;
			document.body.classList.add("block_scroll");
		},
		closePopup() {
			this.currentCourseIndex = null;
			document.body.classList.remove("block_scroll");
		},
	},
	computed: {
		coursePopUp() {
			return this.courses[this.currentCourseIndex];
		},
	},
	data() {
		return {
			filters: [
				"Программирование",
				"Дизайн",
				"Иностранные языки",
				"Школьные предметы",
			],
			courses: [
				{
					name: "Scratch",
					title: "Язык программирования: Scratch",
					img: "./courses_logos/logo_scratch.svg",
					desc:
						"Детский язык программирования, похожий на конструктор Lego: программы собираются",
					merits: [
						"Базовым понятиям математического анализа, дискретной математики, линейной алгебры, стандартной и аналитической геометрии;",
						"Решению олимпиадных задач;",
						"Развитию логического и нестандартного мышления;",
						"Освоит новые математические принципы;",
						"Подготовится к ЕГЭ/ОГЭ по информатике.",
					],
					statistics: [
						{ number: 512, text: "Увлекательных занятий" },
						{ number: 32, text: "Академических часа" },
						{ number: 231, text: "Тем для изучения" },
						{ number: 520, text: "Довольных учеников" },
					],
					tags: ["Школьные предметы", "Программирование"],
				},
				{
					name: "C++",
					title: "Спортивное программирование на C++",
					img: "./courses_logos/logo_c++.svg",
					desc:
						"Хотите стать победителем российской олимпиады по программированию?",
					merits: [
						"Базовым понятиям математического анализа, дискретной математики, линейной алгебры, стандартной и аналитической геометрии;",
						"Решению олимпиадных задач;",
						"Развитию логического и нестандартного мышления;",
						"Освоит новые математические принципы;",
						"Подготовится к ЕГЭ/ОГЭ по информатике.",
					],
					statistics: [
						{ number: 512, text: "Увлекательных занятий" },
						{ number: 32, text: "Академических часа" },
						{ number: 231, text: "Тем для изучения" },
						{ number: 520, text: "Довольных учеников" },
					],
					tags: ["Программирование"],
				},
				{
					name: "Informatics",
					title: "Элементарная информатика (дети)",
					img: "./courses_logos/logo_informatics.svg",
					desc:
						"Для тех, у кого нет времени на обучение. Изучайте только актуальную для вас тему: эксель",
					merits: [
						"Базовым понятиям математического анализа, дискретной математики, линейной алгебры, стандартной и аналитической геометрии;",
						"Решению олимпиадных задач;",
						"Развитию логического и нестандартного мышления;",
						"Освоит новые математические принципы;",
						"Подготовится к ЕГЭ/ОГЭ по информатике.",
					],
					statistics: [
						{ number: 512, text: "Увлекательных занятий" },
						{ number: 32, text: "Академических часа" },
						{ number: 231, text: "Тем для изучения" },
						{ number: 520, text: "Довольных учеников" },
					],
					tags: ["Школьные предметы"],
				},
				{
					name: "Figma",
					title: "Figma",
					img: "./courses_logos/logo_figma.svg",
					desc:
						"Вы познакомитесь с миром веб-дизайна, освоите популярный графический редактор Figma.",
					merits: [
						"Базовым понятиям математического анализа, дискретной математики, линейной алгебры, стандартной и аналитической геометрии;",
						"Решению олимпиадных задач;",
						"Развитию логического и нестандартного мышления;",
						"Освоит новые математические принципы;",
						"Подготовится к ЕГЭ/ОГЭ по информатике.",
					],
					statistics: [
						{ number: 512, text: "Увлекательных занятий" },
						{ number: 32, text: "Академических часа" },
						{ number: 231, text: "Тем для изучения" },
						{ number: 520, text: "Довольных учеников" },
					],
					tags: ["Дизайн"],
				},
			],
		};
	},
	components: {
		Intro,
		About_school,
		About_subj,
		Appointment,
		Footer,
		PopUp,
		MobileIntro,
		Mobile_about_school,
		Mobile_about_subj,
		Mobile_appointment,
		Mobile_PopUp,
	},
	created() {
		document.title = "Viarune study";
	},
};
</script>
<style>
@import url(~@/assets/fonts/fonts.css);
@import url(~@/assets/BaseStyles.css);
@media screen and (max-width: 1124px) {
	.mobile_type {
		display: block;
	}
	.desktop_type {
		display: none;
	}
}
@media screen and (min-width: 1123px) {
	.mobile_type {
		display: none;
	}
	.desktop_type {
		display: block;
	}
}
.block_scroll {
	overflow: hidden;
}
</style>
