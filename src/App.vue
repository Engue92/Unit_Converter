<template>
  <div class="app">
    <div class="container">

      <div class="row">
        <p class="meusur">Conversion unit : <input type="text" v-model="meusur1"/> , <input type="text" v-model="meusur2"/></p>
      </div>

      <div class="row" v-if="meusur1 != '' && meusur2 != ''">
        <p class="taux">Multiplier base : 1 {{ meusur1 }} = <input type="text" v-model="taux"/> {{ meusur2 }}</p>
      </div>

      <div class="row" v-if="taux != ''">
        <p class="conversion"><input type="text" v-model="valeur1"/> {{meusur1}} = {{valeur1 * taux}} {{meusur2}} </p>
      </div>

    </div>
  </div>
</template>
  
  
<script>
  export default 
  {
    data() {
      return {
        meusur1: "",
        meusur2: "",
        valeur1: "",
        taux: "",
      }
    },
  }
</script>
  
<style>
  body {
    background-color: silver;
    font-family: Calibri, Arial, Helvetica, sans-serif;
    font-size: x-large;
    text-align: center;
    margin-top: 200px;
  }
</style>
