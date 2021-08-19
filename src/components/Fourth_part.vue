<template>
	<div class="appointment__main">
		<div class="appointment__bg">
			<img src="./assets/images/appointment/appointment_bg2.svg" alt="" />
		</div>
		<div class="appointment__wrapper">
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
									v-show="
										!fullNameError && !fullNameIsFocused
									"
								></div>
								<input
									class="inputCustom"
									placeholder="Фамилия Имя"
									v-model="fullname"
									v-on:blur="validationFullName()"
									v-on:focus="fullNameIsFocused = true"
									v-bind:class="{
										inputCustomError: fullNameError,
									}"
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
								<div
									class="input__checkMark"
									v-show="!phoneError && !phoneIsFocused"
								></div>
								<input
									v-model="phone"
									class="inputCustom"
									type="tel"
									placeholder="Телефон"
									v-on:blur="validataionPhone()"
									v-on:focus="phoneIsFocused = true"
									v-bind:class="{
										inputCustomError: phoneError,
									}"
								/>
								<div
									class="input__errorLabel"
									v-show="phoneError"
								>
									Неверный формат. Введите корректный телефон.
								</div>
							</div>
						</div>
						<div class="form__item">
							<!-- Почта -->
							<div class="input__wrapper">
								<div
									class="input__checkMark"
									v-show="!emailError && !emailIsFocused"
								></div>
								<input
									v-model="email"
									class="inputCustom"
									type="email"
									placeholder="Email"
									v-on:blur="validataionEmail()"
									v-on:focus="emailIsFocused = true"
									v-bind:class="{
										inputCustomError: emailError,
									}"
								/>
								<div
									class="input__errorLabel"
									v-show="emailError"
								>
									Неверный формат. Введите корректный email.
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
								v-bind:class="{
									checkbox_bgrd: checkBoxChecked,
								}"
							></div>
							<label>
								Я согласен с условиями обработки <br />
								персональных данных
							</label>
						</div>
						<div>
							<a
								class="buttonBox buttonOrange"
								href="#"
								v-on:click.prevent="sendRequset()"
							>
								Записаться
							</a>
						</div>
					</form>
				</div>
			</div>
		</div>
	</div>
</template>
<script>
import { GoogleSpreadsheet } from "google-spreadsheet";
import creds from "../google-api-key.json";
export default {
	methods: {
		async sendRequset() {
			if (this.validataion) {
				let doc = new GoogleSpreadsheet(
					"1VRhWH8856QPfIxbyCKLnacH863D8Jir4BleZ-9mlBqo"
				);
				await doc.useServiceAccountAuth(creds);
				await doc.loadInfo();
				const sheet = await doc.sheetsByIndex[0];
				await sheet.addRows([
					{
						ФИО: this.fullname,
						Телефон: this.phone,
						Почта: this.email,
					},
				]);
				// Показать попу
				this.email = "";
				this.phone = "";
				this.fullname = "";
			}
		},
		validataion() {
			return !this.fullNameError && !this.phoneError && !this.emailError;
		},
		validationFullName() {
			this.fullNameIsFocused = false;
			this.fullNameError = !this.fullname.match(/^\S+(\s\S+)*$/);
		},
		validataionPhone() {
			this.phoneIsFocused = false;
			this.phoneError = !this.phone.match(/^\+\d{4,}$/);
		},
		validataionEmail() {
			this.emailIsFocused = false;
			this.emailError = !this.email.match(/^\S*@\S*$/);
		},
	},
	props: {
		checkBoxChecked: {
			type: Boolean,
			required: true,
		},
		fullNameError: {
			type: Boolean,
			required: true,
		},
		phoneError: {
			type: Boolean,
			required: true,
		},
		emailError: {
			type: Boolean,
			required: true,
		},
		fullname: {
			type: String,
			required: true,
		},
		phone: {
			type: String,
			required: true,
		},
		email: {
			type: String,
			required: true,
		},
		fullNameIsFocused: {
			type: Boolean,
			required: true,
		},
		phoneIsFocused: {
			type: Boolean,
			required: true,
		},
		emailIsFocused: {
			type: Boolean,
			required: true,
		},
	},
};
</script>

<style scoped>
.buttonBox {
	font-weight: bold;
	font-size: 16px;
	line-height: 19px;

	color: #ffffff;

	padding: 18px 106px;
	border-radius: 30px;
}

.buttonBox:focus {
	box-shadow: 0 0 0 2px #fefcff, 0 0 0 3px #30203d;
}

/* Main part & background */
.appointment__bg img {
	object-fit: cover;
	width: 100%;
}

.appointment__wrapper {
	position: absolute;
	top: 0;
	right: 0;
	left: 0;
	bottom: 0;
	display: flex;
	justify-content: center;
	align-items: center;
}

.appointment__main {
	position: relative;
	width: 100%;
}

.appointment__content {
	top: 0;
	margin-top: 27px;
	/* margin-top: 2vw; */
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
	margin: -217px auto 0;
	max-width: 925px;
	position: relative;
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
	border-radius: 30px;
	box-sizing: border-box;
	font-weight: normal;
	font-size: 14px;
	line-height: 16px;
	padding: 17px 44px 17px 20px;
	color: rgba(48, 32, 61, 0.6);

	width: 100%;
	max-width: 338px;
}

.inputCustomError {
	border-color: #e13c3c;
	color: #e13c3c;
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
