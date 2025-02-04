<template>
  <div class="sidebar">
    <h2>Bienvenido</h2>
    <h3>Nombre: {{ registarStore.nombre }}</h3>
    <h3>Email: {{ registarStore.email }}</h3>
    <ul>
      <li><Router-Link to="/contador">Contador</Router-Link></li>
      <li><Router-Link to="/lista-de-tareas">Lista de Tareas</Router-Link></li>
      <li><Router-Link to="/registrar">Registrar</Router-Link></li>

    </ul>
  </div>
</template>
<script setup>
import { useRegistrarStore } from '@/modules/registro/stores/registrarStore';

const registarStore = useRegistrarStore();

</script>
<style>
.sidebar{
  width: 200px;
  background-color: #f0f0f0;
  padding: 20px;
}
</style>
