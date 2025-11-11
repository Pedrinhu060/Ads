<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Página com Seta e Botão</title>
  <style>
    body {
      background-color: #808080;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      height: 100vh;
      margin: 0;
      font-family: Arial, sans-serif;
      color: white;
      overflow: hidden;
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
      background-color: #28a745;
      color: white;
      font-size: 18px;
      padding: 12px 28px;
      border: none;
      border-radius: 8px;
      cursor: pointer;
      transition: background-color 0.3s ease;
      margin-top: 10px;
      z-index: 2;
    }

    button:hover {
      background-color: #218838;
    }

    /* Container para o efeito fullscreen */
    .fullscreen {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background-color: rgba(0, 0, 0, 0.9);
      display: none;
      justify-content: center;
      align-items: center;
      z-index: 1;
      animation: fadeIn 0.8s ease forwards;
    }

    .fullscreen img {
      max-width: 90%;
      max-height: 90%;
      border-radius: 12px;
      object-fit: contain;
      animation: zoomIn 0.8s ease forwards;
      box-shadow: 0 6px 20px rgba(0, 0, 0, 0.4);
    }

    @keyframes fadeIn {
      from { opacity: 0; }
      to { opacity: 1; }
    }

    @keyframes zoomIn {
      from { transform: scale(0.8); opacity: 0; }
      to { transform: scale(1); opacity: 1; }
    }
  </style>
</head>
<body>
  <div class="texto">Aperta no botão para abrir</div>
  <div class="seta">⬇️</div>

  <button id="abrirBtn">Abrir</button>

  <div class="fullscreen" id="fullscreenContainer">
    <img id="imagem" src="[https://i.pinimg.com/originals/ed/02/5c/ed025c0d83b7c60b7d5b046b18b7cc1d.jpg](https://ibb.co/pB8V7PqL)" alt="Imagem exibida ao clicar">
  </div>

  <script>
    const btn = document.getElementById('abrirBtn');
    const fullscreen = document.getElementById('fullscreenContainer');
    const texto = document.querySelector('.texto');
    const seta = document.querySelector('.seta');

    btn.addEventListener('click', () => {
      fullscreen.style.display = 'flex';
      btn.style.display = 'none';
      texto.style.display = 'none';
      seta.style.display = 'none';
    });

    // clicar fora da imagem fecha o fullscreen
    fullscreen.addEventListener('click', (e) => {
      if (e.target === fullscreen) {
        fullscreen.style.display = 'none';
        btn.style.display = 'block';
        texto.style.display = 'block';
        seta.style.display = 'block';
      }
    });
  </script>
</body>
</html>
