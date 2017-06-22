<template>
  <div class="about">
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
    		<article id="mail-col">
    			<h1 class="page-title">{{ title }}</h1>
    			<p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Dignissimos, sequi! Omnis id dolorum nesciunt temporibus ex eius perferendis, a quasi facere illum maxime porro suscipit deserunt consequuntur repellendus eum. Quidem.</p>
    			<p class="dark">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Numquam similique voluptatibus commodi dolores, fugiat repellendus temporibus, a quas distinctio, voluptates consequatur nisi maxime cupiditate eos iusto rem autem hic, unde!</p>
    		</article>
    		<aside id="sidebar">
    			<div class="dark">
    				<h3>{{ subtitle }}</h3>
    				<p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Eveniet consectetur facere assumenda. Repellendus recusandae quasi, aliquam, corporis sit omnis! Nihil voluptas aut repellendus similique voluptatum voluptate veniam minima mollitia veritatis!</p>
    			</div>
    		</aside>
    	</div>
    </section>
    <end></end>
  </div>
</template>

<script>
import Subscribe from './subscribe'
import End from './end'
export default {
  name: 'about'
  ,components: {
  	Subscribe
  	,End
  }
  ,data () {
    return {
      msg: 'Welcome to Your Vue.js App'
      ,title: 'About Us'
      ,subtitle: 'What Vue do'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
