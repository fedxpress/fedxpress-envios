
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>FedXpress</title>
    <style>
        body {
            background-color: #6a0dad;
            color: white;
            font-family: Arial, sans-serif;
            text-align: center;
            margin: 0;
            padding: 0;
        }
        .container {
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            height: 100vh;
        }
        .logo {
            width: 200px;
            margin-bottom: 20px;
        }
        .codigo-form {
            margin-bottom: 20px;
        }
        input[type="text"] {
            padding: 10px;
            border-radius: 5px;
            border: none;
            margin-right: 10px;
        }
        button {
            padding: 10px 20px;
            border-radius: 5px;
            border: none;
            background-color: #ffffff;
            color: #6a0dad;
            font-weight: bold;
            cursor: pointer;
        }
        button:hover {
            background-color: #4c0280;
            color: white;
        }
        .mensaje {
            font-size: 18px;
        }
        .imagen {
            margin-top: 20px;
        }
    </style>
</head>
<body>
    <div class="container">
        <img src="avion.png" alt="Avion.png" class="logo">
        <form class="codigo-form">
            <input type="text" id="codigo" placeholder="Ingrese codigo">
            <button type="button" onclick="mostrarImagen()">Ingresar codigo</button>
        </form>
        <div class="mensaje" id="mensaje"></div>
        <img src="" alt="Entrega" class="imagen" id="imagen" style="display: none;">
    </div>

    <script>
        function mostrarImagen() {
            var codigo = document.getElementById("codigo").value;
            if (codigo === "3R0W0FLW0177") {
                document.getElementById("mensaje").style.display = "none";
                document.getElementById("imagen").src = "xcccc.png"; // Coloca aqui la ruta de la imagen de entrega
                document.getElementById("imagen").style.display = "block";
            } else {
                document.getElementById("mensaje").innerText = "El codigo ingresado no es valido. Por favor, intentelo de nuevo.";
            }
        }
    </script>
</body>
</html>
