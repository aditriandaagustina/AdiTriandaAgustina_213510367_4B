<template>
  <div class="cuaca-container">
    <h2>Cuaca</h2>
    <div class="weather-card">
      <div class="weather-icon">
        <img :src="weatherData.icon" :alt="weatherData.description">
      </div>
      <div class="weather-info">
        <h3>{{ weatherData.temperature }}&deg;C</h3>
        <p>{{ weatherData.city }}</p>
        <p>{{ weatherData.description }}</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Cuaca',
  data() {
    return {
      weatherData: {
        temperature: 0,
        city: '',
        description: '',
        icon: ''
      }
    };
  },
  mounted() {
    // Simulasi data cuaca
    this.weatherData.temperature = 33;
    this.weatherData.city = 'Riau';
    this.weatherData.description = 'Cerah';
    this.weatherData.icon = 'https://cdn.pixabay.com/photo/2013/07/13/12/12/sun-159392_640.png';
  }
};
</script>

<style scoped>
.cuaca-container {
  text-align: center;
}

.weather-card {
  display: inline-block;
  padding: 20px;
  border-radius: 8px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.2);
  background-color: #ffffff6f;
}

.weather-icon img {
  width: 80px;
  height: 80px;
}

.weather-info h3 {
  font-size: 24px;
  margin-bottom: 5px;
}

.weather-info p {
  font-size: 16px;
  margin-bottom: 0;
}
h2 {
  color: rgb(234, 255, 0);
}
</style>
