<template>
  <div class="row justify-center borda">
    <div class="bg-indigo-1 flex flex-center q-pt-lg q-pb-lg q-pr-xl q-pl-xl q-mb-md borda container_geral">
      <img class="q-mr-lg" :src="urlFoto" :alt="nome">
      <div class="text-left container_nome_funcao">
        <h5>{{ nome }}</h5>
        <div>
          <p>{{ funcao }}</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    nome: {},
    funcao: {},
    urlFoto: {}
  }
}
</script>
<style scoped>
.borda{
  border-radius: 20px;
}
img{
  height: 150px;
  width: 150px;
  border-radius: 50%;
}
.container_nome_funcao{
  width: 65%;
}
.container_geral{
  width: 600px;
}
div p{
  font-size: large;
}
p{
  font-weight: bolder;
}
</style>
