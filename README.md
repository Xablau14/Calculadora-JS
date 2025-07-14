# Calculadora
<!DOCTYPE html>
<html lang="pt-br">
<head>
  <meta charset="UTF-8"> 
<body>

  <h2>Calculadora Simples</h2>
  
  <div class="calculadora">
    <input type="text" id="resultado" readonly />
    <div class="botoes">
      <button onclick="adicionar('1')">1</button>
      <button onclick="adicionar('2')">2</button>
      <button onclick="adicionar('3')">3</button>
      <button class="operador" onclick="adicionar('+')">+</button>
      <div>
      </div>
      <button onclick="adicionar('4')">4</button>
      <button onclick="adicionar('5')">5</button>
      <button onclick="adicionar('6')">6</button>
      <button class="operador" onclick="adicionar('-')">-</button>
      <div> 
      </div>      
      <button onclick="adicionar('7')">7</button>
      <button onclick="adicionar('8')">8</button>
      <button onclick="adicionar('9')">9</button>
      <button class="operador" onclick="adicionar('*')">*</button>
      <div>
      </div>
      <button onclick="adicionar('0')">0</button>
      <button onclick="adicionar('.')">.</button>
      <button class="igual" onclick="calcular()">=</button>
      <button class="operador" onclick="adicionar('/')">/</button>
      <div> </div>
      <button class="limpar" onclick="limpar()">Limpar</button>
    </div>
  </div>
  
