<template>
    <div class="main">
        <div class="popUp__container">
            <div class="popUp__title">{{ courseTitle }}</div>
            <div class="subtitle__label">
                О курсе:
            </div>
            <div class="popUp__description">
                {{ courseDesc }}
            </div>
            <div class="subtitle__label">
                Чему научится студент на базовом курсе:
            </div>
            <ul>
                <li>Основам языка программирования C++;</li>
                <li>
                    Базовым понятиям математического анализа, дискретной
                    математики, линейной алгебры, стандартной и аналитической
                    геометрии;
                </li>
                <li>Решению олимпиадных задач;</li>
                <li>Развитию логического и нестандартного мышления;</li>
                <li>Освоит новые математические принципы;</li>
                <li>Подготовится к ЕГЭ/ОГЭ по информатике.</li>
            </ul>
            <div class="popUp__statistics">
                <div class="popUp_stat__item" v-for="(item) in statistics" :key="item">
                    <div class="stat_item__circle">{{item.number}}</div>
                    <div class="stat_item__text">
                        {{item.text}}
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>
<script>
export default {
    data() {
        return {
            statistics: [
                {number: 512, text:"Увлекательных занятий"},
                {number: 32, text: "Академических часа"},
                {number: 231, text: "Тем для изучения"},
                {number: 520, text: "Довольных учеников"},
            ],
            courseMerits: [
                "Базовым понятиям математического анализа, дискретной математики, линейной алгебры, стандартной и аналитической геометрии;",
                "Решению олимпиадных задач;",
                "Развитию логического и нестандартного мышления;",
                "Освоит новые математические принципы;",
                "Подготовится к ЕГЭ/ОГЭ по информатике."
            ],
            courseTitle: "Курс «Олимпиадное программирование»",
            courseDesc:
                "Олимпиадное (спортивное) программирование - одна из разновидностей интеллектуальных игр, которая стоит в одном ряду с шахматами или сборкой кубика Рубика на скорость. Цель «спортсмена» — быстро и безошибочно найти решение поставленной задачи, обойдя конкурентов. За победу в подобных соревнованиях, участник получает ценные призы, приглашения на стажировки и льготы при поступлении в вузы.",
        };
    },
};
</script>
<style>
.popUp__container {
    width: 100%;
    max-width: 660px;
    margin: auto;
    background: #ffffff;
    box-shadow: 4px 4px 20px rgba(48, 32, 61, 0.1);
    border-radius: 6px;

    padding: 29px 40px 40px;

    line-height: 150%;
    font-weight: 500;
    color: #30203d;
}

.popUp__title {
    font-size: 18px;
    margin-bottom: 23px;
}

.subtitle__label {
    font-size: 18px;
    margin-bottom: 5px;
}

.popUp__description {
    font-size: 16px;
    margin-bottom: 12px;
}

.popUp__container li {
    /* background: inear-gradient(141.18deg, #4E3D95 -8.71%, #413373 104.75%);
    background: yellow; */
    margin-bottom: 4px;
}

.popUp__statistics {
    /* width: 100%; */
    /* max-width: 106px; */
    display: flex;
    position: relative;
    justify-content: space-between;
    text-align: center;
}

.stat_item__circle {
    font-size: 24px;
    color: #ffffff;
    background: linear-gradient(141.18deg, #4e3d95 -8.71%, #413373 104.75%);
    border-radius: 50%;
    padding-top: 15px;

    width: 56px;
    height: 56px;

    margin-bottom: 3px;
    margin-top: 19px;
    margin-left: auto;
    margin-right: auto;
}
</style>
