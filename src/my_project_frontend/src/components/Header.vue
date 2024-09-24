<script setup>
import { ref } from 'vue'
import { my_project_backend } from 'declarations/my_project_backend/index'
let greeting = ref('')

async function handleSubmit(e) {
	e.preventDefault()
	const target = e.target
	const name = target.querySelector('#name').value
	await my_project_backend.greet(name).then(response => {
		greeting.value = response
	})
}
</script>

<template>
	<img src="/logo2.svg" alt="DFINITY logo" class="icp-img" />
	<form action="#" @submit="handleSubmit">
		<label for="name">Enter your name: &nbsp;</label>
		<input id="name" alt="Name" type="type" />
		<button type="submit">Click Me!</button>
	</form>
	<header>
		<h1 id="greeting">{{ greeting }}</h1>
		<h2>Frontend Developer</h2>
	</header>
</template>

<style scoped>
header {
	margin-top: 40px;
	text-align: center;
	padding: 85px 20px;
	background: linear-gradient(to right, #0b1c3c, #1e488f);
	color: #fff;
	border-radius: 48px;
	max-width: 1200px;
	width: 100%;
	box-shadow: 0px 0px 32px 6px rgba(30, 72, 143, 1);
	transition: all 0.5s ease-in-out;
	position: relative;
	overflow: hidden;
}

header::before {
	content: '';
	position: absolute;
	top: -50%;
	left: -50%;
	width: 200%;
	height: 200%;
	background: radial-gradient(circle at center, rgba(255, 255, 255, 0.2), transparent);
	transform: rotate(30deg);
	animation: rotateBackground 15s linear infinite;
}

@keyframes rotateBackground {
	from {
		transform: rotate(0deg);
	}
	to {
		transform: rotate(360deg);
	}
}

h1 {
	font-size: 4rem;
	margin-bottom: 10px;
	animation: fadeIn 1s ease-in-out;
	color: #fff;
}

@keyframes fadeIn {
	0% {
		opacity: 0;
		transform: translateY(-20px);
	}
	100% {
		opacity: 1;
		transform: translateY(0);
	}
}

h2 {
	font-size: 2rem;
	color: #a3cfff;
	animation: fadeIn 1.5s ease-in-out;
}

form {
	display: flex;
	flex-direction: row;
	align-items: center;
	justify-content: center;
	gap: 16px;
	margin-top: 20px;
}

input {
	padding: 10px 15px;
	font-size: 1rem;
	border-radius: 24px;
	border: 2px solid #a3cfff;
	outline: none;
	transition: all 0.3s ease-in-out;
}

input:focus {
	border-color: #fff;
	box-shadow: 0px 0px 10px rgba(163, 207, 255, 0.8);
}

button {
	padding: 10px 20px;
	font-size: 1.2rem;
	border: none;
	border-radius: 24px;
	background-color: #1e488f;
	color: #fff;
	cursor: pointer;
	transition: all 0.3s ease-in-out;
	box-shadow: 0px 4px 15px rgba(30, 72, 143, 0.5);
}

button:hover {
	background-color: #fff;
	color: #1e488f;
	box-shadow: 0px 4px 15px rgba(255, 255, 255, 0.5);
	transform: scale(1.05);
}

.icp-img {
	margin-top: 16px;
	width: 150px;
	animation: logoBounce 2s infinite;
}

@keyframes logoBounce {
	0%,
	100% {
		transform: translateY(0);
	}
	50% {
		transform: translateY(-10px);
	}
}
</style>
