<template>
	<section class="projects">
		<h2>Projects</h2>
		<div class="project-list">
			<div class="project-card" v-for="project in projects" :key="project.title">
				<h3>{{ project.title }}</h3>
				<p>{{ project.description }}</p>
			</div>
		</div>
	</section>
</template>

<script>
export default {
	name: 'Projects',
	data() {
		return {
			projects: [
				{ title: 'Project One', description: 'Description of project one.' },
				{ title: 'Project Two', description: 'Description of project two.' },
				{ title: 'Project Three', description: 'Description of project three.' },
			],
		}
	},
}
</script>

<style scoped>
.projects {
	padding: 35px 20px;
	margin-top: 40px;
	background: linear-gradient(135deg, #1c1c1e, #2a2a2d);
	color: #ffffff;
	max-width: 1200px;
	width: 100%;
	border-radius: 16px;
	box-shadow: 0 10px 30px rgba(0, 0, 0, 0.5);
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

.projects h2 {
	font-size: 2.5rem;
	margin-left: 25px;
	color: #a3cfff;
	animation: fadeIn 1.5s ease-in-out;
}

.project-list {
	display: flex;
	flex-wrap: wrap;
	justify-content: space-around;
	gap: 20px;
	margin-top: 30px;
}

.project-card {
	background: rgba(255, 255, 255, 0.1);
	border: 1px solid #a3cfff;
	padding: 30px;
	width: 320px;
	border-radius: 16px;
	box-shadow: 0px 4px 20px rgba(163, 207, 255, 0.2);
	transition: transform 0.3s ease-in-out, box-shadow 0.3s ease-in-out;
	overflow: hidden;
	position: relative;
}

.project-card:hover {
	transform: translateY(-10px) scale(1.03);
	box-shadow: 0px 8px 30px rgba(163, 207, 255, 0.4);
	border-color: #f39c12;
}

.project-card::before {
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

.project-card:hover::before {
	transform: scaleX(1);
}

.project-card h3 {
	font-size: 1.8rem;
	color: #ffffff;
	margin-bottom: 15px;
	animation: fadeIn 2s ease-in-out;
}

.project-card p {
	font-size: 1.2rem;
	line-height: 1.6;
	color: #ffffff;
	animation: fadeIn 2s ease-in-out;
}
</style>
