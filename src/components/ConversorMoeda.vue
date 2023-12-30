<template>
    <div class="conversor">
        <h2> {{ moedaA }} Para {{ moedaB }}</h2>
        <input type="text" v-model="moedaA_value" v-bind:placeholder="moedaA">
        <input type="button" value="Converter" v-on:click="converter" class="botao-converter">
        <h2> {{ moedaB_value }}</h2>
    </div>

</template>



<script>
export default { 
    name: "ConversorMoeda",
    props: ["moedaA", "moedaB"],
    data() {
        return{
            moedaA_value: "",
            moedaB_value: 0
        };
      },
      methods: {
        converter(){
            
            let apiKey = "5e496b3e16715e9dbaf6";
            let url =  `https://free.currconv.com/api/v7/convert?q=${this.moedaA}_${this.moedaB}&compact=ultra&apiKey=${apiKey}`;


        fetch(url).then(res => {

            res.json().then((resultado) => {
            
            this.taxaDeCambio = resultado[`${this.moedaA}_${this.moedaB}`];

            this.moedaB_value = (this.taxaDeCambio * parseFloat(this.moedaA_value)).toFixed(2);
            });

        })
        }
      }
};
</script>

<style scoped>

.conversor {
    padding: 20px;
    max-width: 300px;
    box-shadow: 0 5px  8px 0 #000000;
    background-color: #8d8d8d;

}

.botao-converter:hover {
    background-color: #efbf75; 
}

</style>