<template>
<div class="container" id="login">

    <br>
    <h1>INGRESAR</h1>
    <form action="" class="form-group" method="post">
                <br>
				  <input type="email" class="form-control" name="correo" placeholder="Correo" id="Correo"  required>
				<br>
				  <input type="password" name="contra" class="form-control" placeholder="******"  required>
				<br>
				<button class="btn btn-lg btn-primary btn-block btn-signin" type="submit">Entrar</button>
				<div>
        <br>
          <a href="">Olvidaste tu contraseña?</a>
        </div>
	</form>
</div>
</template>

<script>
export default {
    name:"Login",
    data (){
        return{
            users:[
                
            ]
        }
    },

}
</script>

<style>
#login{
  margin-left: auto;
  margin-right: auto;
  width: 40%;
}


</style>