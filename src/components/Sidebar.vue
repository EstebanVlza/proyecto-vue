<template>
  <div class="sidebar">
    <h2>Bienvenido</h2>
    <h3>Nombre: {{ nombre }}</h3>
    <h3>Email: {{ email }}</h3>
    <ul>
      <li><Router-Link to="/contador">Contador</Router-Link></li>
      <li><Router-Link to="/lista-de-tareas">Lista de Tareas</Router-Link></li>
      <li><Router-Link to="/registrar">Registrar</Router-Link></li>

    </ul>
  </div>
</template>
<script setup>
import { useRegistrarStore } from '@/modules/registro/stores/registrarStore';
import {ref, watch} from 'vue';
const registarStore = useRegistrarStore();
const nombre = ref(registarStore.nombre.value);
const email = ref(registarStore.email.value);
watch(() => registarStore.nombre, (newValue) => {
  nombre.value = newValue;

});
watch(() => registarStore.email, (newValue) => {
  email.value = newValue;

});
</script>
<style>
.sidebar{
  width: 200px;
  background-color: #f0f0f0;
  padding: 20px;
}
</style>
