<template>
  <div class="lokasi-container">
    <h2>Lokasi</h2>
    <div class="map-container">
      <img :src="mapData.imageUrl" :alt="mapData.name">
      <div class="location-info">
        <h3>{{ mapData.name }}</h3>
        <p>{{ mapData.address }}</p>
        <br>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Lokasi',
  data() {
    return {
      mapData: {
        name: '',
        address: '',
        imageUrl: ''
      }
    };
  },
  mounted() {
    // Simulasi data lokasi
    this.mapData.name = 'Perpustakaan Soeman HS';
    this.mapData.address = 'Jl. Jendral Sudirman, Nomor 462Jadirejo, Sukajadi, Pekanbaru, Riau, Indonesia';
    this.mapData.imageUrl = 'https://image.slidesharecdn.com/pekanbaruriau-120619050459-phpapp01/95/pekanbaru-riau-1-728.jpg?cb=1347957637';
  }
};
</script>

<style scoped>
.lokasi-container {
  text-align: center;
}

.map-container {
  position: relative;
  display: inline-block;
  border-radius: 8px;
  overflow: hidden;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.2);
}

.map-container img {
  width: 300px;
  height: auto;
}

.location-info {
  position: absolute;
  bottom: 0;
  left: 0;
  width: 100%;
  padding: 0px;
  background-color: rgba(0, 0, 0, 0.6);
  color: #fff;
  text-align: left;
}

.location-info h3 {
  font-size: 18px;
  margin-bottom: 10px;
}

.location-info p {
  font-size: 14px;
  margin-bottom: 0;
}
h2{
  color:lime;
}
</style>

