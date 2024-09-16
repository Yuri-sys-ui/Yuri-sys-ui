<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Cartinha para Nath</title>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            background-color: #f3e5f5;
            color: #4a148c;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
            flex-direction: column;
        }

        .card {
            background-color: #ffffff;
            border-radius: 10px;
            padding: 20px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
            text-align: center;
            width: 300px;
            position: relative;
            overflow: hidden;
        }

        .card h1 {
            font-size: 24px;
            margin-bottom: 10px;
        }

        .card p {
            font-size: 16px;
            line-height: 1.5;
            color: #4a148c;
        }

        .heart {
            position: absolute;
            width: 100px;
            height: 100px;
            background-color: #e91e63;
            border-radius: 50%;
            top: -50px;
            left: 50%;
            transform: translateX(-50%) scale(0);
            animation: popIn 1s ease forwards;
        }

        .heart:before, .heart:after {
            content: '';
            position: absolute;
            width: 100px;
            height: 100px;
            background-color: #e91e63;
            border-radius: 50%;
        }

        .heart:before {
            top: -50px;
            left: 0;
        }

        .heart:after {
            left: 50px;
            top: 0;
        }

        @keyframes popIn {
            0% {
                transform: translateX(-50%) scale(0);
            }
            50% {
                transform: translateX(-50%) scale(1.2);
            }
            100% {
                transform: translateX(-50%) scale(1);
            }
        }

        .message {
            opacity: 0;
            animation: fadeIn 2s ease forwards 1s;
        }

        @keyframes fadeIn {
            to {
                opacity: 1;
            }
        }
    </style>
</head>
<body>

    <div class="card">
        <div class="heart"></div>
        <h1>Para Nath</h1>
        <p class="message">Aqui você pode escrever sua mensagem de amor. Deixe seu coração falar!</p>
    </div>

</body>
</html>
