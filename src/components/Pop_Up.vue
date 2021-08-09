<template>
	<div class="popUp__main" v-if="course" v-on:click.prevent="checkClick($event)">
		<div class="popUp__container">
			<a
				class="popUp_close__wrapper"
				href="#"
				v-on:click.prevent="$emit('close-popup')"
			>
				<div class="popUp__close"></div>
			</a>
			<div class="popUp__title">{{ course.title }}</div>
			<div class="subtitle__label">
				О курсе:
			</div>
			<div class="popUp__description">
				{{ course.desc }}
			</div>
			<div class="subtitle__label">
				Чему научится студент на базовом курсе:
			</div>
			<ul>
				<li v-for="item in course.merits" :key="item">{{ item }}</li>
			</ul>
			<div class="popUp__statistics">
				<div
					class="popUp_stat__item"
					v-for="item in course.statistics"
					:key="item"
				>
					<div class="stat_item__circle">{{ item.number }}</div>
					<div class="stat_item__text">
						{{ item.text }}
					</div>
				</div>
			</div>
			<a class="popUp__button" href="#">
				<div class="popUp__buttonBox">
					Записаться
				</div>
			</a>
		</div>
	</div>
</template>
<script>
export default {
	props: {
		course: {
			type: Object,
		},
	},
	methods: {
		checkClick(event) {
			console.log(event.target.classList);
			if (event.target.classList.contains("popUp__main"))
				this.$emit("close-popup");
		},
	},
};
</script>
<style scoped>
.popUp__main {
	display: flex;
	background: rgba(62, 58, 68, 0.52);
	position: fixed;
	z-index: 1000;
	top: 0;
	right: 0;
	left: 0;
	bottom: 0;
}

.popUp__container {
	align-items: center;
	justify-content: center;

	position: relative;

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

.popUp_close__wrapper {
	position: absolute;
	display: inline-block;
	border-radius: 9px;
	right: 31px;
	top: 17px;
	height: 42px;
	width: 42px;
	z-index: 10;
}
.popUp_close__wrapper:focus {
	box-shadow: 0 0 0 1px #30203d;
}
.popUp__close {
	background: url("./assets/images/PopUp_Close.svg");
	display: inline-block;
	height: 42px;
	width: 42px;
	position: relative;
}

.popUp__close:after {
	display: block;
	content: "";
	opacity: 0;
	width: 25px;
	height: 1px;
	background-color: #f8840d;
	position: absolute;
	bottom: 6px;
	left: 9px;
}

.popUp__close:active:after {
	opacity: 1;
}

.popUp__close:hover {
	background: url("./assets/images/PopUp_CloseHover.svg");
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
	display: flex;
	position: relative;
	justify-content: space-between;
	text-align: center;

	margin-top: 19px;
	margin-bottom: 34px;
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
	margin-left: auto;
	margin-right: auto;
}

.popUp__button {
	margin-left: 345px;
	text-decoration: none;
	border-radius: 40px;
	display: inline-block;
}

.popUp__button:focus {
	box-shadow: 0 0 0 2px #fff, 0 0 0 3px #070707;
}

.popUp__buttonBox {
	background: linear-gradient(141.18deg, #4e3d95 -8.71%, #413373 104.75%);
	color: #fff;
	padding: 18px 73px;
	border-radius: 40px;
	text-align: center;
	width: 100%;
	max-width: 235px;

	cursor: pointer;
	margin: 0;
	border: none;

	display: inline-block;
	vertical-align: top;
}

.popUp__buttonBox:hover {
	background: linear-gradient(97.42deg, #fb7a0d 0.1%, #fbae0d 115.11%);
	box-shadow: 1px 4px 15px rgba(248, 132, 13, 0.55);
}
</style>
