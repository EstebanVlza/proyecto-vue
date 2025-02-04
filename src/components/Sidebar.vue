<template>
  <div class="sidebar">
    <h2>
      Barra lateral
    </h2>
    <ul>
      <li><Router-Link to="/contador">Contador</Router-Link></li>
      <li><Router-Link to="/lista-de-tareas">Lista de Tareas</Router-Link></li>
    </ul>
  </div>
</template>
<script setup>
</script>
<style>
.sidebar{
  width: 200px;
  background-color: #f0f0f0;
  padding: 20px;
}
</style>
