<template>
  <div id="app">
    <ul>
      <li><a href="default.asp">Home</a></li>
      <li><a href="news.asp">News</a></li>
      <li><a href="contact.asp">Contact</a></li>
      <li><a href="about.asp">About</a></li>
    </ul>
    <div class="main">
    
    </div>
    <AddActivities msg="Welcome to Your Vue.js App"/>
  </div>
</template>

<script>
import AddActivities from './components/AddActivities.vue'

export default {
  name: 'App',
  components: {
    AddActivities
  },
  data() {
            return {
                
            }
        }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin:60px auto;
  flex: 1;
  max-width: 800px;
}

ul {
  list-style-type: none;
  margin: 0;
  padding: 0;
  overflow: hidden;
  background-color: #333;
  border-radius: 10px;
}

li {
  float: left;
}

li a {
  display: block;
  color: white;
  text-align: center;
  padding: 14px 16px;
  text-decoration: none;
}

/* Change the link color to #111 (black) on hover */
li a:hover {
  background-color: #111;
}
</style>
