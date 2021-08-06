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
          <div class="subj_cards__inner">
            <template v-for="(item) in "> 
            <div class="subj__card" >
              <div class="card__header">
                <div class="card__title">
                  Язык программирования: Python
                </div>
                <div class="card__logo">
                  <img
                    src="./assets/images/subj_cards/python-logo2.svg"
                    alt=""
                  />
                </div>
              </div>
              <div class="card__text">
                Научим вас и вашего ребенка кодить на высокоуровневом языке
                программирования. Без слез...
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
            </template> 
          </div>
        </div>
      </div>
    </div>
</template>

<script>
export default ({
  data(){
    return{
      showFilters: false,
      courses: [
        {  name: "Python", title:"Язык программирования: Python",img: "http://example.com/", desc: "Научим вас и вашего ребенка кодить на высокоуровневом языке программирования. Без слез..." },
        { name: "Scratch", title: "Язык программирования: Scratch",img: "http://example.com/", desc: "Детский язык программирования, похожий на конструктор Lego: программы собираются..." },
        {  name: "C++", title:"Спортивное программирование на C++", img: "http://example.com/", desc: "Хотите стать победителем российской олимпиады по программированию?" },
        {  name: "Web", title:"Web", img: "http://example.com/", desc: "Что скрывается за красивой оболочкой сайта? Язык гипертекстовой разметки HTML..." },
        { name: "Informatics", title:"Элементарная информатика (взрослые)", img: "http://example.com/", desc: "Для тех, у кого нет времени на обучение. Изучайте только актуальную для вас тему: эксель..." },
        {  name: "Figma", title:"Figma", img: "http://example.com/", desc: "Вы познакомитесь с миром веб-дизайна, освоите популярный графический редактор Figma." },
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

.card__text {
  font-weight: normal;
  font-size: 16px;
  line-height: 150%;

  color: #30203d;

  margin-bottom: 20px;
}

.card__underground {
  display: flex;
  position: relative;
  justify-content: space-between;
  align-items: center;
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
