<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Invitación - Margarita 80 Años</title>
    <style>
        body {
            font-family: 'Georgia', serif;
            text-align: center;
            background-color: #f8e1e7;
            color: #600020;
        }
        .container {
            max-width: 600px;
            margin: 50px auto;
            padding: 20px;
            background: #fff;
            border-radius: 10px;
            box-shadow: 0 0 15px rgba(96, 0, 32, 0.3);
            border: 5px solid #900C3F;
        }
        h1, h3 {
            color: #900C3F;
        }
        button {
            background-color: #C70039;
            color: white;
            border: none;
            padding: 10px 20px;
            border-radius: 5px;
            cursor: pointer;
            font-size: 16px;
        }
        button:hover {
            background-color: #900C3F;
        }
        input {
            padding: 8px;
            width: 80%;
            margin-top: 5px;
            border: 2px solid #900C3F;
            border-radius: 5px;
        }
    </style>
</head>
<body>
    <audio id="music" autoplay loop>
        <source src="tu-musica.mp3" type="audio/mpeg">
        Tu navegador no soporta audio.
    </audio>
    
    <div class="container">
        <h1>¡Te Invitamos a Celebrar!</h1>
        <h2>Margarita - 80 Aniversario</h2>
        <p>Nos encantaría contar contigo en esta ocasión especial.</p>
        <p><strong>Fecha:</strong> 17 de mayo de 2025</p>
        <p><strong>Hora:</strong> 8:00 PM</p>
        <h3>Confirma tu asistencia</h3>
        <form id="rsvpForm">
            <label for="name">Nombre:</label>
            <input type="text" id="name" required><br><br>
            <label for="email">Correo:</label>
            <input type="email" id="email" required><br><br>
            <button type="submit">Confirmar</button>
        </form>
        <p id="responseMessage"></p>
        <br>
        <button onclick="openLocation()">Ver Ubicación</button>
        <br><br>
        <!-- Enlace para confirmar asistencia en WhatsApp -->
        <button onclick="window.open('https://wa.me/528448695474?text=Confirmo%20mi%20asistencia%20al%20evento', '_blank')">Confirmar Asistencia en WhatsApp</button>
    </div>

    <script>
        document.getElementById('rsvpForm').addEventListener('submit', function(event) {
            event.preventDefault();
            let name = document.getElementById('name').value;
            document.getElementById('responseMessage').textContent = `Gracias por confirmar, ${name}!`;
        });

        function openLocation() {
            window.open('https://maps.app.goo.gl/86mMnjZvNwZJZTUe6', '_blank');
        }
    </script>
</body>
</html>
