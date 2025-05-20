<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Vorace Restaurant</title>
  <style>
    @font-face {
      font-family: 'Areqo';
      src: url('fonts/areqo.woff2') format('woff2'),
           url('fonts/areqo.woff') format('woff');
      font-weight: normal;
      font-style: normal;
    }

    body {
      margin: 0;
      font-family: Arial, sans-serif;
      background-color: #f0e6d6;
      color: #333;
    }

    header {
      background-color: #2e4b3b;
      color: white;
      text-align: center;
      padding: 60px 20px;
    }

    .logo-text {
      font-family: 'Areqo', sans-serif;
      font-size: 64px;
      letter-spacing: 4px;
    }

    .subtitle {
      font-size: 18px;
      letter-spacing: 2px;
      margin-top: 10px;
    }

    nav {
      background-color: #1f3428;
      display: flex;
      justify-content: center;
      gap: 30px;
      padding: 15px;
    }

    nav a {
      color: white;
      text-decoration: none;
      font-weight: bold;
    }

    nav a:hover {
      text-decoration: underline;
    }

    section {
      padding: 40px 20px;
      max-width: 1000px;
      margin: auto;
    }

    .menu {
      margin-top: 30px;
      background-color: #2e4b3b;
      border: 6px solid #5e3b1f;
      border-radius: 20px;
      padding: 60px 40px;
      box-shadow: 0 8px 25px rgba(0, 0, 0, 0.1);
    }

    .menu h2 {
      text-align: center;
      font-family: 'Areqo', sans-serif;
      font-size: 42px;
      color: #f0e6d6;
      margin-bottom: 30px;
      text-shadow: 1px 1px 3px rgba(0, 0, 0, 0.2);
    }

    .menu ul {
      list-style: none;
      padding: 0;
      text-align: center;
    }

    .menu li {
      font-size: 22px;
      padding: 18px 0;
      background: #fffaf0;
      margin: 14px auto;
      max-width: 600px;
      border-radius: 10px;
      color: #4b3b2f;
      font-weight: bold;
      display: flex;
      align-items: center;
      justify-content: center;
      gap: 10px;
      transition: transform 0.3s ease, background-color 0.3s ease;
    }

    .menu li:hover {
      transform: scale(1.05);
      background-color: #f0e6d6;
    }

    

    .booking {
      text-align: center;
      margin: 40px 0;
    }

    .booking a {
      display: inline-block;
      background-color: #2e4b3b;
      color: white;
      padding: 15px 30px;
      text-decoration: none;
      border-radius: 5px;
      font-weight: bold;
    }

    .booking a:hover {
      background-color: #3d6b53;
    }

    .a-propos-container {
      display: flex;
      flex-wrap: wrap;
      align-items: center;
      gap: 20px;
    }

    .a-propos-text {
      flex: 1 1 300px;
    }

    .a-propos-img {
      flex: 1 1 300px;
      text-align: center;
    }

    .a-propos-img img {
      max-width: 100%;
      height: auto;
      border-radius: 10px;
      box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
    }

    footer {
      background-color: #2e4b3b;
      color: white;
      text-align: center;
      padding: 20px;
      margin-top: 40px;
    }
  </style>
</head>
<body>
  <header>
    <div class="logo-text">VORACE</div>
    <div class="subtitle">RESTAURANT</div>
  </header>

  <nav>
    <a href="#a-propos">À propos</a>
    <a href="#menu">Menu</a>
    <a href="#contact">Contact</a>
  </nav>

  <section id="a-propos">
    <h2>À propos de Vorace</h2>
    <div class="a-propos-container">
      <div class="a-propos-text">
        <p>Situé à Plérin, près de Saint-Brieuc, le restaurant Vorace propose une cuisine moderne, locale et de saison. Dans un cadre chaleureux, découvrez une carte audacieuse qui met en valeur les produits bretons.</p>
      </div>
      <div class="a-propos-img">
        <img src="images/WhatsApp%20Image%202025-05-20%20%C3%A0%2018.03.06_e00dde6d.jpg" alt="Chef au comptoir du restaurant Vorace">
      </div>
    </div>
  </section>

  <section id="menu" class="menu">
    <h2>Notre Menu</h2>
    <ul>
      <li><a href="#" onclick="toggleEntrees(event)" style="color: #4b3b2f; text-decoration: none;">Entrées &#x25BC;</a></li>
      <style>
#entrees li, #plats li, #desserts li {
  font-family: 'Areqo', sans-serif;
  font-size: 20px;
  background-color: #f0e6d6;
  margin: 8px auto;
  border-radius: 8px;
  padding: 10px;
  color: #2e4b3b;
  max-width: 500px;
  box-shadow: 0 2px 6px rgba(0,0,0,0.1);
}
</style>
      <ul id="entrees" style="display: none; padding-left: 0;">
        <li>Velouté de topinambours, noisettes grillées</li>
        <li>Tartare de saumon, agrumes et herbes fraîches</li>
        <li>Terrine maison aux champignons</li>
      </ul>
      <li><a href="#" onclick="togglePlats(event)" style="color: #4b3b2f; text-decoration: none;">Plats &#x25BC;</a></li>
      <ul id="plats" style="display: none; padding-left: 0;">
        <li>Filet de bar, risotto aux herbes fraîches</li>
        <li>Magret de canard, purée de céleri</li>
        <li>Ravioles de légumes à la crème d’ail</li>
      </ul>
      <li><a href="#" onclick="toggleDesserts(event)" style="color: #4b3b2f; text-decoration: none;">Desserts &#x25BC;</a></li>
      <ul id="desserts" style="display: none; padding-left: 0;">
        <li>Tarte fine aux pommes, glace au caramel</li>
        <li>Moelleux au chocolat, cœur coulant</li>
        <li>Panna cotta à la vanille et coulis de fruits rouges</li>
      </ul>
    </ul>
  </section>

  <section class="booking">
    <a href="https://app.overfull.fr/booking-v2/?key_id=xbBPwouPgj8&source=Instagram" target="_blank">Réserver une table</a>
  </section>

  <section id="contact" class="contact">
    <h2>Contact</h2>
    <p>📍 12 rue de l'Océan, 22190 Plérin</p>
    <p>📞 02 96 00 00 00</p>
    <p>📧 contact@vorace-restaurant.fr</p>
  </section>

  <footer>
    &copy; 2025 Vorace Restaurant — Tous droits réservés.
  </footer>
<script>
  function toggleEntrees(event) {
    event.preventDefault();
    const sousMenu = document.getElementById("entrees");
    sousMenu.style.display = sousMenu.style.display === "none" ? "block" : "none";
  }
  function togglePlats(event) {
    event.preventDefault();
    const sousMenu = document.getElementById("plats");
    sousMenu.style.display = sousMenu.style.display === "none" ? "block" : "none";
  }

  function toggleDesserts(event) {
    event.preventDefault();
    const sousMenu = document.getElementById("desserts");
    sousMenu.style.display = sousMenu.style.display === "none" ? "block" : "none";
  }
</script>
</body>
</html>
