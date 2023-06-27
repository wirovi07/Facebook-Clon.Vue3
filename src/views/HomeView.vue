<template>

  <div class="home">
    <div class="row mx-0">

      <div class="col-lg-6">
        <div class="img-cont">
          <img alt="Vue logo" class="logo" src="../assets/img/facebook.svg" />
          <h2 class="text-center text-lg-start">
            Conéctate con amigos y el resto del mundo usando Facebook
          </h2>
        </div>
      </div>
      
      <div class="col-lg-6">
        <card-comp :btns="btnArray" class="mx-auto card-comp">

          <template #default>
            <form action="">
              <div class="mb-3 mt-2">
                <input type="email" class="form-control" placeholder="Ingresa tu Email">
              </div>
              <div class="mb-3 mt-2">
                <input type="password" class="form-control" placeholder="Contraseña">
              </div>            
            </form>    
          </template>

          <template #footer>
            <hr/>
            <button class="btn btn-success">
              Crear una cuenta
            </button>
          </template>
          
        </card-comp>
      </div>

    </div>   
  </div> 

</template>

<script>

import CardComp from '../components/CardComp.vue';

  export default {
    name: 'HomeView',
    components: {
      CardComp
    },    
    data(){
      return {
        btnArray: [
          {
            txt: 'Iniciar sesíon',
            class: 'btn-primary',
          },
          {
            txt: 'Olvídaste tu contraseña?',
            class: '',
          },
        ],
      }
    },
  }  

</script>

<style scoped>
  .home{
  max-width: 895px;
  margin: auto;
  }
  h2{
    max-width: 470px;
    margin: auto;
    font-size: 1.8rem;  
    margin-bottom: 1em;
  } 
  .img-cont{
    display: flex;
    flex-direction: column;
  }
  img{
    max-width: 315px;
    margin: 1em auto 0 auto;
  }
  .card-comp{
    max-width: 398px;
  }

.btn-success{
  margin: auto;
  min-width: 195px;
}

  @media (min-width: 992px) {
    .home{
      margin: 4em auto;
    }
    img {
      margin: 0;
      margin-top: 5.6em;
    }
    h2{
      margin: 0;
      margin-top: -0.8em;
      margin-left: 0.8em;
    }
    .card-comp{
      margin-top: 3rem;
    }
  
  }

</style>
