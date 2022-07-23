<template>
  <div class="calculadora">
    <div class="display">25</div>
    <div class="botao operadores">C</div>
    <div  class="botao operadores">+/-</div>
    <div  class="botao operadores">%</div>
    <div  class="botao operadores">÷</div>
    <div  class="botao">7</div>
    <div  class="botao">8</div>
    <div  class="botao">9</div>
    <div  class="botao operadores">x</div>
    <div  class="botao">4</div>
    <div  class="botao">5</div>
    <div  class="botao">6</div>
    <div  class="botao operadores">-</div>
    <div  class="botao">1</div>
    <div  class="botao">2</div>
    <div  class="botao">3</div>
    <div class="botao operadores">+</div>
    <div class="botao zero">0</div>
    <div  class="botao operadores">.</div>
    <div  class="botao operadores">=</div>
  </div>
</template>

<script>
export default {};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.calculadora {
  font-size: 40px;
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  grid-auto-rows: minmax(50px, auto);
}
.display{
  /*para especificar em qual coluna colocar um item e quantas colunas o item abrangerá.*/
  grid-column: 1 / 5;
  background-color: #333;
  opacity: 0.6;
  color: #fff;
}
.zero{
  grid-column: 1 / 3;
}
.botao{
  background-color: #111;
  opacity: 0.4;
  color: #fff;
  border: 2px solid #333;
}
.operadores{
  background-color: rgb(143, 55, 55);
}
</style>
