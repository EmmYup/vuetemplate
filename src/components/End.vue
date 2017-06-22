<template>
	<div id="end">
		<footer>
			<p>{{name}} &copy; {{ getYear() }}</p>
		</footer>
	</div>
</template>

<script>
export default{
	name: 'end'
	,data() {
		return {
			name: 'Emmanuel Yupit, Copyright'
		}
	}
	,methods: {
		getYear: function() {
			return new Date().getFullYear();
		}
	}
}
</script>

<style scoped>

</style>