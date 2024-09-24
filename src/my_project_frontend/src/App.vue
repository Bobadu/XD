<template>
	<div id="app" class="app-container">
		<main>
			<Header />
			<AboutYou />
			<Projects />
			<Skills />
			<Contact />
		</main>
	</div>
</template>

<script>
import AboutYou from './components/aboutYou.vue'
import Contact from './components/contact.vue'
import Header from './components/Header.vue'
import Projects from './components/Projects.vue'
import Skills from './components/skills.vue'

export default {
	name: 'App',
	components: {
		Header,
		AboutYou,
		Projects,
		Skills,
		Contact,
	},
}
</script>
