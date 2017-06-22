<template>
  <div class="services">
    <header>
      <div class="container">
        <div id="branding">
          <h1><span class="highlight">Responsive Vue</span> Template</h1>
        </div>
        <nav>
          <ul>
            <li class="current"><a><router-link to="/">Home</router-link></a></li>
            <li><a><router-link to="/about">About</router-link></a></li>
            <li><a><router-link to="/services">Services</router-link></a></li>
          </ul>
        </nav>
      </div>
    </header>
	<subscribe></subscribe>
    <section id="main">
    	<div class="container">
    		<article id="main">
    			<h1 class="page-title">{{ title }}</h1>
    			<div id="services" v-for="service in services">
		    		<md-card md-with-hover>
		    			<md-card-header>
			    			<div class="md-title">{{ service.title }}</div>
		    			</md-card-header>
		    			<md-card-content>
		    				<p>{{ service.description }}</p>
		    				<p>{{ service.price }}</p>
		    			</md-card-content>
		    		</md-card>
    			</div>
    		</article>
    	</div>
    </section>
    <aside id="sidebar">
    	<div class="dark">
    		<h3>{{ getQuote }}</h3>
    		<form class="quote" action="">
    			<md-input-container>
    				<label>Enter your name</label>
    				<md-input type="text" placeholder="Name"></md-input>
    			</md-input-container>
    			<md-input-container>
    				<label>Enter your email</label>
    				<md-input type="email" placeholder="Email"></md-input>
    			</md-input-container>
    			<md-input-container>
    				<label>Enter your Message</label>
    				<md-textarea type="text" placeholder="Message"></md-textarea>
    			</md-input-container>
    			<md-button class="md-raised md-warn">{{ send }}</md-button>
    		</form>
    	</div>
    </aside>
	<end></end>
  </div>
</template>

<script>
import Subscribe from './subscribe'
import End from './end'
class Service {
	constructor(title,description,price) {
		this.title = title;
		this.description = description;
		this.price = price;
	}
}
export default {
  name: 'services'
  ,components: {
  	Subscribe
  	,End
  }
  ,data () {
    return {
    	title: 'Services'
    	,getQuote: 'Get a quote'
    	,send: 'Send'
    	,services: [
    		new Service(
    			'Website design'
    			,'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Molestias accusamus perferendis libero eligendi, recusandae iure, voluptate explicabo voluptas aliquam excepturi nostrum alias a aperiam, eveniet porro labore, distinctio ipsum. Iusto?'
    			,'Pricing: $1,000 - $3,000'
    			)
    		,new Service(
    			'SEO'
    			,'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Molestias accusamus perferendis libero eligendi, recusandae iure, voluptate explicabo voluptas aliquam excepturi nostrum alias a aperiam, eveniet porro labore, distinctio ipsum. Iusto?'
    			,'Pricing: $250 per month'
    			)
    		,new Service(
    			'Hosting'
    			,'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Molestias accusamus perferendis libero eligendi, recusandae iure, voluptate explicabo voluptas aliquam excepturi nostrum alias a aperiam, eveniet porro labore, distinctio ipsum. Iusto?'
    			,'Pricing: $25 per month'
    			)
    	]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
