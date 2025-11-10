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

  <img id="imagem" src="https://www.google.com/search?client=ms-android-motorola-rvo3&sca_esv=fde8e1c91dfdf3f9&sxsrf=AE3TifNgW1ON4Ec8uNeYLSNb0F-JuTn_0g:1762818009989&udm=2&fbs=AIIjpHydJdUtNKrM02hj0s4nbm4yAFb4PvhjIUcDtaFHkK_tyspyDJg0-Y4Ji8bGEtEDNJFQduqi-TCs4_9mtRCleowrm4wkMMdmjI2QB42C-Jk-i89uBMbU7tPYZGq42zKl-sdKbT2diiPtbbsQdnoe9CzQsSshKneJQc0YuPdzklQRfEwQLz7tAKvYTv0cUGo1VQ-WUjIvlU-v-w1sOlZ63Kv8TlrwxXDTh3TtSP6YwHJc0fLpQm0&q=meme+do+macaco+dando+dedo&sa=X&ved=2ahUKEwi24Kfq4OiQAxXnrZUCHW1DKqwQtKgLegQIERAB&biw=484&bih=969&dpr=1.49#sv=CAMSgwUa4wQKlQIKuQEStgEKd0FMa3RfdkhXeXduNktGYUNWQjNtdEh5Skw0Z0xVbV8zQ1phNk1kOGtUSVJzWFJPZndsdzFhXzdvUTl3V2ctQzRXTi1CRHR0ZmhiQ1VzSDRLM3hDTng0WmFsaVZPVFgtZ1YxNjJuZk9xSHNwXzlyOGp1RXZ6QVdnEhczbmNTYWNPekdJalUxc1FQNHRHVC1RNBoiQUZNQUdHcUpFaVp0MWZfcmh4MkRYQWF3anlISGJHa0lIURIDODQ5GgEzIh4KAXESGW1lbWUgZG8gbWFjYWNvIGRhbmRvIGRlZG8iBwoDdGJzEgAiJgoEZXFsZBIeQ2dJSUFCQUFPZ1FJQUJBQVZaMzUzejV0LUpjWlBnErYCCs8BEswBCowBQUxrdF92RWNYSm4zTWFDOW93RlJrdl85UGVMTTJXSE1OWVlCcXZodnFaUVhpZ0xyRGJlRlBoaWtDUU82am9KQnIzVTQySmYyd1k0R3RFLW5kS1MwOTlraXBtSjVRR0lLeWdKQ1ZfYXFpVWhtaWtnel9heGhRVjJEaDFHR2RDSEhuWG5GbkRmb0xIaHUSFzNuY1NhY096R0lqVTFzUVA0dEdULVE0GiJBRk1BR0dwV3JkZTZXRGx3Q1pQN3VQTV93WXRFTEFvc1JnEgQ0Njk4GgEzIhgKBmltZ2RpaRIOTXR1ZnlsQ2tmUjJCcU0iFwoFZG9jaWQSDmxCNzhzNkUtMzZJWE1NIiYKBGVxbGQSHkNnSUlBQkFBT2dRSUFCQUFWWjM1M3o1dC1KY1pQZyoQZS1NdHVmeWxDa2ZSMkJxTSAEKhcKAXMSEGUtTXR1ZnlsQ2tmUjJCcU0YATABGAcgppXGtgcwAUoKCAIQAhgCIAIoAg">

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
