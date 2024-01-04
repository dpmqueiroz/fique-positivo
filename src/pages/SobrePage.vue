<template>
  <div class="row">
    <div class="q-mt-lg col text-center">
      <div>
        <h2 class="q-mb-md text-indigo-5">Sobre</h2>
      </div>
      <p><span>SURGIMENTO </span>: Surgiu no dia 1º de Dezembro de 2023 com intuito de alertar e monitorar as pessoas sobre o quanto estão gastando, e também sugerir modelos de organizar finanças.</p>
      <p><span>FINALIDADE </span>: Ajudar as pessoas a monitorar os seus gastos e atingir a meta ficando positivo no fim do mês.</p>
      <p><span>MISSÃO </span>: Ajudar na educação financeira dos usuários.</p>
      <div class="row inline q-mt-xl" id="boneco">
        <div class="col-6">
          <img src="../assets/boneco-grafico.png" alt="Grafico">
        </div>
        <div class="col-6 text-right">
          <p>"Se não controla o seu dinheiro não pode reclamar do resultado."</p>
          <h6>Daniel Queiroz</h6>
        </div>
      </div>
    </div>
    <div class="q-mt-lg col text-center">
      <div>
        <h2 class="q-mb-lg text-indigo-5">Idealizadores</h2>
      </div>
      <CardIdealizador :nome="'Daniel Queiroz'" :funcao="'Desenvolvedor Full-Stack responsável pelo FRONT-END da aplicação.'" :urlFoto="'https://media.licdn.com/dms/image/C4D03AQFftiJOwVZ_og/profile-displayphoto-shrink_800_800/0/1663848690740?e=1706745600&v=beta&t=OubVfeDMGp56cITErnneJq0XSwwlqZFWA_QArylMx10'"></CardIdealizador>
      <CardIdealizador :nome="'Danilo Queiroz'" :funcao="'Desenvolvedor Back-End responsável pelo BACK-END da aplicação. '" :urlFoto="'https://avatars.githubusercontent.com/u/147623397?v=4'"></CardIdealizador>
      <CardIdealizador :nome="'Sheron Queiroz'" :funcao="'UI/UX responsável pela aplicação.'" :urlFoto="'https://media.licdn.com/dms/image/C4D03AQGB_w4vgDsiAg/profile-displayphoto-shrink_800_800/0/1658693750249?e=1706745600&v=beta&t=fkWB_JCP2ufM9887zAzJfAR1NR-cXSvYiasJndVEtEI'"></CardIdealizador>
    </div>
  </div>
</template>

<script>
import CardIdealizador from '../components/CardIdealizadores.vue'
export default {
  components: {
    CardIdealizador
  }
}
</script>
<style scoped>
  img{
    width: 50%;
    border-radius: 50%;
  }
  p{
    font-family: Arial, Helvetica, sans-serif;
    font-size: x-large;
    text-align: justify;
    margin-bottom: 30px;
  }
  span{
    font-family: Arial, Helvetica, sans-serif;
    font-weight: bolder;
    font-size: x-large;
  }
  h2{
    font-weight: bolder;
  }
  #boneco img{
    width: 50%;
  }
  #boneco p{
    font-size: xx-large;
    font-weight: bolder;
    font-family: Arial, Helvetica, sans-serif;
  }
</style>
