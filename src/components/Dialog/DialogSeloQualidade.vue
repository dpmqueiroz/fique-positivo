<template>
      <q-card style="width: 750px; max-width: 82vw; height: 38vh; border-radius: 20px;">
        <q-card-section>
          <h2 class="q-mb-md text-indigo-5 text-center">Selo de Qualidade</h2>
        </q-card-section>

        <q-card-section class="row justify-center q-pt-none">
          <div class="col-4 text-center bg-indigo-2 borda q-mr-sm q-pt-md" style="width: 32%;">
            <img src="../../assets/icon-joia_verde.png" alt="OK" class="q-mb-sm">
            <div class="col-12">
              Significa que você está muito bem, ponderando suas dívidas e investindo o seu dinheiro.
            </div>
          </div>
          <div class="col-4 text-center bg-indigo-2 borda q-mr-sm  q-pt-md" style="width: 32%;">
            <img src="../../assets/icon-joia-azul.png" alt="OK" class="q-mb-sm">
            <div class="col-12">
              Significa que você está no caminho certo, pois não está devendo mais do que está ganhando porém não está investindo.
            </div>
          </div>
          <div class="col-4 text-center bg-indigo-2 borda q-mr-sm  q-pt-md" style="width: 32%;">
            <img src="../../assets/icon-joia_vermelha.png" alt="OK" class="q-mb-sm">
            <div class="col-12">
              Significa que você está não está bem, tem mais dívidas do que deveria ter com o seu salário atual.
            </div>
          </div>
        </q-card-section>

        <q-card-actions :align="'right'" class="bg-white text-teal absolute-bottom q-mb-md q-mr-md">
          <q-btn color="indigo-5" label="OK" v-close-popup />
        </q-card-actions>
      </q-card>
</template>
<script>
export default {
}
</script>
<style scoped>
</style>
