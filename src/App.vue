<template>
  <div id="app">
    <h1 class="titulo">Conversor de moedas</h1>

    <div class="linha">
    <ConversorMoeda moedaA="USD" moedaB="BRL"/>
    <ConversorMoeda moedaA="BRL" moedaB="USD"/>
    </div>

    <div class="linha">
    <ConversorMoeda moedaA="EUR" moedaB="BRL"/>
    <ConversorMoeda moedaA="BRL" moedaB="EUR"/>
    </div>

    <div class="linha">
    <ConversorMoeda moedaA="BTC" moedaB="BRL"/>
    <ConversorMoeda moedaA="BRL" moedaB="BTC"/>
    </div>

    <div class="linha">
    <ConversorMoeda moedaA="CAD" moedaB="BRL"/>
    <ConversorMoeda moedaA="BRL" moedaB="CAD"/>
    </div>

    <div class="linha">
    <ConversorMoeda moedaA="GBP" moedaB="BRL"/>
    <ConversorMoeda moedaA="BRL" moedaB="GBP"/>
    </div>

    <div class="linha">
    <ConversorMoeda moedaA="CHF" moedaB="BRL"/>
    <ConversorMoeda moedaA="BRL" moedaB="CHF"/>
    </div>

    <div class="linha">
    <ConversorMoeda moedaA="TRY" moedaB="BRL"/>
    <ConversorMoeda moedaA="BRL" moedaB="TRY"/>
    </div>

    <div class="linha">
    <ConversorMoeda moedaA="CNY" moedaB="BRL"/>
    <ConversorMoeda moedaA="BRL" moedaB="CNY"/>
    </div>
  </div>
</template>

<script>
import ConversorMoeda from "./components/ConversorMoeda.vue";

export default {
  name: "app",
  components: {
    ConversorMoeda
  }
  };
</script>

<style>
#app {
  margin: auto;
  max-width: 900px;
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #000000;
  margin-top: 60px;
  font-weight: 700;
}

body {
  background-image: url('./assets/fundo.jpg');
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}

.titulo {
  font-size: 50px;
  color: #000000;
  text-shadow: 2px 2px 4px #704C2D;
  padding-bottom: 70px;
  font-weight: bold;
  text-align: center;
}

.linha {
  margin-top: 40px;
  display: flex;
  justify-content: space-around;
  padding: 30px;
  padding-left: 80px;
  width: 100%;
  border-radius: 5px;
  transition: transform 0.5s ease-in-out;
  padding-right: 20px;
}

.linha:hover {
  transform: scale(1.1);
}

.linha > * {
  margin-right: 100px;
  width: 48%;
}


@media (max-width: 768px) {
  .linha {
    flex-direction: column;
    padding-left: 110px;
}

  .linha > * {
    margin-bottom: 10px;  
}

.titulo {
  font-size: 30px;
  text-align: center;
  padding-left: 20px;
}

}

</style>
