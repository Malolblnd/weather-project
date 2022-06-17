<template>
  <div class="hello">
    <div class="container-fluid">
      <div class="row my-header">
        <div class="col">
          <span class="title">INOVA WEATHER</span>

        </div>
        <div class="form-group col mb-5">
          <input type="text" id="position" placeholder="Saisir le nom d'une ville..." class="form-group text-input" v-model="input"
            v-on:keypress.enter="getWeather">
          <button type="button" class="btn btn-primary search-btn"  aria-pressed="false" v-on:click="getWeather">
            Search
          </button>
          <!-- <img class="terre" src="https://i.pinimg.com/originals/61/10/76/611076774d5719f42341274cf7017adb.png"
            width="200px" /> -->

        </div>

      </div>
    </div>

    <h1><strong>Weather app to make your life easier</strong></h1>
    <h2>My contact for more informations:

      <ul><a class="insta" href="https://www.instagram.com/malo_lbld/">@MALO_LBLD</a>
       
      </ul>



    </h2>

    


    <div class="weather" v-if="weather">
      City: {{ weather.name }}
      <br />
      Weather: {{ weather.weather[0].description }}
      <br />
      Temperature in celsius: {{ weather.main.temp.toFixed() }}°c
    </div>
    <div v-else>
      y a r pour le moment
    </div>
   

  </div>


</template>

<script>
import axios from 'axios';

export default {
  name: 'WeatherApp',
  data() {
    return {
      apiKey: '',
      input: null,
      searchRequest: 'https://api.openweathermap.org/data/2.5/weather?',
      temperature: null,
      weather: null,
    }
  },
  async mounted() {
    await this.getWeather();
  },
  methods: {
    async getWeather() {
      const townName = this.input ?? 'Paris';
      try {
        await axios.get(`${this.searchRequest}q=${townName}&units=metric&APPID=${this.apiKey}&lang=fr`).then((response) => {
          this.weather = response.data;
        });
        this.input = '';
      } catch (e) {
        console.debug(e);
      }
    }
  }

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped >

@media  (max-width: 768px){ 
  .search-btn{
    display:none;
  }
}
.hello {
  color: white;
  font-size: 20px;
}

h1 {
  color: whitesmoke;
  font-size: 30px;
}

.my-header {
  display: flex;
  justify-content: space-between;
}

.title {
  margin-left: 15px;
  margin-top: 5px;
  font-size: 30px;
}


.form-group {
  height: 30px;
  border-radius: 15px;
  padding-left: 5px;
  font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
}

.btn {
  border-radius: 15px;
  height: 35px;
  width:auto;
  margin-top: 10px;
  padding: 0px 10px;
  
}
.weather{
  font-size:30px;
  padding-bottom:20px;
}
.insta{
  color:aqua;
  text-decoration:none;
}

</style>
