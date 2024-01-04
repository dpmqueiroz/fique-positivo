<template>
  <div class="text-center">
    <h2 class="q-mb-md text-indigo-5">Gerencie seus gastos</h2>
  </div>
  <div class="row">
    <div class="col-6">
      <CardPessoa></CardPessoa>
    </div>
    <div id="dados-pessoa" class="row justify-end col-6">
      <div class="col-5">
        <CardGastoIdeal :salario="this.salario"></CardGastoIdeal>
      </div>
      <div class="col-5">
        <CardGastoAtual/>
      </div>
      <div class="col-2" id="selo-qualidade" @click="modalSeloQualidade = true">
        <div class="bg-indigo-1 borda full-height q-ml-sm flex flex-center">
          <img src="../assets/icon-joia_verde.png" class="full-width" alt="OK">
        </div>
      </div>
    </div>
  </div>
  <div>
    <GridGastos :id=2></GridGastos>
  </div>
  <q-dialog v-model="modalSeloQualidade">
    <DialogSeloQualidade></DialogSeloQualidade>
  </q-dialog>

</template>

<script>
import { ref } from 'vue'
import CardPessoa from '../components/CardPessoa.vue'
import CardGastoIdeal from '../components/CardGastoIdeal.vue'
import CardGastoAtual from '../components/CardGastoAtual.vue'
import DialogSeloQualidade from '../components/Dialog/DialogSeloQualidade.vue'
import GridGastos from '../components/GridGastos.vue'
import axios from 'axios'
export default {
  data () {
    return {
      modalSeloQualidade: ref(false),
      salario: 16800,
      gastos: ref(null)
    }
  },
  mounted () {
    this.buscarCep()
  },
  methods: {
    buscarCep () {
      axios.get('http://localhost:3000/pessoa.id=2')
        .then((res) => {
          this.gastos = res.data
          console.log(res)
        }).catch((error) => {
          console.log(error)
        })
    }
  },
  components: {
    CardPessoa,
    CardGastoIdeal,
    CardGastoAtual,
    DialogSeloQualidade,
    GridGastos
  }
}
</script>
<style scoped>
  .dados-pessoa{
    height: 200px;
  }
  h2{
    font-weight: bolder;
  }
  #selo-qualidade{
    cursor: pointer;
  }
</style>
