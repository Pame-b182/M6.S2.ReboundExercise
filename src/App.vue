<template>
  <div id="app">
    <!-- Etiqueta personalizada correspondiente al componente -->
    <Form/>
  </div>
</template>

<script>
//Se importa el componente "Form"
import Form from './components/Form.vue'

export default {
  name: 'App',
  components: {
    //Se registra el componente "Form"
    Form
  }
}
</script>

<style>

</style>
