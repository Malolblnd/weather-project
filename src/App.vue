<template>
  <div id="app">
    <div class="weather-container">
      <WeatherApp />
    </div>
    <div class="footer-container">
      <MyFooter />
    </div>
  </div>
</template>

<script>
import WeatherApp from './components/weather.vue'
import MyFooter from './components/footer.vue'

export default {
  name: 'App',
  components: {
    WeatherApp,
    MyFooter
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  margin-top: 39px;
 

}

body {
  background-image: url("https://youngandbrave.de/wp-content/uploads/2014/12/4k-wallpaper-15-ULTRA-HD-Collections-Amazing-Wave-2016-Sunset-4K-Wallpapers.jpg");
  background-size: cover;
  background-repeat: no-repeat;
  margin-top:10px;
 
}

.weather-container {
   background: rgb(72, 70, 80);
  background: linear-gradient(90deg, rgba(72, 70, 80, 0.9304315476190477) 0%, rgba(255, 0, 142, 1) 15%, rgba(63, 73, 68, 0.36740633753501406) 78%);
  border: 5px linear-gradient(90deg, rgba(72, 70, 80, 0.9304315476190477) 0%, rgba(255, 0, 142, 1) 15%, rgba(63, 73, 68, 0.36740633753501406) 78%);
  border-style: ridge;
  border-radius:20px;
}


</style>
