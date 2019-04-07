<template>
  <div id="p−Weather">
    <div class="weather_info">
      <p class="weather_city">{{ city }}</p>
      <p class="weather_condition">{{ condition.main }}</p>
      <p class="weather_temp">{{ temp | roundUp }}&deg;C</p>
    </div>
  </div>
</template>

<script>
import axios from 'axios'
export default {
  name: 'Weather',
  data: function () {
    return {
      city: null,
      temp: null,
      condition: {
        main: null
      }
    }
  },
  mounted: function () {
    axios.get('https://api.openweathermap.org/data/2.5/weather?q=Osaka,jp&units=metric&appid=d7da53398134f79c4addcf16fe3f913c').then(function (response) {
      console.log(response)

      this.city = response.data.name
      this.temp = response.data.main.temp
      this.condition = response.data.weather[0]
    }.bind(this)).catch(function (error) {
      console.log(error)
    })
  },
  filters: {
    roundUp (value) {
      return Math.ceil(value)
    }
  }
}
</script>

<style>

</style>
