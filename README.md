# Calculadora
Calculadora simples 
# Ambiente-de-teste
Ambiente de teste de codigos

<!DOCTYPE html>
<html lang="pt-br">
<head>
  <meta charset="UTF-8">
  <title>Calculadora Simples</title>
</head>
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

  <script>
    function adicionar(valor) {
      document.getElementById("resultado").value += valor;
    }

    function limpar() {
      document.getElementById("resultado").value = "";
    }

    function calcular() {
      try {
        const expressao = document.getElementById("resultado").value;
        const resultado = eval(expressao);
        document.getElementById("resultado").value = resultado;
      } catch {
        document.getElementById("resultado").value = "Erro";
      }
    }
  </script>
 <style>
   body {
  font-family: Arial, sans-serif;
  background: #f0f2f5;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  height: 100vh;
  margin: 0;
}

h2 {
  margin-bottom: 20px;
  color: #333;
}

.calculadora {
  background: #fff;
  padding: 20px 30px;
  border-radius: 15px;
  box-shadow: 0 0 20px rgba(255, 0, 157, 0.1);
}

input[type="text"] {
  width: 100%;
  height: 50px;
  font-size: 24px;
  text-align: right;
  margin-bottom: 20px;
  padding: 10px;
  border: none;
  border-radius: 10px;
  background-color:rgba(247, 242, 242, 0.9);
}

.botoes {
  display: grid;
  grid-template-columns: repeat(4, 60px);
  gap: 10px;
}

button {
  height: 60px;
  font-size: 20px;
  border: none;
  border-radius: 10px;
  background-color: #f4f4f4;
  cursor: pointer;
  transition: background 0.2s;
}

button:hover {
  background-color: #d4d4d4;
}

.operador {
  background-color: #ff9f43;
  color: white;
}

.operador:hover {
  background-color: #e67e22;
}

.igual {
  background-color: #1dd1a1;
  color: white;
}

.igual:hover {
  background-color: #10ac84;
}

.limpar {
  grid-column: span 4;
  background-color: #ee5253;
  color: white;
}
.limpar:hover {
  background-color: #c0392b;
}
  </style>
</body>
</html>
