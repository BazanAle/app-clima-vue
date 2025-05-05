<template>
  <h1 class="titulo">Buscador de clima</h1>
  <div class="contenedor buscador-clima">
    <Formulario @obtener-clima="obtenerClima"></Formulario>
    <Spinner v-if="cargando" />
    <Alerta v-if="error">{{ error }}</Alerta>
    <Clima v-if="mostrarClima" :clima="clima"></Clima>
  </div>
</template>
<script setup>
import Formulario from "./components/Formulario.vue";
import useClima from "./composables/useClima";
import Clima from "./components/Clima.vue";
import Alerta from "./components/Alerta.vue";
import Spinner from "./components/Spinner.vue";
const { obtenerClima, clima, mostrarClima, cargando, error } = useClima();
console.log();
</script>
