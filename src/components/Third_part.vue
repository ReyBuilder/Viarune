<template>
    <div class="our_subjects">
      <div class="leftBg">
        <img src="./assets/images/rudiment.svg" alt="" />
      </div>
      <div class="subj__container">
        <div class="subj__title">
          Наши предметы
        </div>
        <div class="subj__filters" v-if="showFilters">
          <a class="buttonWrapper" href="#">
            <div class="buttonBoxFilter buttonFilter">
              Все
            </div>
          </a>
          <a class="buttonWrapper" href="#">
            <div class="buttonBoxFilter buttonFilter">
              Программирование
            </div>
          </a>
          <a class="buttonWrapper" href="#">
            <div class="buttonBoxFilter buttonFilter">
              Дизайн
            </div>
          </a>
          <a class="buttonWrapper" href="#">
            <div class="buttonBoxFilter buttonFilter">
              Иностранные языки
            </div>
          </a>
          <a class="buttonWrapper" href="#">
            <div class="buttonBoxFilter buttonFilter">
              Школьные предметы
            </div>
          </a>
        </div>
        <div class="subj__cards">
          <div class="subj_cards__inner" >
            <div class="subj__card" v-for="(item) in courses" :key="item">
              <div class="card__header">
                <div class="card__title">
                  {{item.title}}
                </div>
                <div class="card__logo" v-bind:style='{ backgroundImage: "url(" + item.img + ") center no-repeat", }'>
                </div>
              </div>
              <div class="card__text">
                {{item.desc}}
              </div>
              <div class="card__underground">
                <a class="buttonWrapper" href="#">
                  <div class="buttonBox buttonPurple">
                    Записаться
                  </div>
                </a>
                <a class="card__link" href="#">
                  <div class="">
                    Подробнее
                  </div>
                </a>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
</template>

<script>
export default ({
  data(){
    return{
      showFilters: true,
      courses: [
        {  name: "Python", title:"Язык программирования: Python", img: "./assets/images/subj_cards/python-logo.svg", desc: "Научим вас и вашего ребенка кодить на высокоуровневом языке программирования. Без слез..." },
        {  name: "Scratch", title: "Язык программирования: Scratch",img: "", desc: "Детский язык программирования, похожий на конструктор Lego: программы собираются..." },
        {  name: "C++", title:"Спортивное программирование на C++", img: "", desc: "Хотите стать победителем российской олимпиады по программированию?" },
        {  name: "Web", title:"Web", img: "", desc: "Что скрывается за красивой оболочкой сайта? Язык гипертекстовой разметки HTML..." },
        {  name: "Informatics", title:"Элементарная информатика (взрослые)", img: "", desc: "Для тех, у кого нет времени на обучение. Изучайте только актуальную для вас тему: эксель..." },
        {  name: "Figma", title:"Figma", img: "", desc: "Вы познакомитесь с миром веб-дизайна, освоите популярный графический редактор Figma." },
        ],
    }
  }
})
</script>

<style scoped>
/* Our Subjects */
.our_subjects {
  padding-top: 250px;
  padding-bottom: 171px;
  position: relative;
}

.leftBg {
  position: absolute;
  top: -210px;
  z-index: -1;
}
.subj__container {
  width: 100%;
  max-width: 1000px;
  margin: 0 auto;
}

.subj__title {
  text-align: center;
  font-weight: 800;
  font-size: 44px;
  line-height: 54px;

  color: #30203d;

  margin-bottom: 39px;
}

/* Filters */
.subj__filters {
  display: flex;
  justify-content: space-between;
}

.buttonBoxFilter {
  font-family: Roboto;
  font-weight: bold;
  font-size: 14px;
  line-height: 16px;
  text-align: center;
  color: #4e3d95;
  text-decoration: none;
  text-align: center;

  cursor: pointer;
  margin: 0;
  padding: 0;
  border-radius: 50px;
  border: 3px solid #4e3d95;

  display: inline-block;
  vertical-align: top;

  width: 100%;

  padding: 18px 40px 21px;
  border-radius: 50px;
}

.buttonWrapper {
  border-radius: 50px;
}
/* Cards Containers */
.subj__cards {
  padding-top: 40px;
  padding-bottom: 75px;
}
.subj_cards__inner {
  display: flex;
  position: relative;
  justify-content: space-between;
  flex-wrap: wrap;
}
/* Card */
.subj__card {
  flex: 30%;
  max-width: 320px;
  background: #ffffff;
  box-shadow: 4px 4px 20px rgba(48, 32, 61, 0.1);
  border-radius: 6px;
  padding: 20px 20px 30px;
  margin-bottom: 20px;
}

.card__header {
  position: relative;
  display: flex;
  justify-content: space-between;
  margin-bottom: 20px;
}

.card__title {
  font-weight: 500;
  font-size: 16px;
  line-height: 150%;

  padding-top: 10px;
  max-width: 175px;
  text-align: left;

  color: #30203d;
}

.card__logo{
  width: 80px;
  height: 80px;
  border-radius: 50%;
  border: 3px solid #4E3D95;

  /* background: url("./assets/images/subj_cards/python-logo.svg") center no-repeat; */
}
.card__text {
  font-weight: normal;
  font-size: 16px;
  line-height: 150%;

  color: #30203d;

  margin-bottom: 20px;
}

.card__underground {
  display: flex;
  justify-content: space-between;
  align-items: center;

  bottom: 0;
}

.card__link {
  font-weight: 500;
  font-size: 16px;
  line-height: 19px;
  padding: 4px 10px 7px;
  
  color: #30203d;

  border-radius: 30px;
}

.card__link:hover {
  font-weight: 500;
  font-size: 16px;
  line-height: 19px;

  color: #F8840D;
}

.card__link:focus{
  box-shadow: 0 0 0 1px #30203D;
}
.buttonBox {
  padding: 18px 36px;
  border-radius: 40px;
}
</style>
