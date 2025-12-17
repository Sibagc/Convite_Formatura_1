# Convite de Formatura em ADS
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Convite Interativo</title>
    <link href="https://fonts.googleapis.com/css2?family=Dancing+Script&display=swap" rel="stylesheet"> <!-- Fonte manuscrita -->
    <style>
        body {
            font-family: Arial, sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
            background-color: #f0f0f0;
        }
        .envelope {
            position: relative;
            width: 105mm;
            height: 148mm;
            background-color: #fff;
            border: 3px solid #002366; /* Azul royal para detalhes */
            border-radius: 10px;
            box-shadow: 0 4px 8px rgba(0,0,0,0.1);
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
        }
        .selo {
            width: 50px;
            height: 50px;
            background-color: #002366; /* Azul royal */
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: bold;
            font-size: 18px;
            color: #fff;
            cursor: pointer;
            margin-bottom: 10px;
        }
        .mensagem {
            text-align: center;
            font-size: 14px;
            color: #333;
        }
        .convite {
            display: none;
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: #002366; /* Azul royal */
            border-radius: 10px;
            color: #fff;
            text-align: center;
            padding: 15px; /* Ajustado para caber mais texto */
            box-sizing: border-box;
            flex-direction: column;
            justify-content: flex-start; /* Ajustado para começar do topo */
            align-items: center;
            overflow-y: auto; /* Permite rolagem se necessário */
        }
        .convite h1 {
            margin: 0 0 10px 0;
            font-size: 20px; /* Reduzido para caber */
        }
        .convite p {
            margin: 8px 0;
            font-size: 14px; /* Ajustado para legibilidade */
            line-height: 1.4;
        }
        .mensagem-personalizada {
            text-align: justify; /* Justificado para melhor leitura */
            margin-bottom: 15px;
        }
        .verso {
            font-style: italic;
            margin-top: 15px;
        }
        .assinatura {
            font-family: 'Dancing Script', cursive; /* Fonte manuscrita */
            font-size: 18px;
            margin-top: 20px;
            text-align: center;
        }
        .botao-confirmacao {
            margin-top: 15px;
            padding: 8px 16px;
            background-color: #fff;
            color: #002366;
            border: none;
            border-radius: 5px;
            font-size: 14px;
            cursor: pointer;
            text-decoration: none; /* Para o link */
            display: inline-block;
            transition: background-color 0.3s;
            animation: piscar 2s infinite; /* Animação de piscar lentamente */
        }
        .botao-confirmacao:hover {
            background-color: #e0e0e0;
        }
    </style>
</head>
<body>
    <div class="envelope" id="envelope">
        <div class="selo" id="selo">GM</div>
        <div class="mensagem">Aperte no selo para abrir o envelope</div>
        <div class="convite" id="convite">
            <h1>Convite</h1>
            <p class="mensagem-personalizada">Hoje eu chego a um dos momentos mais importantes da minha vida, e não poderia viver isso sem lembrar de quem esteve comigo nos dias difíceis, nas conquistas e nos desafios.<br><br>Seu apoio, incentivo e presença fizeram toda a diferença na minha caminhada. Por isso, será uma alegria imensa ter você ao meu lado na minha formatura, celebrando comigo essa conquista que também carrega um pouco de você.<br><br>Sua presença tornará esse momento ainda mais especial 🤍🎓</p>
            <p><strong>Local:</strong> Av. Washington Soares, 1321, Edson Queiroz - UNIFOR</p>
            <p><strong>Data:</strong> 19 de Dezembro</p>
            <p><strong>Horário:</strong> 20h</p>
            <p class="verso">"Em tudo dai graças, porque esta é a vontade de Deus em Cristo Jesus para convosco" 1Ts 5,18</p>
            <p class="assinatura">Gabriella Moreira</p>
            <a href="https://wa.me/558597639459?text=Olá%20Gabriella,%20confirmo%20minha%20presença%20na%20formatura!" class="botao-confirmacao" id="confirmar">Confirmar Presença</a>
        </div>
    </div>

    <script>
        document.getElementById('selo').addEventListener('click', function() {
            document.getElementById('convite').style.display = 'flex';
            document.getElementById('selo').style.display = 'none';
            document.querySelector('.mensagem').style.display = 'none';
        });
    </script>
</body>
</html>
