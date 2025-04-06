<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <title>Headtrick do Cardoso</title>
  <style>
    * { margin: 0; padding: 0; box-sizing: border-box; }
    body, html { height: 100%; font-family: Arial, sans-serif; }
    .page {
      display: none;
      width: 100%;
      height: 100%;
      align-items: center;
      justify-content: center;
      flex-direction: column;
      background: #1a1a1a;
      color: #fff;
    }
    .page.active { display: flex; }
    h1 { margin-bottom: 2rem; font-size: 2.5rem; }
    button {
      padding: 1rem 2rem;
      font-size: 1.2rem;
      border: none;
      border-radius: 5px;
      cursor: pointer;
      background: #ff5722;
      color: #fff;
      transition: background .2s;
    }
    button:hover { background: #e64a19; }
    .message {
      margin-top: 1.5rem;
      font-size: 1.5rem;
      color: #4caf50;
    }
  </style>
</head>
<body>

  <!-- Página 1 -->
  <div id="page1" class="page active">
    <h1>Headtrick do Cardoso</h1>
    <button id="goToPage2">Quero o Headtrick!</button>
  </div>

  <!-- Página 2 -->
  <div id="page2" class="page">
    <h1>Escolha sua opção</h1>
    <button id="activateHeadtrick">Ativar Headtrick</button>
    <button id="activateAimbot" style="margin-top:1rem;">Ativar AIMBOT</button>
    <div id="message" class="message"></div>
  </div>

  <script>
    const page1 = document.getElementById('page1');
    const page2 = document.getElementById('page2');
    const btnGo = document.getElementById('goToPage2');
    const btnHead = document.getElementById('activateHeadtrick');
    const btnAim = document.getElementById('activateAimbot');
    const msg = document.getElementById('message');

    btnGo.addEventListener('click', () => {
      page1.classList.remove('active');
      page2.classList.add('active');
      msg.textContent = ''; // limpa mensagem anterior
    });

    btnHead.addEventListener('click', () => {
      msg.style.color = '#4caf50';
      msg.textContent = 'Headtrick ativado!';
    });

    btnAim.addEventListener('click', () => {
      msg.style.color = '#f44336';
      msg.textContent = 'Hacker ativado!';
    });
  </script>

</body>
</html>
