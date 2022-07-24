<template>
  <div class="calculadora">
    <div class="display">{{valorCorrente || '0'}}</div>
    <div @click="limpar" class="botao operadores">C</div>
    <div  v-on:click="porcentagem" class="botao operadores">%</div>
    <div  class="botao operadores">÷</div>
    <div  class="botao operadores">x</div>


    <div v-on:click="JuntarNumeros('7')"  class="botao">7</div>
    <div v-on:click="JuntarNumeros('8')"  class="botao">8</div>
    <div v-on:click="JuntarNumeros('9')"  class="botao">9</div>
    <div  class="botao operadores">-</div>

    <div v-on:click="JuntarNumeros('4')"  class="botao">4</div>
    <div v-on:click="JuntarNumeros('5')"  class="botao">5</div>
    <div v-on:click="JuntarNumeros('6')"  class="botao">6</div>
    <div class="botao operadores">+</div>

    <div v-on:click="JuntarNumeros('1')"  class="botao">1</div>
    <div v-on:click="JuntarNumeros('2')"  class="botao">2</div>
    <div v-on:click="JuntarNumeros('3')"  class="botao">3</div>
    <div id="igual"  class="botao">=</div>

    <div v-on:click="JuntarNumeros('0')" class="botao">0</div>
    <div  class="botao">.</div>
    <div  class="botao"><img src="../assets/icons8-delete-32.png" alt=""></div>

  </div>
</template>

<script>
export default {
  data() {
    return {
      valorCorrente: '123',
      operadorclicado: false,
    };
  },
  methods: {
    limpar() {
      this.valorCorrente = '';
    },
    // método responsável por guardar os numeros no visor
    JuntarNumeros(numero) {
      if (this.operadorclicado) {
        this.valorCorrente = '';
        this.operadorclicado = false;
      }
      this.valorCorrente = `${this.valorCorrente}${numero}`;
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.calculadora {
  width: 400px;
  height: 600px;
  margin: 50px auto;
  font-size: 40px;
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  grid-auto-rows: minmax(50px, auto);
  background-color: #333A58;
  border: 3px solid #333A58;
}
.display{
  /*para especificar em qual coluna colocar um item e quantas colunas o item abrangerá.*/
  grid-column: 1 / 5;
  background-color: #333A58;
  color: #fff;
  margin:auto;
  font-size: 60px;
  height: 130px;
  padding-top: 50px;

}
#igual{
  grid-row: span 2;
  padding-top:75px;
  background-color: #FF3764;
  color: #fff;
}
.botao{
  background-color: #3B3F5D;
  color: #fff;
  border: 3px solid #333A58;
  padding-top: 20px;
  transition-property: background-color;
transition: #333A58 2s ease 100s;
}
.botao:hover ,#igual:hover{
background-color:#3c4467;
  cursor: pointer;
}
#igual:hover{
background-color:#fa5579;
  cursor: pointer;
}
.operadores{
  background-color: #50556E;
  color: #FF3764;
}
</style>
