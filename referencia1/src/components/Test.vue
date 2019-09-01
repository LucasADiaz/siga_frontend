<template>
    
   
  <!--   <div v-if="mostrarNombre">
        <p>
            {{user.primerNombre}}
        </p>
    </div>

    <div v-else>
        <p>
            no puedo mostrar nombre
        </p>
    </div> -->


  <!--   <div>
          <input type="text" v-model="user.primerNombre"> 
          <button type="button" v-on:click="saludar(user.primerNombre)">
            TOCAME
          </button>
    </div> -->
    

   <!--  <div>
      <input type="text" v-on:keyup="tipeando">
    </div> -->


    <!-- <div>
     
      {{nombreCompleto()}}
      <hr>

    </div> -->
    <div>
        <h1>msj por defecto en test </h1>
    </div>
</template>

<script>
export default {

  name: 'Test',
  data () {
    return  {
      msj: 'Hola soy componente',
      user: {
          primerNombre: 'juan',
          segundoNombre: 'daneri',
      },

      myhtml : '<h3>Holahola123</h3>',
      mostrarNombre: false,

    }
  },

  methods: {
    saludar(nombre){
      alert("hola " + nombre)
    },
    tipeando(e){
      console.log(e.key);
      if(e.key=="Enter")
        alert("no toques enter");
    },

  },

  computed: {
      nombreCompleto(){
        return this.user.primerNombre + ' ' + this.user.segundoNombre;
      },
  },

  props:{
    msg:{
      type:String

    }
  }
  
}
</script>

<style>
.test{
  background-color: blueviolet;
}

</style>