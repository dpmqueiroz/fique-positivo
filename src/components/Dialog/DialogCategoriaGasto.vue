<template>
  <q-card style="width: 200; height: 38vh; border-radius: 20px;">
    <q-card-section>
      <h3 class="q-mb-md q-mt-lg text-indigo-5 text-center">{{ titulo }}</h3>
    </q-card-section>

    <q-card-section class="row justify-center q-pt-none">
      <p>{{ mensagem }}</p>
    </q-card-section>

    <q-card-actions :align="'right'" class="bg-white text-teal absolute-bottom q-mb-md q-mr-md">
      <q-btn color="indigo-5" label="OK" v-close-popup />
    </q-card-actions>
  </q-card>
</template>
<script>
export default {
  props: {
    titulo: {},
    mensagem: {}
  }
}
</script>
<style scoped>
h3{
  font-weight: bolder;
}
</style>
