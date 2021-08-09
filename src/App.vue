<template>
	<div>
		<div class="desktop_type">
			<Intro></Intro>
			<About_school></About_school>
			<About_subj
				v-bind:courses="courses"
				v-on:click-course="currentCourseIndex = $event"
				v-bind:filters="filters"
				v-bind:showFilters="showFilters"
			></About_subj>
			<Appointment></Appointment>
			<Footer></Footer>
			<PopUp
				v-bind:course="coursePopUp"
				v-on:close-popup="currentCourseIndex = null"
			></PopUp>
		</div>
		<div class="mobile_type">
			<MobileIntro></MobileIntro>
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
import MobileIntro from "./components/Mobile_Intro.vue"

export default {
	name: "App",
	computed: {
		coursePopUp() {
			return this.courses[this.currentCourseIndex];
		},
	},
	data() {
		return {
			isMobile: false,
			showFilters: true,
			currentCourseIndex: null,
			filters: [
				"Программирование",
				"Дизайн",
				"Иностранные языки",
				"Школьные предметы",
			],
			courses: [
				{
					name: "Python",
					title: "Язык программирования: Python",
					img: "./courses_logos/logo_python.svg",
					desc:
						"Научим вас и вашего ребенка кодить на высокоуровневом языке программирования. Без слез...",
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
					tags: ["Программирование", "Школьные предметы"],
				},
				{
					name: "Scratch",
					title: "Язык программирования: Scratch",
					img: "./courses_logos/logo_scratch.svg",
					desc:
						"Детский язык программирования, похожий на конструктор Lego: программы собираются...",
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
						"Для тех, у кого нет времени на обучение. Изучайте только актуальную для вас тему: эксель...",
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
	.desktop_type{
		display: none;
	}
}
@media screen and (min-width: 1123px) {
	.mobile_type {
		display: none;
	}
	.desktop_type{
		display: block;
	}
}

</style>
