<template class="no-scroll">
  <q-layout class="no-scroll" view="hHh lpR fff">
    <q-header>
      <div class="row shadow-24">
        <div class="col-4">
          <div class="bg-indigo-10 q-pb-md q-pt-md q-pl-xl no-scroll menu_principal flex" >
            <a @click="goHome()"><h2 class="flex flex-center"> <img class="q-mr-md" src="../assets/icon-joia_verde.png" alt="">Fique Positivo</h2></a>
          </div>
          <div class="linha_secundaria bg-indigo-5"></div>
        </div>
        <div class="col-8">
          <div class="row reverse bg-indigo-10 q-pb-md q-pt-md q-pl-xl no-scroll menu_principal items-end" >
            <a @click="goSobre()"><h4 class="text-right q-mr-xl"> Sobre </h4></a>
            <a @click="goGastos()"><h4 class="text-right q-mr-xl"> Meus gastos </h4></a>
          </div>
          <div class="linha_secundaria bg-indigo-5"></div>
        </div>
      </div>
    </q-header>
    <q-page-container class="bg-light-blue-1">
      <div class="row container_principal">
        <div class="col-1"></div>
        <div class="col-10 q-mt-lg q-pt-lg q-pl-lg q-pr-lg q-pb-lg q-mb-lg bg-white bordas">
          <RouterView></RouterView>
        </div>
        <div class="col-1"></div>
      </div>
    </q-page-container>
    <q-footer>
      <div class="bg-blue-grey-10 flex flex-center q-pb-md q-pt-md" >
        <h6 class="flex flex-center q-pr-md"> Desenvolvido por </h6>
        <div>
          <h5 class="flex flex-center"> Daniel Queiroz
            <a href="https://wa.me/5561991993893" target="_blank">
              <img src="../assets/icon-whatsapp.png" alt="Wpp">
            </a>
            <a href="https://www.linkedin.com/in/daniel-queiroz-79b37b1b9/" target="_blank">
              <img src="../assets/icon-linkedin.png" alt="in">
            </a>
            <a href="https://instagram.com/euodanielqueiroz?igshid=OGQ5ZDc2ODk2ZA%3D%3D&utm_source=qr" target="_blank">
              <img src="../assets/icon-instagram.png" alt="instagram">
            </a>
          </h5>
          <h5 class="flex flex-center"> Danilo Queiroz
            <a href="https://wa.me/5561995813460" target="_blank">
              <img src="../assets/icon-whatsapp.png" alt="Wpp">
            </a>
            <a href="https://www.linkedin.com/in/danilo-queiroz-a4923a230/" target="_blank">
              <img src="../assets/icon-linkedin.png" alt="in">
            </a>
            <a href="https://instagram.com/euodanielqueiroz?igshid=OGQ5ZDc2ODk2ZA%3D%3D&utm_source=qr" target="_blank">
              <img src="../assets/icon-instagram.png" alt="instagram">
            </a>
          </h5>
        </div>
      </div>
    </q-footer>
  </q-layout>
</template>

<script>
export default {
  methods: {
    goHome () {
      alert('vou implementar ainda a tela inicial')
    },
    goGastos () {
      this.$router.push('/meus-gastos')
    },
    goSobre () {
      this.$router.push('/sobre')
    }
  }
}
</script>
<style>
  *{
    margin: 0px;
  }
  .menu_principal{
    color: white;
    height: 95px;
  }
  .linha_secundaria{
    height: 10px;
  }
  .container_principal{
    min-height: 60em;
    width: 100%;
  }
  .bordas{
    border-radius: 20px;
  }
  .menu_lateral{
    width:10%
  }
  h2{
    font-family: Arial, Helvetica, sans-serif;
    font-weight: bold;
  }
  h4{
    font-family: Arial, Helvetica, sans-serif;
    font-size: xx-large;
  }
  img{
    width: 65px;
  }
  footer img{
    width: 30px;
    margin-left: 15px;
  }
  a{
    cursor: pointer;
  }
</style>
