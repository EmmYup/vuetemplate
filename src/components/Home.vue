<template>
  <div class="home">
    <header>
      <div class="container">
        <div id="branding">
          <h1><span class="highlight">Responsive Vue</span> Template</h1>
        </div>
        <nav>
          <ul>
            <li class="current alink"><router-link to="/">Home</router-link></li>
            <li><a><router-link to="/about">About</router-link></a></li>
            <li><a><router-link to="/services">Services</router-link></a></li>
          </ul>
        </nav>
      </div>
    </header>
    <section id="showcase">
      <div class="container">
        <h1>This is a professional Vue Responsive website</h1>
        <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Ex hic est commodi, veniam voluptas placeat dolorem quaerat ullam assumenda dignissimos molestiae repudiandae quam facere laborum harum aspernatur vitae quasi libero.</p>
      </div>
    </section>
    <subscribe></subscribe>
    <section id="tech">
      <div class="container">
        <div class="box" v-for="tech in techs">
          <img :src="getImgUrl(tech.logo)">
          <h3>{{tech.title}}</h3>
          <p>{{tech.description}}</p>
        </div >
      </div>
    </section>
    <end></end>
  </div>
</template>

<script>
import Subscribe from './subscribe'
import End from './end'
class Tech {
  constructor(logo,title,description){
    this.logo = logo;
    this.title = title;
    this.description = description;
  }
}
export default {
  name: 'home'
  ,components: {
    End
    ,Subscribe
  }
  ,data () {
    return {
      techs: [
        new Tech(
            'html'
            ,'HTML5 Markup'
            ,'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aut odit laboriosam magni, cupiditate delectus ex rem in et accusantium, sequi, mollitia. Debitis labore magni nostrum minus adipisci consequatur iure praesentium!'
          )
        ,new Tech(
          'css'
          ,'CSS3 Styling'
          ,'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Nostrum animi soluta quis voluptate ea explicabo assumenda excepturi obcaecati voluptatibus repudiandae aliquam odit, molestiae dicta illum repellat doloribus, laboriosam voluptatem odio!'
          )
        ,new Tech(
          'angular'
          ,'Spectangular!'
          ,'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Totam quaerat rem, eos incidunt. Hic, necessitatibus, provident, cupiditate odit vel velit numquam maiores voluptas error corporis dolores officia illum consequatur placeat.'
          )
      ]
    }
  }
  ,methods: {
    getImgUrl: function(img) {
      var images = require.context('../assets/',false,/\.png$/);
      return images('./' + img + ".png");
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
