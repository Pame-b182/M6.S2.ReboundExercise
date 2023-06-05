<template>
<div class="col col-md-6 m-3 p-3 mx-auto">
    <div class="form-floating mb-3">
        <input type="text" class="form-control" id="inputNombre" placeholder="Ingrese su nombre" v-model="nombre"/>
        <label for="inputNombre">Nombre</label>
    </div>
    <div class="form-floating mb-3">
        <input type="text" class="form-control" id="inputApellido" placeholder="Ingrese su apellido" v-model="apellido"/>
        <label for="inputApellido">Apellido</label>
    </div>
    <div class="form-floating mb-3">
        <input type="email" class="form-control" id="inputCorreo" placeholder="name@example.com" v-model="correo"/>
        <label for="inputCorreo">Correo</label>
    </div>
    <div class="form-floating mb-3">
        <input type="number" class="form-control" id="inputEdad" placeholder="Ingrese su edad" v-model="edad"/>
        <label for="inputEdad">Edad</label>
    </div>
    <div class="d-grid gap-2 col-6 mx-auto m-4">
        <button class="btn btn-primary" type="button" @click.prevent = "registrar">Registrar</button>
    </div>
    <div class="text-center border rounded" v-if="edad>0 && edad<14 ">
        Usted está en la etapa Niñez
    </div>
        <div class="text-center border rounded" v-if="edad>=14 && edad<18 ">
        Usted está en la etapa Adolescencia
    </div>
    <div class="text-center border rounded" v-if="edad>=18 && edad<36 ">
        Usted está en la etapa Adulto Joven
    </div>
    <div class="text-center border rounded" v-if="edad>=36 && edad<65 ">
        Usted está en la etapa Adulto
    </div>
    <div class="text-center border rounded" v-if="edad>=65">
        Usted está en la etapa Tercera edad
    </div>
</div>
</template>

<script>
export default {
  name: "component-name",
  // props: {},
  data: function () {
    return {
        //Se crean los datos a utilizar.
        nombre: '',
        apellido: '',
        correo: '',
        edad: '',
    };
  },
  // computed: {},
  methods: {
    //Método registrar que muestra una alerta con los datos de "data"
    registrar(){
        alert(`Saludos ${this.nombre} ${this.apellido} tu correo es ${this.correo}`)
        //luego que se muestra la alerta, se limpian los input.
        this.nombre='',
        this.apellido='',
        this.correo='',
        this.edad=''
    }
  }
  // watch: {},
  // components: {},
  // mixins: [],
  // filters: {},
  // -- Lifecycle Methods
  // -- End Lifecycle Methods
};
</script>

<style scoped>
</style>