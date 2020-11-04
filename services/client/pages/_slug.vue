<script>
const HOMEPAGE = Object.freeze('index')

export default {
	async asyncData({ $content, params }) {
		const page = await $content(params.slug || HOMEPAGE).fetch()
		return { page }
	}
}
</script>

<template>
	<main>
		<h1>{{ page.title }}</h1>
		<nuxt-content :document="page"/>
	</main>
</template>
