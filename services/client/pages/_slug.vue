<script>
const HOMEPAGE = Object.freeze('index')

export default {
	async asyncData({ $content, params }) {
		const page = await $content(params.slug || HOMEPAGE).fetch()
		return { page }
	},
	head() {
		const {
			description,
			title,
		} = this.page
		return {
			title,
			meta: [
				{
					content: description,
					hid: 'description',
					name: 'description',
				},
			]
		}
	},
}
</script>

<template>
	<main>
		<h1>{{ page.title }}</h1>
		<nuxt-content :document="page"/>
	</main>
</template>
