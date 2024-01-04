<template>
    <div class="row justify-center bg-indigo-1 borda container_geral q-pt-lg q-pb-lg q-pl-lg q-pr-lg full-width full-height">
      <div class="col-9 text-left column flex justify-center">
        <h4 class="text-weight-bolder text-indigo-5">Daniel Pereira Mendes de Queiroz</h4>
          <p class="text-weight-bolder">Desenvolvedor de Software</p>
      </div>
      <div class="col-3 flex justify-end text-right ">
        <h5 class="text-weight-bolder text-green flex flex-center">R$: 16.800,00</h5>
      </div>
    </div>
</template>

<script>
export default {
  props: {
    idPessoa: {}
  }
}
</script>
<style scoped>
.borda{
  border-radius: 20px;
  height: 110px;
}
img{
  height: 150px;
  width: 150px;
  border-radius: 50%;
}
.container_geral{
  width: 800px;
  height: 130px;
}
div p{
  font-size: x-large;
}
</style>
