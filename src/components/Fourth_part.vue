<template>
	<div class="appointment__main">
		<div class="appointment__bg"></div>
		<div class="container">
			<div class="appointment__header">
				<div class="appointment__title" id="desktop_appointment">
					Записаться на пробный урок
				</div>
				<div class="appointment__text">
					Приглашаем вас познакомиться с нашими преподавателями
				</div>
			</div>
			<div class="appointment__content">
				<form class="appointment_input__form">
					<div class="form__item">
						<!-- Фамилия Имя -->
						<div class="input__wrapper">
							<div
								class="input__checkMark"
								v-show="!fullNameError && isActive"
							></div>
							<input
								class="inputCustom"
								placeholder="Константин Константинопольский"
								v-model="fullname"
							/>
							<div
								class="input__errorLabel"
								v-show="fullNameError"
							>
								Неверный формат. Введите только буквы.
							</div>
						</div>
					</div>
					<div class="form__item">
						<!-- Телефонька -->
						<div class="input__wrapper">
							<div class="input__checkMark"
							v-show="!phoneError && isActive"></div>
							<input
								v-model="phone"
								class="inputCustom"
								type="tel"
								placeholder="+79199118950"
							/>
							<div class="input__errorLabel"
							v-show="phoneError">
								Неверный формат. Введите только цифры.
							</div>
						</div>
					</div>
					<div class="form__item">
						<!-- Почта -->
						<div class="input__wrapper">
							<div class="input__checkMark"
							v-show="!emailError && isActive"></div>
							<input
								class="inputCustom"
								type="email"
								placeholder="Astronaut@gmail.com"
							/>
							<div class="input__errorLabel"
							v-show="emailError">
								Неверный формат. Введите только цифры.
							</div>
						</div>
					</div>
					<!-- Чекбокс -->
					<div
						class="form_item__checkbox form__item"
						v-on:click="checkBoxChecked = !checkBoxChecked"
					>
						<div
							class="checkbox_custom"
							v-bind:class="{ checkbox_bgrd: checkBoxChecked }"
						></div>
						<label>
							Я согласен с условиями обработки <br />
							персональных данных
						</label>
					</div>
					<div>
						<a class="buttonBox buttonOrange" href="#">
							Записаться
						</a>
					</div>
				</form>
			</div>
		</div>
	</div>
</template>
<script>
export default {
	methods: {
		validate() {},
	},
	data() {
		return {
			checkBoxChecked: false,
			fullNameError: false,
			phoneError: false,
			emailError: false,
			fullname: "",
			phone: "",
			email: "",
			isActive:false,
		};
	},
};
</script>

<style scoped>
.buttonBox {
	padding: 18px 125px;
	border-radius: 30px;
}

.buttonBox:focus {
	box-shadow: 0 0 0 2px #fefcff, 0 0 0 3px #30203d;
}

/* Main part & background */
.appointment__main {
	position: relative;
	width: 100%;
	background: url("./assets/images/appointment/appointment_bg2.svg");
	background-size: cover;
	background-position: center center;
	padding-top: 210px;
	padding-bottom: 24%;
}

.appointment__content {
	top: 0;
	margin-top: 27px;
	width: 100%;
	max-width: 405px;
}

.appointment__header {
	margin: 0 auto;

	text-align: center;
	color: #fff;
}
.appointment__title {
	font-weight: 800;
	font-size: 44px;
	line-height: 54px;
	margin-bottom: 28px;
}

.appointment__text {
	max-width: 490px;
	font-weight: 500;
	font-size: 18px;
	line-height: 150%;
	margin: 0 auto;
}

/* Input form */
.appointment_input__form {
	background: #fefcff;
	box-shadow: 0px 10px 40px rgba(0, 0, 0, 0.1);
	border-radius: 6px;
	padding: 40px 34px;
}
.form__item {
	margin-bottom: 20px;
}

.form_item__checkbox {
	position: relative;
	display: flex;

	width: 100%;
	max-width: 338px;

	cursor: pointer;
}

.container {
	width: 100%;
	margin: 0 auto;
	max-width: 925px;
}

/* Inputs */
.input__wrapper {
	position: relative;
}

.input__checkMark {
	position: absolute;
	background: url("./assets/images/appointment/appointment_checkbox_OK.svg")
		center no-repeat;
	width: 16px;
	height: 13px;
	z-index: 10;
	right: 20px;
	top: 20px;
}

.input__errorLabel {
	position: absolute;
	font-weight: 300;
	font-size: 10px;
	line-height: 12px;

	color: #e13c3c;

	left: 20px;
	bottom: -14px;
}

.inputCustom {
	background: #ffffff;
	border: 0.5px solid rgba(48, 32, 61, 0.6);
	box-sizing: border-box;
	border-radius: 30px;

	font-weight: normal;
	font-size: 14px;
	line-height: 16px;
	padding: 17px 44px 17px 20px;
	color: rgba(48, 32, 61, 0.6);

	width: 100%;
	max-width: 338px;
}

.inputCustom:focus {
	outline: none;
	box-shadow: 0 0 0 2px #fefcff, 0 0 0 3px #30203d;
}

.inputCustom:active {
	border: 0.5px solid #fb7a0d;
}

label {
	font-weight: 500;
	font-size: 14px;
	line-height: 150%;

	color: rgba(48, 32, 61, 0.6);

	cursor: pointer;
}

label::selection {
	background-color: none;
}
.checkbox_custom {
	margin-top: 2px;
	margin-right: 9px;

	background: #feffff;
	border: 0.5px solid rgba(48, 32, 61, 0.6);
	border-radius: 9px;
	height: 20px;
	width: 20px;
}

.checkbox_custom:active {
	box-shadow: 0 0 0 1px #fff, 0 0 0 2px #30203d;
}

.checkbox_bgrd {
	background: url("./assets/images/appointment/appointment__checkboxClick.svg")
		center no-repeat;
}
</style>
