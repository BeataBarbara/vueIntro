<template>
  <div class="hello">
    <Header />
    <Container />
    <Footer />
    <User-data-info />
    <h1>{{ msg }}</h1>
    <p v-if="show">Lorem ipsum dolor sit amet consectetur adipisicing elit. Veritatis ratione nesciunt veniam dolores debitis odit quaerat dolorem porro deleniti recusandae officiis eveniet illum, doloremque necessitatibus quas voluptates corporis sit. Beatae?</p>
    <li v-for="item in items" :key="item">
      {{ item }}
    </li>
    <p> 
         <ul>
      <li v-for="tableOfObject in tableOfObjects" :key="tableOfObject.object">
        {{ tableOfObject.object }}
      </li>
    </ul> 
    </p>

    
    
    <p>

      For a guide and recipes on how to configure / customize this project,<br />
      check out the
      <a href="https://cli.vuejs.org" target="_blank" rel="noopener"
        >vue-cli documentation</a
      >.
    </p>

  </div>
</template>

<script>
import Container from './Container.vue';
import Header from './Header.vue';
import Footer from './Footer.vue';
import UserDataInfo from './UserDataInfo.vue'
export default {
  components: { Header, Container, Footer, UserDataInfo },
  name: "HelloWorld",
  props: {
    msg: String,
  },
  data() {
    return{
    myName: "Beata",
    show: true,
     items: ['Foo', 'Bar','Elo'],
     tableOfObjects: [
       {object: 'kaczka'},
       {object: 'długopis'},
       {object: 'naklejka'},
       {object: 'czekoladka'},
       {object: 'stojak'}

     ]
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
