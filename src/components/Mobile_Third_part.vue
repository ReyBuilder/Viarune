<template>
	<div class="about_subj">
		<div class="title" id="mobile_about_subjs">
			Наши предметы
		</div>
		<div class="m_subj__filters" v-show="showFilters">
			<a
				class="button__filter"
				v-on:click.prevent="currentFilter = null"
				href="#"
			>
				Все
			</a>
			<a
				class="button__filter"
				href="#"
				v-for="(item, index) in filters"
				:key="'A' + index"
				v-on:click.prevent="currentFilter = item"
			>
				{{ item }}
			</a>
		</div>
		<div class="subj__cards">
			<div class="subj_cards__inner">
				<div
					class="subj__card"
					v-for="(item, index) in showedCourses"
					:key="'B' + index"
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
							href="#m_appointment"
							v-smooth-scroll="{ duration: 2000, offset: -50 }"
						>
							<div class="buttonBox">
								Записаться
							</div>
						</a>
						<a
							class="card__link"
							href="#"
							v-on:click.prevent="$emit('click-course', index)"
						>
							<div>
								Подробнее
							</div>
						</a>
					</div>
				</div>
				<div class="spacer" v-for="i in spacerCount" :key="i"></div>
			</div>
		</div>
		<a
			class="button_showMore"
			href="#"
			v-on:click.prevent="showMore = !showMore"
			v-if="filteredCourses.length > 4 && !showMore"
		>
			Показать еще
		</a>
	</div>
</template>
<script>
export default {
	data() {
		return {
			currentFilter: null,
			showMore: false,
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
		spacerCount() {
			return 3 - (this.courses.length % 3);
		},
		showedCourses() {
			const courses = this.filteredCourses;
			if (!this.showMore) {
				const tmp = [];
				for (let i = 0; i < 4; i++) tmp.push(courses[i]);
				return tmp;
			}
			return courses;
		},
	},
	methods: {
		textPreview(text) {
			if (text.length < 82) return text;
			else {
				const tmp = text.match(/^.{0,82}\s/);
				if (!tmp || !tmp[0]) return text;
				return tmp[0].substring(0, tmp[0].length - 1) + "...";
			}
		},
	},
};
</script>
<style scoped>
.title {
	margin: 62px auto 26px;
	text-align: center;
	font-weight: 800;
	font-size: 44px;
	line-height: 54px;
	color: #30203d;
}

/*  Фильтры */
.m_subj__filters {
	display: flex;
	text-align: center;
	margin-left: 31px;
	margin-right: 28px;
	flex-wrap: wrap;
}

.button__filter {
	margin: 7px;

	flex: 1 1 auto;
	font-family: Roboto;
	font-weight: bold;
	font-size: 14px;
	line-height: 16px;
	text-decoration: none;
	text-align: center;

	color: #4e3d95;
	background: #ffffff;

	cursor: pointer;
	border: 3px solid #4e3d95;

	display: block;
	border-radius: 50px;

	padding-top: 13px;
	padding-bottom: 13px;
	min-width: 101px;
	max-width: 186px;
}

.button__filter:hover {
	color: #f8840d;
	border: 3px solid #f8840d;
}

.button__filter:active {
	color: #ffffff;
	background: linear-gradient(97.42deg, #fb7a0d 0.1%, #fbae0d 115.11%);
}

.button__filter:focus {
	box-shadow: 0 0 0 2px #fff, 0 0 0 3px #30203d;
}

/* Cards */
.subj_cards__inner {
	display: flex;
	position: relative;
	flex-wrap: wrap;
	align-items: center;
	justify-content: center;
	margin-top: 27px;
}

/* Card */
.subj__card {
	margin-left: 10px;
	margin-right: 10px;
	margin-bottom: 20px;

	max-width: 300px;
	background: #ffffff;
	box-shadow: 4px 4px 20px rgba(48, 32, 61, 0.1);
	border-radius: 6px;
	padding: 20px 20px 30px;
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

.button_showMore {
	display: block;
	margin-left: 38px;
	margin-right: 37px;
	margin-top: 30px;
	text-align: center;
	text-decoration: none;
	padding-top: 18px;
	padding-bottom: 18px;

	background: linear-gradient(97.42deg, #fb7a0d 0.1%, #fbae0d 115.11%);
	box-shadow: 1px 4px 15px rgba(248, 132, 13, 0.35);
	border-radius: 40px;
	color: #fff;
	font-weight: bold;
	font-size: 16px;
	line-height: 19px;

	color: #ffffff;
}

@media screen and (max-width: 959px) {
	.spacer {
		display: none;
	}
}
.spacer {
	width: 100%;
	margin-left: 10px;
	margin-right: 10px;
	margin-bottom: 20px;

	max-width: 300px;
}
</style>
