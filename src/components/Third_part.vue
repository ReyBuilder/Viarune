<template>
	<div class="our_subjects">
		<div class="leftBg">
			<img src="./assets/images/rudiment.svg" alt="rudiment" />
		</div>
		<div class="subj__container">
			<div class="subj__title" id="desktop_about_subjs">
				Наши предметы
			</div>
			<div class="subj__filters" v-show="showFilters">
				<a class="filterWrapper" href="#">
					<div
						class="buttonBoxFilter "
						v-on:click.prevent="currentFilter = null"
					>
						Все
					</div>
				</a>
				<a
					class="filterWrapper"
					href="#"
					v-for="(item, i) in filters"
					:key="'C' + i"
					v-on:click.prevent="currentFilter = item"
				>
					<div class="buttonBoxFilter ">
						{{ item }}
					</div>
				</a>
			</div>
			<div class="subj__cards">
				<div class="subj_cards__inner">
					<div
						class="subj__card"
						v-for="item in filteredCourses"
						:key="item.id"
					>
						<div class="card__header">
							<div class="card__title">
								{{ item.title }}
							</div>
							<div
								class="card__logo"
								v-bind:style="{
									backgroundImage: 'url(' + item.img + ')',
								}"
							></div>
						</div>
						<div class="card__text">
							{{ textPreview(item.desc) }}
						</div>
						<div class="card__underground">
							<a
								class="card__button"
								href="#desktop_appointment"
								v-smooth-scroll="{
									duration: 2000,
									offset: -50,
								}"
							>
								<div class="buttonBox">
									Записаться
								</div>
							</a>
							<a
								class="card__link"
								href="#"
								v-on:click.prevent="
									$emit('click-course', index)
								"
							>
								<div>
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
export default {
	data() {
		return {
			currentFilter: null,
		};
	},
	props: {
		courses: {
			type: Array,
			required: true,
		},
		filters: {
			type: Array,
			required: true,
		},
		showFilters: {
			type: Boolean,
			required: true,
		},
	},
	computed: {
		filteredCourses() {
			if (this.currentFilter) {
				const tmp = [];
				this.courses.forEach((t) => {
					if (t.tags.some((s) => s === this.currentFilter))
						tmp.push(t);
				});
				return tmp;
			} else return this.courses;
		},
	},
	methods: {
		textPreview(text) {
			if (text.length < 82) return text;
			else {
				const tmp = text.match(/^.{0,82}\s/);
				if (!tmp || !tmp[0]) return text;
				return tmp[0].substring(0,tmp[0].length-1)+"..."
			}
		},
	},
};
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

.filterWrapper {
	border-radius: 50px;
}

.filterWrapper:focus {
	box-shadow: 0 0 0 2px #fff, 0 0 0 3px #30203d;
}

.buttonBoxFilter {
	font-family: Roboto;
	font-weight: bold;
	font-size: 14px;
	line-height: 16px;
	text-decoration: none;
	text-align: center;

	color: #4e3d95;
	background: #ffffff;

	cursor: pointer;
	margin: 0;
	border: 3px solid #4e3d95;

	display: inline-block;
	vertical-align: top;

	width: 100%;

	padding: 18px 40px 21px;
	border-radius: 50px;
}

.buttonBoxFilter:hover {
	color: #f8840d;
	border: 3px solid #f8840d;
}

.buttonBoxFilter:active {
	color: #ffffff;
	background: linear-gradient(97.42deg, #fb7a0d 0.1%, #fbae0d 115.11%);
}
/* Cards Containers */
.subj__cards {
	padding-top: 40px;
}
.subj_cards__inner {
	display: flex;
	position: relative;
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

.subj__card:nth-child(3n-1) {
	margin: 0 20px 20px;
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

.card__logo {
	width: 80px;
	height: 80px;
	border-radius: 50%;
	border: 3px solid #4e3d95;

	background-repeat: no-repeat;
	background-position: center center;
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

.card__button {
	border-radius: 40px;
}

.card__button:focus {
	box-shadow: 0 0 0 2px #fff, 0 0 0 3px #070707;
}

.buttonBox {
	padding: 18px 36px;
	border-radius: 40px;
	background: linear-gradient(141.18deg, #4e3d95 -8.71%, #413373 104.75%);
}

.buttonBox:hover {
	background: linear-gradient(97.42deg, #fb7a0d 0.1%, #fbae0d 115.11%);
	box-shadow: 1px 4px 15px rgba(248, 132, 13, 0.55);
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

	color: #f8840d;
}

.card__link:focus {
	box-shadow: 0 0 0 1px #30203d;
}
</style>
