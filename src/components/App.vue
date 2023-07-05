<template>
  <div class="container">
    <h1> Welcome </h1>
    <div class="card">
      <Cuaca/>
    </div>
    <div class="card">
      <Lokasi/>
    </div>
    <div class="card">
      <Stopwatch/>
    </div>
    <div class="card">
      <GameTicTacToe/>
    </div>
    <div class="card">
      <Foto/>
    </div>
  </div>
</template>

<script>
import Cuaca from './Cuaca.vue';
import Lokasi from './Lokasi.vue';
import Stopwatch from './Stopwatch.vue';
import GameTicTacToe from './GameTicTacToe.vue';
import Foto from './Foto.vue';

export default {
  components: {
    Cuaca,
    Lokasi,
    Stopwatch,
    GameTicTacToe,
    Foto
  }
}
</script>

<style scoped>
h1 {
  text-align: center;
  margin-bottom: 20px;
  color:rgb(255, 106, 0)
}
</style>
