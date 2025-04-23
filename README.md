<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Connexion sécurisée</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background: #f3f3f3;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      padding: 20px;
    }
    .card {
      background: white;
      padding: 2rem;
      border-radius: 12px;
      box-shadow: 0 4px 12px rgba(0,0,0,0.1);
      text-align: center;
      max-width: 400px;
      width: 100%;
    }
    input {
      display: block;
      width: 100%;
      padding: 0.6rem;
      margin: 10px 0;
      border-radius: 8px;
      border: 1px solid #ccc;
    }
    button {
      padding: 0.7rem 1.5rem;
      background: #007BFF;
      color: white;
      border: none;
      border-radius: 8px;
      cursor: pointer;
      font-weight: bold;
    }
    .message {
      margin-top: 20px;
      font-size: 1rem;
      color: #e63946;
    }
  </style>
</head>
<body>
  <div class="card">
    <h2>Connexion requise</h2>
    <p>Merci d'entrer votre nom pour continuer.</p>
    <form id="trapForm">
      <input type="text" id="prenom" placeholder="Prénom" required>
      <input type="text" id="nom" placeholder="Nom" required>
      <button type="submit">Valider</button>
    </form>
    <div id="result" class="message"></div>
  </div>

  <script>
    const form = document.getElementById('trapForm');
    const result = document.getElementById('result');

    form.addEventListener('submit', function(e) {
      e.preventDefault();
      const prenom = document.getElementById('prenom').value;
      const nom = document.getElementById('nom').value;

      form.style.display = 'none';
      result.innerHTML = `
        👀 Merci ${prenom} ${nom}...<br><br>
        🎣 Tu viens de tomber dans un piège !<br><br>
        ⚠️ Les QR codes sauvages peuvent être des pièges à données personnelles.<br>
        La prochaine fois, méfie-toi ! 😅<br><br>
        <em>(Mais t'inquiète, celui-ci était juste pour le fun... ou presque 👻)</em>
      `;
    });
  </script>
</body>
</html>
