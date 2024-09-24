<template>
	<section class="about">
		<h2>About You</h2>
		<div class="about-content">
			<p>{{ aboutText }}</p>
		</div>
	</section>
</template>

<script>
export default {
	name: 'AboutUs',
	data() {
		return {
			aboutText: 'Short description about you 🙂',
		}
	},
}
</script>

<style scoped>
.about {
	margin-top: 40px;
	padding: 35px 20px;
	background: linear-gradient(135deg, #1c1c1e, #2a2a2d);
	color: #ffffff;
	max-width: 1200px;
	width: 100%;
	border-radius: 16px;
	box-shadow: 0 10px 30px rgba(0, 0, 0, 0.5);
	animation: fadeIn 1s ease-in-out;
	position: relative;
	overflow: hidden;
}

.about::before {
	content: '';
	position: absolute;
	top: 0;
	left: 0;
	width: 100%;
	height: 100%;
	background: radial-gradient(circle at top left, rgba(255, 255, 255, 0.1), transparent);
	transform: rotate(45deg);
	animation: rotateBackground 10s linear infinite;
}

@keyframes rotateBackground {
	from {
		transform: rotate(0deg);
	}
	to {
		transform: rotate(360deg);
	}
}

@keyframes fadeIn {
	0% {
		opacity: 0;
		transform: translateY(20px);
	}
	100% {
		opacity: 1;
		transform: translateY(0);
	}
}

.about h2 {
	font-size: 2.5rem;
	margin-left: 10px;
	color: #a3cfff;
	animation: fadeIn 1.5s ease-in-out;
}

.about-content {
	margin: 10px;
	padding: 30px;
	background: rgba(255, 255, 255, 0.1);
	border: 1px solid #a3cfff;
	border-radius: 16px;
	backdrop-filter: blur(10px);
	box-shadow: 0px 4px 15px rgba(163, 207, 255, 0.2);
	transition: all 0.3s ease-in-out;
}

.about-content:hover {
	transform: scale(1.02);
	box-shadow: 0px 6px 20px rgba(163, 207, 255, 0.4);
}

.about-content p {
	font-size: 1.2rem;
	line-height: 1.6;
	color: #ffffff;
	animation: fadeIn 2s ease-in-out;
}
</style>
