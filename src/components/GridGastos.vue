<template>
  <div class="row q-mt-md">
    <div class="col-11 bg-indigo-1 borda text-center">
      <h2 class="q-mb-xs q-mt-xs text-indigo-5">Gastos</h2>
    </div>
    <div class="col-1 flex flex-center">
      <q-icon id="pointer" name="add" size="xl" class="bg-green borda pointer shadow-8"></q-icon>
    </div>
  </div>
  <div class="row q-mt-lg ">
    <div class="col-12 bg-indigo-1 borda">
      <q-table
        class="borda"
        bordered
        no-data-label="Não temos nenhum gasto cadastrado para essa pessoa"
        rows-per-page-label="Quantidade de registros por página"
        :rows-per-page-options="[7, 15]"
        :columns="columns"
        :rows="rows"
        row-key="name"
        table-header-class="bg-indigo-2"
      />
    </div>
  </div>
</template>
<script>
import axios from 'axios'
import { ref } from 'vue'
export default {
  inject: {
    $f: {
      from: '@text-formatters'
    }
  },
  props: {
    id: {}
  },
  data () {
    return {
      columns: [
        { name: 'data', align: 'center', label: 'Data', field: 'data', sortable: true },
        { name: 'desc', align: 'center', label: 'Descrição', field: 'descricao', sortable: false },
        { name: 'categoria', align: 'center', label: 'Categoria', field: 'categoria', sortable: true },
        { name: 'necessario', align: 'center', label: 'necessário', field: 'necessidade', sortable: true },
        { name: 'valor', align: 'center', label: 'Valor', field: val => 'R$: ' + val.valor.toFixed(2), sortable: true },
        { name: 'acoes', align: 'center', label: 'Ações', field: 'acoes', sortable: false }
      ],
      rows: ref.null
    }
  },
  mounted () {
    this.buscarGastosDaPessoa()
  },
  methods: {
    buscarGastosDaPessoa () {
      axios.get('http://localhost:3000/gastos?pessoa.id=' + this.id)
        .then((res) => {
          this.gastos = res.data
          this.rows = res.data
          console.log(res)
        }).catch((error) => {
          console.log(error)
        })
    }
  }
}
</script>
<style scoped>
  #pointer:hover{
    width: 55px;
    height: 55px;
  }
</style>
