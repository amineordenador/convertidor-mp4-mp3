<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Convertidor MP4 a MP3</title>
    <style>
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #4facfe, #00f2fe);
            margin: 0;
            padding: 0;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
        }
        .container {
            background: white;
            padding: 40px;
            border-radius: 20px;
            box-shadow: 0 10px 25px rgba(0,0,0,0.2);
            text-align: center;
            width: 90%;
            max-width: 400px;
            animation: fadeIn 1s ease-in-out;
        }
        h1 {
            color: #333;
            margin-bottom: 20px;
        }
        input[type="file"] {
            margin-top: 20px;
            padding: 10px;
            background: #f4f4f4;
            border: none;
            border-radius: 10px;
            width: 100%;
        }
        button {
            margin-top: 20px;
            padding: 12px 20px;
            background: #4facfe;
            color: white;
            border: none;
            border-radius: 10px;
            cursor: pointer;
            font-size: 16px;
            transition: 0.3s;
        }
        button:hover {
            background: #00c6fb;
        }
        button:disabled {
            background: #ccc;
            cursor: not-allowed;
        }
        a {
            display: inline-block;
            margin-top: 20px;
            text-decoration: none;
            padding: 10px 15px;
            background: #28a745;
            color: white;
            border-radius: 10px;
            transition: 0.3s;
        }
        a:hover {
            background: #218838;
        }
        @keyframes fadeIn {
            from {opacity: 0; transform: translateY(-20px);}
            to {opacity: 1; transform: translateY(0);}
        }
    </style>
</head>
<body>

    <div class="container">
        <h1>🎵 Convertidor MP4 a MP3</h1>
        <input type="file" id="fileInput" accept="video/mp4">
        <br>
        <button id="convertBtn" disabled>Convertir a MP3</button>
        <br>
        <a id="downloadLink" style="display:none;" download="output.mp3">⬇ Descargar MP3</a>
    </div>

    <script>
        const fileInput = document.getElementById('fileInput');
        const convertBtn = document.getElementById('convertBtn');
        const downloadLink = document.getElementById('downloadLink');

        fileInput.addEventListener('change', () => {
            convertBtn.disabled = !fileInput.files.length;
        });

        convertBtn.addEventListener('click', () => {
            alert("Aquí irá la conversión con FFmpeg en el navegador.");
        });
    </script>

</body>
</html>
