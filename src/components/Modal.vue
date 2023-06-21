<script setup>
import cerrarModal from '../assets/img/cerrar.svg';

const emit = defineEmits(['ocultar-modal']);
</script>

<template>
  <div class="modal">
    <div class="cerrar-modal">
      <img
        :src="cerrarModal"
        alt="cerrar modal"
        @click="$emit('ocultar-modal')" />
    </div>

    <div class="contenedor">
      <form action="">
        <legend>Añadir Gastos</legend>
        <div class="campo">
          <label for="nombre">Nombre Gasto:</label>
          <input type="number" id="nombre" placeholder="Añade el Gasto" />
        </div>

        <div class="campo">
          <label for="cantidad">Cantidad:</label>
          <input
            type="number"
            id="cantidad"
            placeholder="Añade la cantidad del Gasto, ej. 300" />
        </div>

        <div class="campo">
          <label for="categoria">Categoria:</label>
          <select id="categoria">
            <option value="ahorro">Ahorro</option>
            <option value="comida">Comida</option>
            <option value="casa">Casa</option>
            <option value="gastos">Gastos Varios</option>
            <option value="ocio">Ocio</option>
            <option value="salud">Salud</option>
            <option value="suscripciones">Suscripciones</option>
          </select>
        </div>
        <input type="submit" value="Añadir gasto"/>
      </form>
    </div>
  </div>
</template>

<style scoped>
.modal {
  position: absolute;
  background-color: rgb(0 0 0 / 0.9);
  top: 0;
  bottom: 0;
  right: 0;
  left: 0;
}
.cerrar-modal {
  position: absolute;
  right: 3rem;
  top: 3rem;
}
.cerrar-modal img {
  width: 3rem;
  cursor: pointer;
}
</style>
