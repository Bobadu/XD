<template>
	<header class="header">
		<div class="contact-list">
			<a href="https://github.com/yourusername" target="_blank" class="contact-item">
				<i class="fab fa-github"></i> GitHub
			</a>
			<a href="https://linkedin.com/in/yourusername" target="_blank" class="contact-item">
				<i class="fab fa-linkedin"></i> LinkedIn
			</a>
			<a href="mailto:your.email@example.com" class="contact-item"> <i class="fas fa-envelope"></i> Email </a>
		</div>
	</header>
</template>

<style scoped>
.header {
	text-align: center;
	margin-bottom: 16px;
	padding: 30px 20px;
	background: linear-gradient(135deg, #0b1c3c, #1e488f);
	color: #ffffff;
	border-radius: 16px;
	max-width: 1200px;
	width: 100%;
	box-shadow: 0px 10px 30px rgba(0, 0, 0, 0.4);
	animation: fadeIn 1.5s ease-in-out;
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

.contact-list {
	display: flex;
	justify-content: center;
	gap: 40px;
}

.contact-item {
	display: flex;
	align-items: center;
	color: #ffffff;
	text-decoration: none;
	font-size: 1.4rem;
	font-weight: 500;
	padding: 10px 20px;
	border-radius: 12px;
	background: rgba(255, 255, 255, 0.1);
	transition: background 0.3s ease-in-out, transform 0.3s ease-in-out;
	box-shadow: 0px 4px 15px rgba(163, 207, 255, 0.2);
}

.contact-item i {
	margin-right: 8px;
	font-size: 1.5rem;
}

.contact-item:hover {
	background: rgba(255, 255, 255, 0.3);
	color: #f39c12;
	transform: translateY(-5px);
	box-shadow: 0px 8px 20px rgba(163, 207, 255, 0.4);
}

.contact-item:active {
	transform: translateY(0);
}

@media (max-width: 768px) {
	.contact-list {
		flex-direction: column;
		gap: 20px;
	}
}
</style>
