<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Accueil - Le Chanvre d'ici</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
        }

        /* Bandeau avec le logo */
        header {
            background-color: #333;
            color: #fff;
            padding: 10px 20px;
            display: flex;
            align-items: center;
        }
        header img {
            height: 150px;
            margin-right: 20px;
        }
        header h1 {
            margin: 0;
            font-size: 24px;
        }

        /* Menu horizontal */
        nav {
            display: flex;
            justify-content: space-around;
            background-color: #f4f4f4;
            padding: 10px 0;
        }
        nav a {
            text-decoration: none;
            color: #333;
            text-align: center;
        }
        nav a img {
            width: 100px;
            height: 100px;
            display: block;
            margin: 0 auto;
        }
        nav a span {
            font-size: 14px;
        }

        /* Bandeau promo */
        .promo {
        background-color: orange; /* Fond orange pour le bandeau */
        display: flex;
        justify-content: center; /* Centre le contenu horizontalement */
        align-items: center; /* Centre le contenu verticalement */
        height: 250px; /* Ajuster la hauteur pour inclure le titre */
        flex-direction: column; /* Aligne le contenu verticalement */
        }

        .promo-content {
        text-align: center; /* Centre tout le contenu horizontalement */
        }

        .promo-content h2 {
        font-size: 24px; /* Taille du texte pour 'PROMO DU MOMENT' */
        margin: 0 0 10px 0; /* Espacement en bas */
        font-weight: bold; /* Met le texte en gras */
        color: white; /* Couleur du texte */
        }

        .promo-item {
        display: flex;
        align-items: center; /* Aligne l'image et le contenu verticalement */
        gap: 15px; /* Espace entre l'image et le contenu */
        padding: 10px;
        background-color: white; /* Fond blanc autour des éléments */
        border: 1px solid #ddd; /* Optionnel, pour délimiter visuellement */
        border-radius: 5px;
        box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1); /* Optionnel, ajoute une ombre */
        }

        .promo-item img {
        max-width: 150px; /* Taille de l'image */
        height: auto;
        border-radius: 5px; /* Coins arrondis */
        }

        .promo-details {
        display: flex;
        flex-direction: column; /* Aligne le texte et le bouton verticalement */
        }

        .promo-details h3 {
        margin: 0 0 10px 0; /* Espacement en bas du titre */
        }

        .promo-details p {
        margin: 0 0 10px 0; /* Espacement en bas du prix */
        }

        .promo-details button {
        background-color: #28a745;
        color: #fff;
        border: none;
        padding: 10px 15px;
        cursor: pointer;
        border-radius: 5px;
        font-size: 14px;
        }

        .promo-details button:hover {
        background-color: #218838;
        }



        /* Liste des produits */
        .products {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            padding: 20px;
            gap: 20px;
        }
        .product {
            border: 1px solid #ddd;
            border-radius: 5px;
            width: 200px;
            text-align: center;
            padding: 10px;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
        }
        .product img {
            max-width: 100%;
            height: auto;
            border-bottom: 1px solid #ddd;
            margin-bottom: 10px;
        }
        .product h3 {
            font-size: 16px;
            margin: 10px 0;
        }
        .product p {
            color: #333;
            font-size: 14px;
            margin: 5px 0;
        }
        .product button {
            background-color: #28a745;
            color: #fff;
            border: none;
            padding: 10px 15px;
            cursor: pointer;
            border-radius: 5px;
            font-size: 14px;
        }
        .product button:hover {
            background-color: #218838;
        }

        /* panier */
        .cart {
        margin-top: 20px;
        padding: 10px;
        border: 1px solid #ddd;
        background-color: #f9f9f9;
        border-radius: 5px;
        max-width: 300px;
        }

        .cart h2 {
        font-size: 20px;
        margin-bottom: 10px;
        }

        #cart-list {
        list-style-type: none;
        padding: 0;
        }

        #cart-list li {
        margin-bottom: 5px;
        }

        #cart-total {
        font-weight: bold;
        margin-top: 10px;
        }
    </style>
</head>
<body>

    <!-- Bandeau avec le logo -->
    <header>
        <img src="logo.jpg" alt="Logo">
        <h1>Le Chanvre D'ici</h1>
    </header>

    <!-- Menu horizontal avec catégories -->
    <nav>
        <a href="#">
            <img src="fleursdechanvre.jpg" alt="Fleurs de Chanvre">
            <span>Fleurs de Chanvre</span>
        </a>
        <a href="#">
            <img src="pollen.jpg" alt="Pollen">
            <span>Pollen</span>
        </a>
        <a href="#">
            <img src="infusions.jpg" alt="infusions">
            <span>Infusions</span>
        </a>
        <a href="#">
            <img src="graines.jpg" alt="graines">
            <span>Graines</span>
        </a>
    </nav>

   <!-- Bandeau promo --> 
    <div class="promo">
        <div class="promo-content">
            <h2>PROMO DU MOMENT</h2> <!-- Titre du bandeau -->
            <div class="promo-item" data-name="PROMO DU MOMENT Fleurs de chanvre" data-price="19.99">
                <img src="fleursdechanvre.jpg" alt="fleursdechanvre"> 
                <div class="promo-details">
                    <h3>fleurs de chanvre</h3>
                    <p>Prix : 19,99 €</p>
                    <button>Ajouter au panier</button>
                </div>
            </div>
        </div>
    </div>



    <!-- Liste des produits -->
    <div class="products">
        <div class="product" data-name="Fleurs de chanvre2" data-price="19.99">
            <img src="produit1.jpg" alt="Produit 1">
            <h3>Produit 1</h3>
            <p>Prix : 19,99 €</p>
            <button>Ajouter au panier</button>
        </div>
        <div class="product" data-name="Fleurs de chanvre3" data-price="29.99">
            <img src="produit2.jpg" alt="Produit 2">
            <h3>Produit 2</h3>
            <p>Prix : 29,99 €</p>
            <button>Ajouter au panier</button>
        </div>
        <div class="product" data-name="Fleurs de chanvre4" data-price="39.99">
            <img src="produit3.jpg" alt="Produit 3">
            <h3>Produit 3</h3>
            <p>Prix : 39,99 €</p>
            <button>Ajouter au panier</button>
        </div>
        <div class="product" data-name="Fleurs de chanvre5" data-price="49.99">
            <img src="produit4.jpg" alt="Produit 4">
            <h3>Produit 4</h3>
            <p>Prix : 49,99 €</p>
            <button>Ajouter au panier</button>
        </div>
    </div>

    <!-- Affichage du panier -->
    <div class="cart">
        <h2>Panier</h2>
        <ul id="cart-list">
            <!-- Les produits ajoutés apparaîtront ici -->
        </ul>
        <p id="cart-total">Total : 0,00 €</p>
    </div>

    <div id="gpay-container"></div>

    <script>
        // Initialisation du panier
        const cart = [];
    
        // Fonction pour mettre à jour l'affichage du panier et récupérer le total
        function updateCartDisplay() {
            const cartList = document.getElementById('cart-list');
            const cartTotal = document.getElementById('cart-total');
    
            // Vide la liste actuelle
            cartList.innerHTML = '';
    
            // Ajoute chaque produit dans le panier à la liste
            let total = 0;
            cart.forEach((item) => {
                const li = document.createElement('li');
                li.textContent = `${item.name} - ${item.price.toFixed(2)} €`;
                cartList.appendChild(li);
                total += item.price;
            });
    
            // Met à jour le total
            cartTotal.textContent = `Total : ${total.toFixed(2)} €`;
    
            // Met à jour la variable globale pour le total du panier
            window.cartTotalPrice = total.toFixed(2); // Store the total in a global variable
        }
    
        // Écouteur d'événements pour les boutons "Ajouter au panier"
        document.querySelectorAll('button').forEach(button => {
            button.addEventListener('click', (event) => {
                // Trouve l'élément parent avec les données du produit
                const productElement = event.target.closest('.product, .promo-item');
                const productName = productElement.getAttribute('data-name');
                const productPrice = parseFloat(productElement.getAttribute('data-price'));
    
                // Ajoute le produit au panier
                cart.push({ name: productName, price: productPrice });
    
                // Met à jour l'affichage du panier
                updateCartDisplay();
            });
        });

    </script>
    <script type="text/javascript" src="main.js"></script>
    <script
      async src="https://pay.google.com/gp/p/js/pay.js"
      onload="onGooglePayLoaded()">
    </script>
    
</body>
</html>

