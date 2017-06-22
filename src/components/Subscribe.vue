<template>
	<div id="subscribe">
		<section id="newsletter">
	      <div class="container">
	        <h1>{{ title }}</h1>
	        <form action="">
	        	<md-input-container>
			        <md-input type="email" placeholder="Enter email"></md-input>
	        	</md-input-container>
	  		    <md-button class="md-raised md-warn">{{ desc }}</md-button>
	        </form>
	      </div>
	    </section>
	</div>
</template>

<script>
export default {
	name: 'subscribe'
	,data() {
		return {
			title: 'Subscribe to our website'
			,desc: 'Subscribe'
		}
	}
}
</script>

<style scoped>
	
</style>