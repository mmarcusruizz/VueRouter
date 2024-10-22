<template>
    <Card
      :data="{ // Se pasa un objeto como prop al componente Card
        menu: menu, // El valor de 'menu' en el objeto será igual al valor de la prop 'menu' recibida por ProductosView
        descripcion: descripcion,
        precio: precio,
        cantidad: cantidad,
      }"
    />
    <router-view />
    <div class="text-center mt-4 mb-5 p-3">
      <router-link class="btn btn-secondary p-2" to="/">Volver al inicio</router-link>
    </div>
  </template>
  
  <script>
  import Card from "../components/Card.vue";
  export default {
    components: {
      Card,
    },
    props: {
      menu: { // Se define la prop 'menu' (tipo String, requerida)
        type: String,
        required: true,
      },
      descripcion: {
        type: String,
        required: true,
      },
      precio: {
        type: String,
        required: true,
      },
      cantidad: {
        type: String,
        required: true,
      },
    },
  };
  </script>
  