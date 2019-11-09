<!DOCTYPE html>
<html lang="pt-br" dir="ltr">
  <head>
    <meta charset="utf-8">
    <title>Estudo do Js</title>
  </head>
  <body>

<form>
  <p>
    <label> Valor do Condomínio</label>
    <input type="text" id="condominio" >
  </p>
    <button type="button" id="calcular">Calcular</button>

<p id="m1"></p>
<p id="m2"></p>
<p id="m3"></p>
<p id="m4"></p>
</form>




<script type="text/javascript" src="./js/estudo02.js"></script>
  </body>


</html>
----JS----
//Pegar o botão
let btn = document.querySelector("#calcular")

//Fazer a função do condominio
btn.addEventListener("click",total)

function total() {

let valorCondominio = document.querySelector("#condominio").value
let fundoDeReserva = (5 * valorCondominio)/10
let benfeitorias =  (7* valorCondominio)/10
let taxaDeAdministracao = (15 * valorCondominio)/10
let somadetudo = fundoDeReserva + benfeitorias + taxaDeAdministracao + valorCondominio

document.querySelector("#m1").textContent = " Valor Total " + somadetudo
document.querySelector("#m2").textContent = " Valor Fundo de Reserva " + fundoDeReserva
document.querySelector("#m3").textContent = " Valor Benfeitorias " + benfeitorias
document.querySelector("#m4").textContent = " Valor Taxa de Administração " + taxaDeAdministracao

}
