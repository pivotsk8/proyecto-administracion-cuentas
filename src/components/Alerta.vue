<!-- el slot nos sirve para recuperar informacion desde a donde se llama el componenete si necesidad de
     pasar props ver el componente Presupuesto para ver como recupera la informacion -->
<template>
  <div class="alerta">
    <slot></slot>
  </div>
</template>

<style scoped>
.alerta {
  padding: 1rem;
  font-size: 900;
  text-transform: uppercase;
  font-size: 1.6rem;
  text-align: center;
  background-color: var(--blanco);
  border-left: 0.5rem solid red;
  color: red;
  margin-bottom: 2rem;
}
</style>
