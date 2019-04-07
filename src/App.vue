<template>
  <div id="app">
    <HeaderCommon></HeaderCommon>
    <main>
    <router-view/>
    <Weather></Weather>
    </main>
    <footer>
        <p>&copy;Ankh-Systems s-nakanos</p>
    </footer>
  </div>
</template>

<script>
import HeaderCommon from './HeaderCommon'
import Weather from './Weather'
export default {
  name: 'App',
  components: {
    HeaderCommon, Weather
  }
}
</script>

<style>
#app {
/*  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;*/
}
</style>
