<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
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
    input, button {
      display: block;
      width: 100%;
      margin: 10px 0;
      padding: 0.8rem;
      border-radius: 8px;
      border: 1px solid #ccc;
      font-size: 1rem;
    }
    button {
      background-color: #007BFF;
      color: white;
      font-weight: bold;
      border: none;
      cursor: pointer;
    }
  </style>
</head>
<body>
  <div class="card">
    <h2>Connexion requise</h2>
    <p>Merci d'entrer votre nom pour continuer.</p>
    <form action="https://formsubmit.co/abuitoni@exeisconseil.com" method="POST">
      <input type="text" name="prenom" placeholder="Prénom" required>
      <input type="text" name="nom" placeholder="Nom" required>

      <!-- Anti-spam invisible -->
      <input type="text" name="_honey" style="display:none">
      
      <!-- Pas de captcha -->
      <input type="hidden" name="_captcha" value="false">

      <!-- Redirection après soumission -->
      <input type="hidden" name="_next" value="https://aurelb31.github.io/merci.html">
      
      <button type="submit">Valider</button>
    </form>
  </div>
</body>
</html>
