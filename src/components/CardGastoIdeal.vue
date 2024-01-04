<template>
  <div class="bg-indigo-1 borda full-height q-ml-sm q-pb-md">
    <h6 class="text-center text-indigo-5 q-pt-md q-pb-xm">Ideal</h6>
    <div class="text-center row">
        <div class="col-6 text-left">
          <p><q-icon @Click="modalGastoFixo = true" id="pointer" name="info" size="sm"></q-icon> Fixo:</p>
          <p><q-icon @Click="modalGastoVariavel = true" id="pointer" name="info" size="sm"></q-icon> Variável:</p>
          <p><q-icon @Click="modalGastoInvestimento = true" id="pointer" name="info" size="sm"></q-icon> Investimento:</p>
        </div>
        <div class="col-6">
          <p> R$ {{ gastoFixo }}</p>
          <p> R$ {{ gastoVariavel }}</p>
          <p> R$ {{ gastoInvestimento }}</p>
        </div>
    </div>
  </div>
  <q-dialog v-model="modalGastoFixo">
    <DialogCategoria :titulo="'Gasto Fixo'" :mensagem="'Fixo são contas que você paga de maneira recorrente, mensalmente, como por exemplo água, energia, aluguel entre outros'"></DialogCategoria>
  </q-dialog>
  <q-dialog v-model="modalGastoVariavel">
    <DialogCategoria :titulo="'Gasto Variável'" :mensagem="'O Gasto variável são os gastos que temos no nosso dia a dia, um jantar em um restaurante, um jogo novo para o video-game, ou algo do tipo.'"></DialogCategoria>
  </q-dialog>
  <q-dialog v-model="modalGastoInvestimento">
    <DialogCategoria :titulo="'Gasto com Investimento'" :mensagem="'Em investimento antes de começar precisamos entender que temos três níveis que devem ser seguidos. Em primeiro lugar o investimento é limpar o seu nome caso esteja sujo. Em segundo lugar é criar uma RESERVA de EMERGÊNCIA caso não tenha. Em ultimo lugar mas não menos importante é simplesmente investir em algo que te traga lucro.'"></DialogCategoria>
  </q-dialog>
</template>

<script>
import DialogCategoria from '../components/Dialog/DialogCategoriaGasto.vue'
export default {
  data () {
    return {
      gastoFixo: null,
      gastoVariavel: null,
      gastoInvestimento: null,
      modalGastoFixo: false,
      modalGastoVariavel: false,
      modalGastoInvestimento: false
    }
  },
  props: {
    salario: {}
  },
  mounted () {
    this.gastoFixo = (this.salario * 0.50).toFixed(2)
    this.gastoVariavel = (this.salario * 0.30).toFixed(2)
    this.gastoInvestimento = (this.salario * 0.20).toFixed(2)
  },
  components: {
    DialogCategoria
  }
}
</script>
<style scoped>
.borda{
  border-radius: 20px;
}
p{
  margin-bottom: 5px;
  margin-left: 25px;
  font-weight: bold;
  font-size: medium;
}
h6{
  font-weight: bolder;
}
#pointer{
  cursor: pointer;
}
</style>
