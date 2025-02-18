<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Protocolo de Emagrecimento Médico - Descubra Seu Plano</title>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            line-height: 1.6;
            max-width: 700px;
            margin: 0 auto;
            padding: 20px;
            background: #f7f7f7;
        }
        .header {
            text-align: center;
            padding: 30px;
            background: #2A9D8F;
            color: white;
            border-radius: 10px 10px 0 0;
        }
        .form-container {
            background: white;
            padding: 25px;
            border-radius: 0 0 10px 10px;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
        }
        .question {
            margin-bottom: 25px;
        }
        label {
            display: block;
            margin-bottom: 8px;
            font-weight: bold;
            color: #264653;
        }
        select, input[type="text"], input[type="email"] {
            width: 100%;
            padding: 12px;
            margin-bottom: 15px;
            border: 1px solid #ddd;
            border-radius: 5px;
            font-size: 16px;
        }
        button {
            background: #E76F51;
            color: white;
            padding: 15px 30px;
            border: none;
            border-radius: 5px;
            font-size: 18px;
            cursor: pointer;
            width: 100%;
            transition: background 0.3s;
        }
        button:hover {
            background: #D04A2A;
        }
    </style>
</head>
<body>
    <div class="header">
        <h1>🍃 Descubra Seu Protocolo de Emagrecimento Personalizado</h1>
        <p>Responda 4 perguntas e receba um plano 100% adaptado às suas necessidades!</p>
    </div>

    <div class="form-container">
        <form id="bantForm">
            <!-- Budget -->
            <div class="question">
                <label>Qual valor você investiria para emagrecer com segurança?</label>
                <select required>
                    <option value="">Selecione...</option>
                    <option value="ate1000">Até R$ 1.000</option>
                    <option value="1000-2000">R$ 1.000 - R$ 2.000</option>
                    <option value="acima2000">Acima de R$ 2.000</option>
                </select>
            </div>

            <!-- Authority -->
            <div class="question">
                <label>Você decide sozinha sobre tratamentos de saúde?</label>
                <select required>
                    <option value="">Selecione...</option>
                    <option value="sim">Sim</option>
                    <option value="nao">Não (preciso conversar com familiares)</option>
                </select>
            </div>

            <!-- Need -->
            <div class="question">
                <label>Qual seu principal objetivo?</label>
                <select required>
                    <option value="">Selecione...</option>
                    <option value="5-10kg">Perder 5-10kg</option>
                    <option value="10-15kg">Perder 10-15kg</option>
                    <option value="manter">Manter o peso atual</option>
                </select>
            </div>

            <!-- Timing -->
            <div class="question">
                <label>Quando quer iniciar o protocolo?</label>
                <select required>
                    <option value="">Selecione...</option>
                    <option value="imediato">Imediatamente</option>
                    <option value="1mes">Em 1 mês</option>
                    <option value="3meses">Em 3 meses</option>
                </select>
            </div>

            <button type="submit">👉 Gerar Meu Protocolo Gratuitamente</button>
        </form>
    </div>

    <script>
        // Substitua SCRIPT_URL pelo link do seu Google Apps Script
        const SCRIPT_URL = 'SUA_URL_DO_GOOGLE_SCRIPT_AQUI';
        const form = document.forms['bantForm'];

        form.addEventListener('submit', e => {
            e.preventDefault();
            fetch(SCRIPT_URL, { method: 'POST', body: new FormData(form) })
                .then(() => {
                    window.location.href = 'https://wa.me/5511999999999?text=Acabei%20de%20preencher%20o%20formulário%20e%20quero%20saber%20meu%20protocolo!';
                })
                .catch(error => console.error('Erro!', error.message));
        });
    </script>
</body>
</html>
