<template>
  <div class="bg-indigo-1 borda full-height q-ml-sm">
    <h6 class="text-center text-indigo-5 q-pt-md q-pb-xm">Atual</h6>
    <div class="row">
      <div class="col-5 text-left">
        <p class="q-ml-md">Fixo :</p>
        <p class="q-ml-md">Variável :</p>
        <p class="q-ml-md">Investimento :</p>
      </div>
      <div class="col-4 text-left">
        <p>R$ 16.400,00</p>
        <p>R$ 8.100,00</p>
        <p>R$ 500,000</p>
      </div>
      <div class="col-3 text-left">
        <p>50%</p>
        <p>30%</p>
        <p>20%</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    salario: {},
    gastos: [{}]
  }
}
</script>
<style>
.borda{
  border-radius: 20px;
}
p{
  margin-bottom: 5px;
  font-weight: bold;
  font-size: medium;
}
h6{
  font-weight: bolder;
}
</style>
