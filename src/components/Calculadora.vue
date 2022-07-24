<template>
  <div class="calculadora">
    <div class="display">25</div>
    <div class="botao operadores">C</div>
    <div  class="botao operadores">%</div>
    <div  class="botao operadores">÷</div>
    <div  class="botao operadores">x</div>


    <div  class="botao">7</div>
    <div  class="botao">8</div>
    <div  class="botao">9</div>
    <div  class="botao operadores">-</div>

    <div  class="botao">4</div>
    <div  class="botao">5</div>
    <div  class="botao">6</div>
    <div class="botao operadores">+</div>

    <div  class="botao">1</div>
    <div  class="botao">2</div>
    <div  class="botao">3</div>
    <div id="igual"  class="botao">=</div>

    <div class="botao">0</div>
    <div  class="botao">.</div>
    <div  class="botao"><img src="../assets/icons8-delete-32.png" alt=""></div>

  </div>
</template>

<script>
export default {};
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
  /* grid-column: 3 / 5; */
  /* grid-row: 3 / 5; */
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
