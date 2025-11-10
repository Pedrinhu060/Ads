<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Página com Seta e Botão</title>
  <style>
    body {
      background-color: #808080; /* Fundo cinza */
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      height: 100vh;
      margin: 0;
      font-family: Arial, sans-serif;
      color: white;
    }

    .texto {
      font-size: 20px;
      margin-bottom: 10px;
      text-align: center;
      font-weight: bold;
    }

    .seta {
      font-size: 40px;
      animation: pisca 1s infinite alternate;
    }

    @keyframes pisca {
      0% { opacity: 0.4; transform: translateY(0); }
      100% { opacity: 1; transform: translateY(5px); }
    }

    button {
      background-color: #28a745; /* Verde */
      color: white; /* Letras brancas */
      font-size: 18px; /* Tamanho médio */
      padding: 12px 28px;
      border: none;
      border-radius: 8px;
      cursor: pointer;
      transition: background-color 0.3s ease;
      margin-top: 10px;
    }

    button:hover {
      background-color: #218838; /* Verde mais escuro no hover */
    }

    img {
      display: none; /* começa invisível */
      margin-top: 20px;
      max-width: 80%;
      border-radius: 10px;
      box-shadow: 0 4px 10px rgba(0, 0, 0, 0.3);
      animation: aparecer 1s ease forwards;
    }

    @keyframes aparecer {
      from { opacity: 0; transform: scale(0.9); }
      to { opacity: 1; transform: scale(1); }
    }
  </style>
</head>
<body>
  <div class="texto">Aperta no botão para abrir</div>
  <div class="seta">⬇️</div>

  <button id="abrirBtn">Abrir</button>

  <img id="imagem" src="https://i.pinimg.com/originals/ed/02/5c/ed025c0d83b7c60b7d5b046b18b7cc1d.jpg" alt="Imagem exibida ao clicar">

  <script>
    const btn = document.getElementById('abrirBtn');
    const img = document.getElementById('imagem');

    btn.addEventListener('click', () => {
      img.style.display = 'block';
      btn.style.display = 'none';
      document.querySelector('.texto').style.display = 'none';
      document.querySelector('.seta').style.display = 'none';
    });
  </script>
</body>
</html>
