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
            <Appointment v-on:validate="validationPopupShow"></Appointment>
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
                v-on:validate="validationPopupShow"
            ></Mobile_appointment>
            <Footer></Footer>
            <Mobile_PopUp
                v-bind:course="coursePopUp"
                v-on:close-popup="closePopup"
            ></Mobile_PopUp>
        </div>
        <ValidationPopup
            v-bind:active="isValidationPopupActive"
            v-on:close="validationPopupClose"
        ></ValidationPopup>
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
import ValidationPopup from "./components/ValidationPopup.vue";

export default {
    name: "App",
    beforeCreate() {
        var inner = document.createElement("div");
        inner.style.width = "100%";
        inner.style.height = "1px";

        var outer = document.createElement("div");
        outer.style.position = "absolute";
        outer.style.top = "0px";
        outer.style.left = "-100%";
        outer.style.width = "100%";
        outer.style.height = "2px";
        outer.style.overflow = "hidden";
        outer.appendChild(inner);

        document.body.appendChild(outer);
        var w1 = inner.offsetWidth;
        outer.style.overflow = "scroll";
        var w2 = inner.offsetWidth;
        if (w1 == w2) w2 = outer.clientWidth;

        document.body.removeChild(outer);

        this.$scrollSize = w1 - w2;
    },
    methods: {
        clickCourse(event) {
            this.currentCourseIndex = event;
            document.body.classList.add("block_scroll");
			document.body.style.paddingRight = this.$scrollSize + 'px';
        },
        closePopup() {
            this.currentCourseIndex = null;
            document.body.classList.remove("block_scroll");
			document.body.style.paddingRight = '0';
        },
        validationPopupShow() {
            this.isValidationPopupActive = true;
            document.body.classList.add("block_scroll");
			document.body.style.paddingRight = this.$scrollSize + 'px';
        },
        validationPopupClose() {
            this.isValidationPopupActive = false;
            document.body.classList.remove("block_scroll");
			document.body.style.paddingRight = '0';
        },
    },
    computed: {
        coursePopUp() {
            return this.courses[this.currentCourseIndex];
        },
    },
    data() {
        return {
            isValidationPopupActive: false,
            showFilters: false,
            currentCourseIndex: null,
            filters: [
                "Программирование",
                "Дизайн",
                "Иностранные языки",
                "Школьные предметы",
            ],
            courses: [
                {
                    name: "C++",
                    title: "Спортивное программирование на C++",
                    img: "./courses_logos/logo_c++.svg",
                    desc: "Хотите стать победителем российской олимпиады по программированию?",
                    merits: [
                        "Базовым понятиям математического анализа, дискретной математики, линейной алгебры, стандартной и аналитической геометрии;",
                        "Решать олимпиадных задач;",
                        "Развитию логического и нестандартного мышления;",
                        "Освоит новые математические принципы;",
                        "Подготовится к ЕГЭ/ОГЭ по информатике.",
                    ],
                    statistics: [
                        { number: 55, text: "минут - одно занятие" },
                        { number: 260, text: "Тем для изучения" },
                        { number: 777, text: "Довольных учеников" },
                    ],
                    tags: ["Программирование"],
                },
                {
                    name: "EGEMath",
                    title: "ЕГЭ математика",
                    img: "./courses_logos/logo_math.svg",
                    desc: "Опытный педагог поможет подготовится к единому государственному экзамену (ЕГЭ) по математике",
                    merits: [
                        "Быстро Рещать тестовые задания;",
                        "Решать геометрические задачи;",
                        "Решать задания с параметром;",
                        "Решать олимпиадные задания;",
                        "Решать тригонометрические уравнения, неравенства и задания с параметром.",
                    ],
                    statistics: [
                        { number: 55, text: "минут - одно занятие" },
                        { number: 20, text: "Тем для изучения" },
                        { number: 77, text: "Довольных учеников" },
                    ],
                    tags: ["Школьные предметы", "Программирование"],
                },
                {
                    name: "OGEmath",
                    title: "ОГЭ математика",
                    img: "./courses_logos/logo_math.svg",
                    desc: "Опытный педагог поможет подготовится к общему государственному экзамену (ОГЭ) по математике",
                    merits: [
                        "Решать текстовые задачи;",
                        "Решать геометрические задачи;",
                        "Решать неравенства и уравнения;",
                        "Решать системы уравнений;",
                        "Строить и читать графики функций.",
                    ],
                    statistics: [
                        { number: 55, text: "минут - одно занятие" },
                        { number: 25, text: "Тем для изучения" },
                        { number: 67, text: "Довольных учеников" },
                    ],
                    tags: ["Школьные предметы", "Программирование"],
                },
                {
                    name: "EGEinf",
                    title: "ЕГЭ информатика",
                    img: "./courses_logos/logo_informatics.svg",
                    desc: "Опытный педагог поможет подготовится к единому государственному экзамену (ЕГЭ) по информатике",
                    merits: [
                        "Быстро Выполнять тестовые задания;",
                        "Изучит язык программирования C++;",
                        "Научитьсярешать решать задачи с помощью программирования;",
                        "Решать задания повышенного уровня;",
                        "Работать в текстовых редакторах и программ предназначенных для работы с таблицами.",
                    ],
                    statistics: [
                        { number: 55, text: "минут - одно занятие" },
                        { number: 27, text: "Тем для изучения" },
                        { number: 102, text: "Довольных учеников" },
                    ],
                    tags: ["Школьные предметы"],
                },
                {
                    name: "OGEinf",
                    title: "ОГЭ информатика",
                    img: "./courses_logos/logo_informatics.svg",
                    desc: "Опытный педагог поможет подготовится к общему государственному экзамену (ОГЭ) по информатике",
                    merits: [
                        "Быстро Выполнять тестовые задания;",
                        "Изучит язык программирования Python;",
                        "Научитьсярешать решать задачи с помощью программирования;",
                        "Базовым понятиям информатики",
                        "Работать в текстовых редакторах и программ предназначенных для работы с таблицами.",
                    ],
                    statistics: [
                        { number: 55, text: "минут - одно занятие" },
                        { number: 17, text: "Тем для изучения" },
                        { number: 92, text: "Довольных учеников" },
                    ],
                    tags: ["Школьные предметы"],
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
        ValidationPopup,
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
