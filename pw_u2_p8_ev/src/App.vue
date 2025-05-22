<template>
  <!-- <HolaMundoView/> -->
  <!-- <ContadorView /> -->
  <!-- <EstudianteView/> -->
  <!-- <EstudianteTablaView/> -->
  <!-- <CarroView /> -->
   <PreguntaView/>
</template>

<script>
// import Pregunta from './components/Pregunta.vue';

  // import HolaMundoView from '@/views/HolaMundoView.vue'
  // import ContadorView from '@/views/ContadorView.vue'
  // import EstudianteTablaView from "@/views/EstudianteTablaView.vue";
  // import CarroView from "@/views/CarroView.vue";
  import PreguntaView from '@/views/PreguntaView.vue'

  export default {
    name: "App",
    components: {
      // HolaMundoView,
      // ContadorView,
      // EstudianteView,
      // EstudianteTablaView,
      // CarroView,
      PreguntaView,
    },
  };
</script>

<style>
  #app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    margin-top: 60px;
  }
</style>
