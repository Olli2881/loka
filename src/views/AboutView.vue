<script setup>
import TheWelcome from '../components/TheWelcome.vue'
</script>

<style>

div{
  display: flex;
  justify-content: left;
  padding-left: 15px;
  width: auto;
}

.upp{
  display: flex;
  flex-direction: column;
  width: auto;
  padding: 15px;
  background-color: darkblue;
  border-radius: 20px;
  height: 100vh;
}

.name{
  display: flex;
  justify-content: center;
  color: darkblue;
  font-size: larger;
  background-color: gold;
}

.creator{
  color: gold;
  background-color: darkblue;
}

.info{
  display: flex;
  justify-content: center;
  color: gold;
  background-color: darkblue;
}

a{
  display: flex;
  padding-left: 10px;
  padding-right: 10px;
  color: darkblue;
}

</style>

<template>

  <div class="upp">

  <div class="name">
    <strong>
      Upplýsinga
    </strong>
  </div>

    <div class="info">
      Hérna er Upplýsinga síðan
    </div>

    <div>
      þessi síða er búin til þess að þú getur vitað hvenær myndir mundu vera sýna og hvar þau eru sínd.
    </div>

    <div>
      Þú getur ekki keypt miða á þessa síðu því miður
    </div>

    <div>
      þetta síða er einfalega bara að reyna að sína
    </div>

    <div>
      Hér getur þú fundið hvað Imdb þeirra eru sum myndir munu kannski ekki hafa imdb strax því þau komdu bara út rosa snemma
    </div>

    <div>
      Ef þið viljið panta miða eða fara á síðu með almenna upplýsinga þá væri gott að fara á þessa síður: <a href="https://www.sambio.is/">Sambíó</a>, <a href="https://laugarasbio.is/">Laugarás Bíó</a> og <a href="https://www.smarabio.is/">Smárabíó</a>
    </div>

    <div>
      Hér getur þú fundið hvaða myndir eru að fara koma seinna við þau bíósalar eða bara einfaldlega hérna eru Væntanlegt: <a href="https://www.sambio.is/ComingSoon"> Sambíó </a>, <a href="https://laugarasbio.is/vaentanlegt"> Laugarás Bíó </a> og <a href="https://bio.smarabio.is/coming-soon">Smárabíó</a>
    </div>

    <div>
      Hérna getur þú fundið um upplýsinga um síðurnar sjálfa: <a href="https://www.sambio.is/Upplysingar"> Sambíó </a> og <a href="https://laugarasbio.is/upplysingar/um-bioid"> Laugarás Bíó </a> fann ekki fyrir Smárabíó :(
    </div>

    <div class="creator">
      <strong>Frá Óli Viðar Sigurbjörnsson</strong>
    </div>

  </div>

</template>