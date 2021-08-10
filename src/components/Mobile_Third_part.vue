<template>
	<div class="about_subj">
		<div class="title">
			Наши предметы
		</div>
		<div class="m_subj__filters">
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
				v-for="item in filters"
				:key="item"
				v-on:click.prevent="currentFilter = item"
			>
				{{ item }}
			</a>
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
	margin-left: 38px;
	margin-right: 35px;
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
</style>
