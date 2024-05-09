<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Verificador de Situação</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            margin: 20px;
        }

        #result {
            margin-top: 20px;
            font-weight: bold;
        }
    </style>
</head>
<body>
    <h1>Verificador de Situação</h1>

    <label for="nota1">Nota 1:</label>
    <input type="number" id="nota1" required><br>
    <bb>

    <label for="nota2">Nota 2:</label>
    <input type="number" id="nota2" required><br>
      <bb>
    <label for="nota3">Nota 3:</label>
    <input type="number" id="nota3" required><br>
       <bb>
    <label for="nota4">Nota 4:</label>
    <input type="number" id="nota4" required><br>
      <bb>-
    <button onclick="calcularMedia()">Calcular Média</button>
          <bb>
    <div id="result"></div>

    <script>
        function calcularMedia() {
            var nota1 = parseFloat(document.getElementById("nota1").value);
            var nota2 = parseFloat(document.getElementById("nota2").value);
            var nota3 = parseFloat(document.getElementById("nota3").value);
            var nota4 = parseFloat(document.getElementById("nota4").value);

            var media = (nota1 + nota2 + nota3 + nota4) / 4;

            var resultadoElement = document.getElementById("result");
            if (!isNaN(media)) {
                if (media >= 7) {
                    resultadoElement.textContent = "Média: " + media.toFixed(2) + " - Aprovado";
                } else {
                    resultadoElement.textContent = "Média: " + media.toFixed(2) + " - Reprovado";
                }
            } else {
                resultadoElement.textContent = "Por favor, insira valores válidos para as notas.";
            }
        }
    </script>
</body>
</html>

