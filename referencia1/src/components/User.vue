<template>
  <div>
      <h1>COMPONENTE DE USUARIO</h1>
      <ul>
          <li v-for="user in users">
              {{user.name}} - {{user.apellido}}  {{user.email}} <button v-on:click= "deleteUser">X</button>

          </li>
      </ul>

      <form v-on:submit.prevent="addUser(newUser)">
          <input type="text" v-model="newUser.name">
          <input type="text" v-model="newUser.apellido">
          <input type="email" v-model="newUser.email">
          <input type="submit">

      </form>
    

  </div>
</template>

<script>

export default {
    
    data(){
        return {
            users:[
                
            ],
            newUser : {
            },
        }

     

    },

    methods:{
            addUser(){
                
                this.users.push(this.newUser);
                this.newUser = {};
            
            },

            deleteUser(){
                this.users.splice(this.users.indexOf,1,)
            },
            
            
    },

    created(){
                console.log('cargando componente');
                this.$http.get('https://jsonplaceholder.typicode.com/users')
                .then(res => this.users = res.body)




            }

}
</script>

<style>

</style>