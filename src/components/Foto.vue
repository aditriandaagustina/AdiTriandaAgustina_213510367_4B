<template>
    <div class="foto-container">
      <h2>Foto</h2>
      <div class="photo-gallery">
        <div v-for="(photo, index) in photos" :key="index" class="photo">
          <img :src="photo.imageUrl" :alt="photo.title">
          <div class="caption">
            <h3>{{ photo.title }}</h3>
            <p>{{ photo.description }}</p>
          </div>
        </div>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    name: 'Foto',
    data() {
      return {
        photos: [
          {
            title: 'BMW',
            description: 'First founded by Franz Josef Popp in 1916.',
            imageUrl: 'https://www.selasar.com/wp-content/uploads/2020/03/gambar-di-mobil-truk.jpg'
          },
          {
            title: 'Jeep',
            description: 'Reliable when passing through hilly terrain, dashing against swift currents.',
            imageUrl: 'https://www.selasar.com/wp-content/uploads/2020/04/gambar-mobil-mobilan.jpg'
          },
          {
            title: 'Pajero',
            description: 'His body is cute and stylish, feels dashing when seen.',
            imageUrl: 'https://www.selasar.com/wp-content/uploads/2020/04/gambar-mobil-estilo.jpg'
          }
        ]
      };
    }
  };
  </script>
  
  <style scoped>
  .foto-container {
    text-align: center;
  }
  
  .photo-gallery {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    grid-gap: 20px;
  }
  
  .photo {
    position: relative;
    overflow: hidden;
    border-radius: 8px;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.2);
  }
  
  .photo img {
    width: 100%;
    height: auto;
  }
  
  .caption {
    position: absolute;
    bottom: 0;
    left: 0;
    width: 100%;
    padding: 10px;
    background-color: rgba(0, 0, 0, 0.6);
    color: #fff;
    text-align: left;
  }
  
  .caption h3 {
    font-size: 18px;
    margin-bottom: 5px;
  }
  
  .caption p {
    font-size: 14px;
    margin-bottom: 0;
  }
  h2{
    color:rgb(32, 255, 251);
  }
  </style>
  
  