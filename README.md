# atividades-lsw
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
   <div class="area">
    <div class="container">
        <h1>Calculador de IMC</h1>
        <div class="input_area">
            <h2>Altura (cm) </h2>
            <input id="height" type="number">
        </div>
        <div class="input_area">
            <h2>Peso (kg) </h2>
            <input id="weight" type="number">
        </div>
        <button onclick="calculate()">Calcular</button>
        <textarea name="" id="text_area" rows="6"></textarea>
        </div>
       
    </div>  
    <script src="index.js"></script>
</body>
</html>

------------------------------------------------------------------------------
javascript

function calculate() {
    var height = document.getElementById("height").value / 100;
    var weight = document.getElementById("weight").value;
  
    var imc = weight / height ** 2;
    var text=""
    if (imc < 18.5) {
      text="Você está magro"
    } else if (imc < 24.9) {
      text="Você está normal"
    } else if (imc < 29.9) {
      text="Você está com sobrepeso"
    } else if (imc < 39.9) {
      text="Você está com obesidade"
    } else if (imc > 39.9) {
      text="Você está com obesidade mórbida"
    }
    document.getElementById("text_area").innerText=text
  }
  
  ---------------------------------------------------------
  
  css
  h2{
    color: #D4D4D2;
}h1{
    margin-block-start: 0em; 
    color: white;
}
.input_area{
    width: 100%;
    display: flex;
    align-items: center;
    justify-content: space-between;
}
input{
    height: 1.5em;
}
textarea{
    width: 100%;
    margin-top: 2em;
}
.container{
    background-color: #1C1C1C;
    display: inline-flex;
    padding: 1.5em;
    border-radius: 0.5em;
    flex-direction: column;
    align-items: center;
    width: 20em;
}

.area{
    display: flex;
    justify-content: center;
}

button{
    height: 3em;
    width: 100%;
    background-color: #FF9500;
    border: none;
    color: white;
}
button:hover{
    cursor: pointer;
}
