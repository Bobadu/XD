<template>
	<section class="skills">
		<h2>Skills</h2>
		<div class="skill-list">
			<div class="skill" v-for="skill in skills" :key="skill">
				{{ skill }}
			</div>
		</div>
	</section>
</template>

<script>
export default {
	name: 'Skills',
	data() {
		return {
			skills: ['HTML', 'CSS', 'SCSS', 'LUA', 'C++', 'Vue.js', 'Python3', 'JavaScript', 'XML', 'Java'],
		}
	},
}
</script>

<style scoped>
.skills {
	padding: 60px 20px;
	background: linear-gradient(135deg, #0b1c3c, #1e488f);
	color: #ffffff;
	text-align: center;
	max-width: 1200px;
	width: 100%;
	border-radius: 16px;
	box-shadow: 0 10px 30px rgba(0, 0, 0, 0.5);
	margin-top: 40px;
	animation: fadeIn 1s ease-in-out;
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

.skills h2 {
	font-size: 2.5rem;
	margin-bottom: 30px;
	color: #a3cfff;
	animation: fadeIn 1.5s ease-in-out;
}

.skill-list {
	display: flex;
	justify-content: center;
	flex-wrap: wrap;
	gap: 20px;
}

.skill {
	background: rgba(255, 255, 255, 0.1);
	border: 1px solid #a3cfff;
	padding: 15px 30px;
	margin: 10px;
	border-radius: 16px;
	box-shadow: 0px 4px 20px rgba(163, 207, 255, 0.2);
	font-size: 1.2rem;
	color: #ffffff;
	transition: transform 0.3s ease-in-out, box-shadow 0.3s ease-in-out;
	animation: fadeIn 2s ease-in-out;
}

.skill:hover {
	transform: translateY(-10px) scale(1.05);
	box-shadow: 0px 8px 30px rgba(163, 207, 255, 0.4);
	border-color: #f39c12;
}

.skill::before {
	content: '';
	position: absolute;
	top: 0;
	left: 0;
	width: 100%;
	height: 100%;
	background: linear-gradient(135deg, rgba(243, 156, 18, 0.3), transparent);
	transform: scaleX(0);
	transform-origin: left;
	transition: transform 0.4s ease-in-out;
}

.skill:hover::before {
	transform: scaleX(1);
}
</style>
