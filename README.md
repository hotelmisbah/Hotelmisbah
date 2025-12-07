<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Hotel Misbah | Authentic Cuisine</title>
    <style>
        /* --- RESET & PREMIUM VARIABLES --- */
        :root {
            /* Muted Gold for Premium Accent */
            --primary-color: #a0855c; 
            /* Very Dark Charcoal for Navigation/Footer */
            --bg-dark: #121212;
            /* Dark Charcoal for Main Background */
            --bg-light: #1e1e1e;
            /* Creamy Off-White for Text on Dark Backgrounds */
            --text-light: #f3f3f3; 
            /* Light Grey for General Text */
            --text-dark: #d1d5db; 
            
            /* --- NEW FONT CHOICES --- */
            /* Elegant, modern Sans-serif for body */
            --font-main: 'Avenir Next', 'Inter', 'Helvetica Neue', Arial, sans-serif;
            /* Classic, premium Serif for headings and logo */
            --font-serif: 'Palatino Linotype', Palatino, Georgia, serif; 
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: var(--font-main); /* Changed */
            line-height: 1.6;
            color: var(--text-dark);
            background-color: var(--bg-light); 
        }

        a { text-decoration: none; color: inherit; }
        ul { list-style: none; }
        img { max-width: 100%; display: block; }

        /* --- NAVIGATION --- */
        nav {
            background-color: var(--bg-dark);
            color: var(--text-light);
            padding: 1rem 2rem;
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            display: flex;
            justify-content: space-between;
            align-items: center;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.5); 
        }

        .logo {
            font-family: var(--font-serif); /* Changed */
            font-size: 1.5rem;
            font-weight: bold;
            color: var(--primary-color);
        }

        .nav-links {
            display: flex;
            gap: 2rem;
        }

        .nav-links a {
            font-weight: 500;
            transition: color 0.3s;
        }

        .nav-links a:hover {
            color: var(--primary-color);
        }

        /* --- HERO SECTION --- */
        .hero {
            height: 100vh;
            background: url('1000095857.jpg'); 
            background-size: cover;
            background-position: center;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            color: var(--text-light);
            padding: 0 1rem;
            position: relative;
        }
        
        .hero::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.4); 
            z-index: 1;
        }

        .hero-content {
            z-index: 2; 
        }

        .hero h1 {
            font-family: var(--font-serif); /* Changed */
            font-size: 3.5rem;
            margin-bottom: 1rem;
            text-shadow: 0 0 10px rgba(0, 0, 0, 1); 
        }

        .hero p {
            font-size: 1.2rem;
            margin-bottom: 2rem;
            text-shadow: 0 0 5px rgba(0, 0, 0, 1);
        }

        .cta-button {
            background-color: var(--primary-color);
            color: var(--bg-dark); 
            padding: 1rem 2rem;
            font-size: 1.1rem;
            border-radius: 5px;
            font-weight: bold;
            transition: background 0.3s;
        }

        .cta-button:hover {
            background-color: var(--text-light); 
            color: var(--bg-dark);
        }

        /* --- MENU SECTION --- */
        .menu-section {
            padding: 4rem 2rem;
            max-width: 1200px;
            margin: 0 auto;
        }

        .section-title {
            text-align: center;
            font-family: var(--font-serif); /* Changed */
            font-size: 2.5rem;
            margin-bottom: 3rem;
            color: var(--text-light); 
        }

        .menu-category {
            margin-bottom: 3rem;
            padding: 1rem 0;
            border-bottom: 2px solid var(--primary-color);
        }
        
        .menu-category h3 {
            font-family: var(--font-serif); /* Changed */
            font-size: 1.8rem;
            color: var(--primary-color);
            margin-bottom: 1.5rem;
            text-align: center;
        }

        .menu-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 1.5rem;
        }

        /* --- MENU ITEM CARD DESIGN UPDATE --- */
        .menu-item {
            background: #2a2a2a; 
            padding: 1.2rem 1.5rem; 
            border-radius: 8px;
            border: 1px solid var(--primary-color); 
            box-shadow: 0 4px 10px rgba(0,0,0,0.5); 
            transition: transform 0.3s, box-shadow 0.3s;
        }

        .menu-item:hover {
            transform: translateY(-3px);
            box-shadow: 0 8px 16px rgba(0,0,0,0.4), 0 0 10px var(--primary-color); 
            background: #333333;
        }

        .item-header {
            display: flex;
            justify-content: space-between;
            margin-bottom: 0.5rem;
            padding-bottom: 0.3rem;
            border-bottom: 1px dashed #555; 
        }

        .item-name { 
            font-weight: bold; 
            font-size: 1.15rem; 
            color: var(--text-light); 
        } 
        
        .item-price { 
            color: var(--primary-color); 
            font-weight: bold; 
            font-size: 1.1rem;
        }

        .item-desc { 
            font-size: 0.9rem; 
            color: #b0b0b0; 
            margin-top: 0.5rem; 
        }

        /* --- ABOUT / INFO --- */
        .info-section {
            background-color: var(--bg-dark); 
            color: var(--text-light);
            padding: 4rem 2rem;
            text-align: center;
        }
        
        .info-grid {
            display: grid;
            grid-template-columns: 1fr 1fr 1fr; 
            gap: 2rem;
            max-width: 1200px; 
            margin: 0 auto;
        }

        .info-grid h3 {
             color: var(--primary-color);
             margin-bottom: 1rem;
             font-size: 1.4rem;
             font-family: var(--font-serif); /* Changed */
        }
        
        .info-grid p {
             font-size: 1rem;
             margin-bottom: 0.5rem;
        }

        /* Footer Styling */
        footer {
            background-color: var(--bg-dark);
            color: #555;
            text-align: center;
            padding: 1rem;
            font-size: 0.85rem;
        }


        /* --- MOBILE RESPONSIVE --- */
        @media (max-width: 900px) { 
            .hero h1 { font-size: 2.5rem; }
            .info-grid { 
                grid-template-columns: 1fr; 
                max-width: 500px;
            }
            .nav-links { display: none; } 
        }
    </style>
</head>
<body>

    <nav>
        <div class="logo">Hotel Misbah</div>
        <ul class="nav-links">
            <li><a href="#home">Home</a></li>
            <li><a href="#menu">Menu</a></li>
            <li><a href="#about">About</a></li>
        </ul>
    </nav>

    <header id="home" class="hero">
        <div class="hero-content">
            <h1>Hotel Misbah</h1>
            <p>Experience Authentic South Indian, Chinese, and Arabian Specialties.</p>
            <a href="#menu" class="cta-button">Explore Our Menu</a>
        </div>
    </header>

    <section id="menu" class="menu-section">
        <h2 class="section-title">Our Full Menu</h2>

        <div class="menu-category">
            <h3>Breads, Staples & Combos</h3>
            <div class="menu-grid">
                <div class="menu-item"><div class="item-header"><span class="item-name">Appam</span><span class="item-price">₹10</span></div><p class="item-desc">Soft, bowl-shaped pancake, perfect with curry.</p></div>
                <div class="menu-item"><div class="item-header"><span class="item-name">Idiyappam</span><span class="item-price">₹10</span></div><p class="item-desc">Delicate rice flour string hoppers.</p></div>
                <div class="menu-item"><div class="item-header"><span class="item-name">Puttu</span><span class="item-price">₹10</span></div><p class="item-desc">Steamed rice cake with grated coconut.</p></div>
                <div class="menu-item"><div class="item-header"><span class="item-name">Poori</span><span class="item-price">₹10</span></div><p class="item-desc">Deep-fried bread.</p></div>
                <div class="menu-item"><div class="item-header"><span class="item-name">Pathiri</span><span class="item-price">₹4</span></div><p class="item-desc">Thin, soft rice flatbread.</p></div>
                <div class="menu-item"><div class="item-header"><span class="item-name">Porotta</span><span class="item-price">₹12</span></div><p class="item-desc">Flaky, layered flatbread.</p></div>
                <div class="menu-item"><div class="item-header"><span class="item-name">Chappati</span><span class="item-price">₹10</span></div><p class="item-desc">Thin, unleavened whole wheat flatbread.</p></div>
                <div class="menu-item"><div class="item-header"><span class="item-name">Kuboos</span><span class="item-price">₹10</span></div><p class="item-desc">Fluffy flatbread, ideal for grills.</p></div>
                <div class="menu-item"><div class="item-header"><span class="item-name">Kothu Porotta</span><span class="item-price">₹160</span></div><p class="item-desc">Shredded porotta mixed with spices and meat.</p></div>
                <div class="menu-item"><div class="item-header"><span class="item-name">Chilli Porotta</span><span class="item-price">₹100</span></div><p class="item-desc">Porotta tossed in spicy chili sauce.</p></div>
                <div class="menu-item"><div class="item-header"><span class="item-name">Appam With Chicken Curry</span><span class="item-price">₹60</span></div><p class="item-desc">Appam served with a side of Chicken Curry.</p></div>
                <div class="menu-item"><div class="item-header"><span class="item-name">Puttu With Chicken Curry</span><span class="item-price">₹60</span></div><p class="item-desc">Puttu served with a side of Chicken Curry.</p></div>
                <div class="menu-item"><div class="item-header"><span class="item-name">Appam With Beef Curry</span><span class="item-price">₹80</span></div><p class="item-desc">Appam served with a side of Beef Curry.</p></div>
                <div class="menu-item"><div class="item-header"><span class="item-name">Puttu With Beef Curry</span><span class="item-price">₹80</span></div><p class="item-desc">Puttu served with a side of Beef Curry.</p></div>
                <div class="menu-item"><div class="item-header"><span class="item-name">Porotta With Beef Curry</span><span class="item-price">₹80</span></div><p class="item-desc">Porotta served with a side of Beef Curry.</p></div>
                <div class="menu-item"><div class="item-header"><span class="item-name">Porotta With Chicken Curry</span><span class="item-price">₹60</span></div><p class="item-desc">Porotta served with a side of Chicken Curry.</p></div>
            </div>
        </div>

        <div class="menu-category">
            <h3>Biriyanis & Specialty Rice</h3>
            <div class="menu-grid">
                <div class="menu-item"><div class="item-header"><span class="item-name">Veg Biriyani</span><span class="item-price">₹120</span></div><p class="item-desc">Aromatic rice cooked with seasonal vegetables.</p></div>
                <div class="menu-item"><div class="item-header"><span class="item-name">Egg Biriyani</span><span class="item-price">₹120</span></div><p class="item-desc">Flavored rice layered with boiled eggs.</p></div>
                <div class="menu-item"><div class="item-header"><span class="item-name">Chicken Biriyani</span><span class="item-price">₹150</span></div><p class="item-desc">Classic chicken and spiced rice preparation.</p></div>
                <div class="menu-item"><div class="item-header"><span class="item-name">Half Chicken Biriyani</span><span class="item-price">₹100</span></div><p class="item-desc">A smaller portion of our famous Chicken Biriyani.</p></div>
                <div class="menu-item"><div class="item-header"><span class="item-name">Beef Biriyani</span><span class="item-price">₹160</span></div><p class="item-desc">Spicy rice and tender beef pieces.</p></div>
                <div class="menu-item"><div class="item-header"><span class="item-name">Mutton Biriyani</span><span class="item-price">₹180</span></div><p class="item-desc">Premium mutton with fragrant basmati rice.</p></div>
                <div class="menu-item"><div class="item-header"><span class="item-name">Fish Biriyani</span><span class="item-price">₹180</span></div><p class="item-desc">Fresh fish chunks layered with spiced rice.</p></div>
                <div class="menu-item"><div class="item-header"><span class="item-name">Prawns Biriyani</span><span class="item-price">₹150</span></div><p class="item-desc">Delicious biriyani with succulent prawns.</p></div>
                <div class="menu-item"><div class="item-header"><span class="item-name">Hyderabad Biriyani</span><span class="item-price">₹130</span></div><p class="item-desc">The famous spicy Hyderabad style biriyani.</p></div>
                <div class="menu-item"><div class="item-header"><span class="item-name">Mandi Rice</span><span class="item-price">₹70</span></div><p class="item-desc">Plain, flavorful Mandi style rice.</p></div>
                <div class="menu-item"><div class="item-header"><span class="item-name">Ghee Rice</span><span class="item-price">₹70</span></div><p class="item-desc">Fragrant rice cooked in clarified butter.</p></div>
                <div class="menu-item"><div class="item-header"><span class="item-name">Biriyani Rice</span><span class="item-price">₹70</span></div><p class="item-desc">Plain, flavored biriyani rice.</p></div>
                <div class="menu-item"><div class="item-header"><span class="item-name">Biriyani Rice (Half)</span><span class="item-price">₹50</span></div><p class="item-desc">Half portion of plain biriyani rice.</p></div>
                <div class="menu-item"><div class="item-header"><span class="item-name">Meals</span><span class="item-price">₹60</span></div><p class="item-desc">Complete daily meal with rice and various side dishes.</p></div>
                <div class="menu-item"><div class="item-header"><span class="item-name">Ifthar (Special)</span><span class="item-price">₹220</span></div><p class="item-desc">Seasonal special meal platter.</p></div>
            </div>
        </div>

        <div class="menu-category">
            <h3>Beef & Mutton Specialties</h3>
            <div class="menu-grid">
                <div class="menu-item"><div class="item-header"><span class="item-name">Beef Roast</span><span class="item-price">₹150</span></div><p class="item-desc">Slow-cooked tender beef roast.</p></div>
                <div class="menu-item"><div class="item-header"><span class="item-name">Beef Fry</span><span class="item-price">₹180</span></div><p class="item-desc">Spicy, dry-fried beef.</p></div>
                <div class="menu-item"><div class="item-header"><span class="item-name">Beef Masala</span><span class="item-price">₹180</span></div><p class="item-desc">Thick, semi-gravy beef preparation.</p></div>
                <div class="menu-item"><div class="item-header"><span class="item-name">Beef Perattu</span><span class="item-price">₹130</span></div><p class="item-desc">Semi-dry preparation, slow-cooked with spices.</p></div>
                <div class="menu-item"><div class="item-header"><span class="item-name">Beef Ularthu</span><span class="item-price">₹110</span></div><p class="item-desc">Traditional beef dry fry.</p></div>
                <div class="menu-item"><div class="item-header"><span class="item-name">Beef Kadai</span><span class="item-price">₹160</span></div><p class="item-desc">Beef cooked in a kadai (wok) with bell peppers and spices.</p></div>
                <div class="menu-item"><div class="item-header"><span class="item-name">Beef Ularthu</span><span class="item-price">₹110</span></div><p class="item-desc">Kerala style dry beef preparation.</p></div>
                <div class="menu-item"><div class="item-header"><span class="item-name">Beef Chaps</span><span class="item-price">₹100</span></div><p class="item-desc">A thin, flavorful gravy preparation.</p></div>
                <div class="menu-item"><div class="item-header"><span class="item-name">B.D.F. (Beef Dry Fry)</span><span class="item-price">₹150</span></div><p class="item-desc">Popular spicy dry-fried beef preparation.</p></div>
                <div class="menu-item"><div class="item-header"><span class="item-name">Chilly Beef</span><span class="item-price">₹180</span></div><p class="item-desc">Indo-Chinese style spicy chili beef (Gravy).</p></div>
                <div class="menu-item"><div class="item-header"><span class="item-name">Chilli Beef Dry</span><span class="item-price">₹180</span></div><p class="item-desc">Indo-Chinese style spicy chili beef (Dry).</p></div>
                <div class="menu-item"><div class="item-header"><span class="item-name">Pepper Beef</span><span class="item-price">₹180</span></div><p class="item-desc">Beef tossed with crushed black pepper.</p></div>
                <div class="menu-item"><div class="item-header"><span class="item-name">Mutton Curry</span><span class="item-price">₹120</span></div><p class="item-desc">Traditional mutton curry.</p></div>
                <div class="menu-item"><div class="item-header"><span class="item-name">Mutton Roast</span><span class="item-price">₹140</span></div><p class="item-desc">Rich and aromatic mutton roast.</p></div>
                <div class="menu-item"><div class="item-header"><span class="item-name">Liver Roast</span><span class="item-price">₹80</span></div><p class="item-desc">Spiced liver cooked to perfection.</p></div>
            </div>
        </div>

        <div class="menu-category">
            <h3>Chicken Specialties</h3>
            <div class="menu-grid">
                <div class="menu-item"><div class="item-header"><span class="item-name">Chicken Roast</span><span class="item-price">₹150</span></div><p class="item-desc">Spicy roasted chicken, a signature dish.</p></div>
                <div class="menu-item"><div class="item-header"><span class="item-name">Chicken Masala</span><span class="item-price">₹160</span></div><p class="item-desc">Classic chicken semi-gravy.</p></div>
                <div class="menu-item"><div class="item-header"><span class="item-name">Chicken Kuruma</span><span class="item-price">₹120</span></div><p class="item-desc">Mild, creamy chicken curry.</p></div>
                <div class="menu-item"><div class="item-header"><span class="item-name">Chicken Fry</span><span class="item-price">₹80</span></div><p class="item-desc">Marinated and deep-fried chicken pieces.</p></div>
                <div class="menu-item"><div class="item-header"><span class="item-name">Chicken Lollipop</span><span class="item-price">₹50</span></div><p class="item-desc">Indo-Chinese style chicken wings (Small Portion).</p></div>
                <div class="menu-item"><div class="item-header"><span class="item-name">Chicken Lollipop</span><span class="item-price">₹200</span></div><p class="item-desc">Indo-Chinese style chicken wings (Large Portion).</p></div>
                <div class="menu-item"><div class="item-header"><span class="item-name">Chicken Kadai</span><span class="item-price">₹200</span></div><p class="item-desc">Chicken cooked in a kadai (wok) with bell peppers and spices.</p></div>
                <div class="menu-item"><div class="item-header"><span class="item-name">Chicken Curry</span><span class="item-price">₹80</span></div><p class="item-desc">Traditional home-style chicken curry.</p></div>
                <div class="menu-item"><div class="item-header"><span class="item-name">Malabar Chicken</span><span class="item-price">₹150</span></div><p class="item-desc">Spicy chicken prepared in authentic Malabar style.</p></div>
                <div class="menu-item"><div class="item-header"><span class="item-name">Chicken Chettinadu</span><span class="item-price">₹200</span></div><p class="item-desc">Fiery chicken curry with roasted spices.</p></div>
                <div class="menu-item"><div class="item-header"><span class="item-name">Chicken Kuttukoi</span><span class="item-price">₹120</span></div><p class="item-desc">A special house chicken preparation.</p></div>
                <div class="menu-item"><div class="item-header"><span class="item-name">Chicken Kondattom</span><span class="item-price">₹180</span></div><p class="item-desc">Dry, crispy chicken preparation.</p></div>
                <div class="menu-item"><div class="item-header"><span class="item-name">Chilly Chicken</span><span class="item-price">₹150</span></div><p class="item-desc">Hot and spicy Indo-Chinese chicken (Gravy).</p></div>
                <div class="menu-item"><div class="item-header"><span class="item-name">Chilli Chicken Dry</span><span class="item-price">₹180</span></div><p class="item-desc">Hot and spicy Indo-Chinese chicken (Dry).</p></div>
                <div class="menu-item"><div class="item-header"><span class="item-name">Chicken 65 (Half)</span><span class="item-price">₹50</span></div><p class="item-desc">Spicy deep-fried chicken starter (Half Portion).</p></div>
                <div class="menu-item"><div class="item-header"><span class="item-name">Garlic Chicken</span><span class="item-price">₹200</span></div><p class="item-desc">Chicken cooked in a heavy garlic sauce.</p></div>
                <div class="menu-item"><div class="item-header"><span class="item-name">Chicken Manjuri (Manchurian)</span><span class="item-price">₹150</span></div><p class="item-desc">Sweet and sour Indo-Chinese favorite.</p></div>
                <div class="menu-item"><div class="item-header"><span class="item-name">Pepper Chicken</span><span class="item-price">₹180</span></div><p class="item-desc">Chicken cooked with crushed black pepper.</p></div>
                <div class="menu-item"><div class="item-header"><span class="item-name">Butter Chicken</span><span class="item-price">₹200</span></div><p class="item-desc">Creamy, tomato-based classic Indian curry.</p></div>
                <div class="menu-item"><div class="item-header"><span class="item-name">Szechuan Chicken</span><span class="item-price">₹140</span></div><p class="item-desc">Chicken tossed in spicy Szechuan sauce.</p></div>
                <div class="menu-item"><div class="item-header"><span class="item-name">Chicken Mughlai / Mughlai Chicken</span><span class="item-price">₹140</span></div><p class="item-desc">Rich, creamy Mughlai style chicken curry.</p></div>
                <div class="menu-item"><div class="item-header"><span class="item-name">Lemon Chicken</span><span class="item-price">₹130</span></div><p class="item-desc">Chicken in a light, tangy lemon sauce.</p></div>
            </div>
        </div>

        <div class="menu-category">
            <h3>Seafood & Other Meat</h3>
            <div class="menu-grid">
                <div class="menu-item"><div class="item-header"><span class="item-name">Kozhuva Fry</span><span class="item-price">₹70</span></div><p class="item-desc">Anchovies marinated and fried until crispy.</p></div>
                <div class="menu-item"><div class="item-header"><span class="item-name">Kada Fry (Quail)</span><span class="item-price">₹100</span></div><p class="item-desc">Marinated and spiced quail fry.</p></div>
                <div class="menu-item"><div class="item-header"><span class="item-name">Kakka (Clams)</span><span class="item-price">₹60</span></div><p class="item-desc">Spicy roasted clams preparation.</p></div>
                <div class="menu-item"><div class="item-header"><span class="item-name">Fish Fry</span><span class="item-price">₹70</span></div><p class="item-desc">Marinated fish pieces fried to perfection (price per piece).</p></div>
                <div class="menu-item"><div class="item-header"><span class="item-name">Fish Masala</span><span class="item-price">₹80</span></div><p class="item-desc">Fish cooked in a thick aromatic gravy.</p></div>
                <div class="menu-item"><div class="item-header"><span class="item-name">Chilly Fish</span><span class="item-price">₹120</span></div><p class="item-desc">Hot and tangy Indo-Chinese fish.</p></div>
                <div class="menu-item"><div class="item-header"><span class="item-name">Prawns Roast</span><span class="item-price">₹80</span></div><p class="item-desc">Prawns roasted in a spicy masala.</p></div>
                <div class="menu-item"><div class="item-header"><span class="item-name">Squid Roast</span><span class="item-price">₹60</span></div><p class="item-desc">Tender squid pieces roasted in spices.</p></div>
            </div>
        </div>

        <div class="menu-category">
            <h3>Vegetarian & Paneer Specials</h3>
            <div class="menu-grid">
                <div class="menu-item"><div class="item-header"><span class="item-name">Chilly Paneer</span><span class="item-price">₹90</span></div><p class="item-desc">Paneer cubes tossed in a spicy chili sauce.</p></div>
                <div class="menu-item"><div class="item-header"><span class="item-name">Paneer Masala</span><span class="item-price">₹120</span></div><p class="item-desc">Creamy paneer and tomato gravy.</p></div>
                <div class="menu-item"><div class="item-header"><span class="item-name">Kadai Paneer</span><span class="item-price">₹110</span></div><p class="item-desc">Paneer cooked with bell peppers in a rich kadai masala.</p></div>
                <div class="menu-item"><div class="item-header"><span class="item-name">Veg Masala</span><span class="item-price">₹40</span></div><p class="item-desc">Mixed vegetables cooked in a spicy masala.</p></div>
                <div class="menu-item"><div class="item-header"><span class="item-name">Veg Kurma</span><span class="item-price">₹30</span></div><p class="item-desc">Mild, creamy vegetable curry.</p></div>
                <div class="menu-item"><div class="item-header"><span class="item-name">Kadala Masala</span><span class="item-price">₹40</span></div><p class="item-desc">Black chickpeas cooked in a flavorful masala.</p></div>
                <div class="menu-item"><div class="item-header"><span class="item-name">Dragon Paneer</span><span class="item-price">₹150</span></div><p class="item-desc">Spicy, tangy paneer starter.</p></div>
                <div class="menu-item"><div class="item-header"><span class="item-name">Chilly Gobi</span><span class="item-price">₹80</span></div><p class="item-desc">Cauliflower florets tossed in chili sauce.</p></div>
                <div class="menu-item"><div class="item-header"><span class="item-name">Gobi Manjuri (Manchurian)</span><span class="item-price">₹90</span></div><p class="item-desc">Cauliflower dumplings in a tangy sauce.</p></div>
                <div class="menu-item"><div class="item-header"><span class="item-name">Green Salad</span><span class="item-price">₹50</span></div><p class="item-desc">Freshly chopped mixed vegetables.</p></div>
            </div>
        </div>
        
        <div class="menu-category">
            <h3>Arabian Grilled Specials & Rolls</h3>
            <div class="menu-grid">
                <div class="menu-item"><div class="item-header"><span class="item-name">Alfahm Quarter</span><span class="item-price">₹110</span></div><p class="item-desc">Quarter portion of Charcoal Grilled Chicken.</p></div>
                <div class="menu-item"><div class="item-header"><span class="item-name">Alfahm Half</span><span class="item-price">₹240</span></div><p class="item-desc">Half portion of Charcoal Grilled Chicken.</p></div>
                <div class="menu-item"><div class="item-header"><span class="item-name">Alfahm Full</span><span class="item-price">₹400</span></div><p class="item-desc">Full portion of Charcoal Grilled Chicken.</p></div>
                <div class="menu-item"><div class="item-header"><span class="item-name">Shawai Quarter</span><span class="item-price">₹150</span></div><p class="item-desc">Quarter portion of Arabic Grilled Chicken.</p></div>
                <div class="menu-item"><div class="item-header"><span class="item-name">Shawai Half</span><span class="item-price">₹300</span></div><p class="item-desc">Half portion of Arabic Grilled Chicken.</p></div>
                <div class="menu-item"><div class="item-header"><span class="item-name">Shawai Full</span><span class="item-price">₹550</span></div><p class="item-desc">Full portion of Arabic Grilled Chicken.</p></div>
                <div class="menu-item"><div class="item-header"><span class="item-name">Alfahm Mandi</span><span class="item-price">₹220</span></div><p class="item-desc">Alfahm served with Mandi Rice.</p></div>
                <div class="menu-item"><div class="item-header"><span class="item-name">Shawai Mandi Quarter</span><span class="item-price">₹220</span></div><p class="item-desc">Shawai Chicken served with Mandi Rice.</p></div>
                <div class="menu-item"><div class="item-header"><span class="item-name">Alfahm Mandi Full</span><span class="item-price">₹850</span></div><p class="item-desc">Full Alfahm served with large portion of Mandi Rice.</p></div>
                <div class="menu-item"><div class="item-header"><span class="item-name">Shawarma Roll</span><span class="item-price">₹80</span></div><p class="item-desc">Spiced meat wrapped in bread.</p></div>
                <div class="menu-item"><div class="item-header"><span class="item-name">Shawarma Plate</span><span class="item-price">₹130</span></div><p class="item-desc">Meat, bread, and sides served on a plate.</p></div>
                <div class="menu-item"><div class="item-header"><span class="item-name">Rumali Roll</span><span class="item-price">₹130</span></div><p class="item-desc">Meat filling wrapped in thin rumali roti.</p></div>
                <div class="menu-item"><div class="item-header"><span class="item-name">Rumali Plate</span><span class="item-price">₹160</span></div><p class="item-desc">Meat and rumali roti served on a plate.</p></div>
                <div class="menu-item"><div class="item-header"><span class="item-name">Meat Rumali</span><span class="item-price">₹110</span></div><p class="item-desc">Rumali roti with a simple meat filling.</p></div>
                <div class="menu-item"><div class="item-header"><span class="item-name">Rumali Cheese</span><span class="item-price">₹130</span></div><p class="item-desc">Rumali roti with cheese filling.</p></div>
            </div>
        </div>

        <div class="menu-category">
            <h3>Eggs, Soups & Drinks</h3>
            <div class="menu-grid">
                <div class="menu-item"><div class="item-header"><span class="item-name">Egg Chilly</span><span class="item-price">₹60</span></div><p class="item-desc">Boiled eggs tossed in chili sauce.</p></div>
                <div class="menu-item"><div class="item-header"><span class="item-name">Egg Masala</span><span class="item-price">₹40</span></div><p class="item-desc">Boiled eggs in a semi-gravy masala.</p></div>
                <div class="menu-item"><div class="item-header"><span class="item-name">Chicken Soup</span><span class="item-price">₹120</span></div><p class="item-desc">Warm, savory clear chicken soup.</p></div>
                <div class="menu-item"><div class="item-header"><span class="item-name">Lemon Tea</span><span class="item-price">₹15</span></div><p class="item-desc">Refreshing hot tea with lemon.</p></div>
                <div class="menu-item"><div class="item-header"><span class="item-name">Mint Lime</span><span class="item-price">₹30</span></div><p class="item-desc">Cooling lime juice with fresh mint.</p></div>
                <div class="menu-item"><div class="item-header"><span class="item-name">Pineapple Juice</span><span class="item-price">₹70</span></div><p class="item-desc">Freshly squeezed pineapple juice.</p></div>
                <div class="menu-item"><div class="item-header"><span class="item-name">Carrot Juice</span><span class="item-price">₹50</span></div><p class="item-desc">Freshly squeezed carrot juice.</p></div>
                <div class="menu-item"><div class="item-header"><span class="item-name">Musambi Juice</span><span class="item-price">₹70</span></div><p class="item-desc">Freshly squeezed sweet lime juice.</p></div>
                <div class="menu-item"><div class="item-header"><span class="item-name">Watermelon Juice</span><span class="item-price">₹40</span></div><p class="item-desc">Freshly squeezed watermelon juice.</p></div>
                <div class="menu-item"><div class="item-header"><span class="item-name">Orange Juice</span><span class="item-price">₹70</span></div><p class="item-desc">Freshly squeezed orange juice.</p></div>
                <div class="menu-item"><div class="item-header"><span class="item-name">Grape Juice</span><span class="item-price">₹60</span></div><p class="item-desc">Freshly squeezed grape juice.</p></div>
                <div class="menu-item"><div class="item-header"><span class="item-name">Sharjah Shake</span><span class="item-price">₹70</span></div><p class="item-desc">Popular rich and creamy signature shake.</p></div>
                <div class="menu-item"><div class="item-header"><span class="item-name">Mango Shake</span><span class="item-price">₹70</span></div><p class="item-desc">Thick, sweet mango flavored shake.</p></div>
                <div class="menu-item"><div class="item-header"><span class="item-name">Apple Shake</span><span class="item-price">₹80</span></div><p class="item-desc">Refreshing apple blended shake.</p></div>
                <div class="menu-item"><div class="item-header"><span class="item-name">Papaya Shake</span><span class="item-price">₹40</span></div><p class="item-desc">Healthy and creamy papaya shake.</p></div>
                <div class="menu-item"><div class="item-header"><span class="item-name">Musambi Shake</span><span class="item-price">₹70</span></div><p class="item-desc">Sweet lime blended shake.</p></div>
                <div class="menu-item"><div class="item-header"><span class="item-name">Samam Shake</span><span class="item-price">₹50</span></div><p class="item-desc">Cool and refreshing seasonal shake.</p></div>
                <div class="menu-item"><div class="item-header"><span class="item-name">Oreo Shake</span><span class="item-price">₹80</span></div><p class="item-desc">Classic creamy chocolate Oreo shake.</p></div>
            </div>
        </div>
        
        <div class="menu-category">
            <h3>Fried Rice & Noodles</h3>
            <div class="menu-grid">
                <div class="menu-item"><div class="item-header"><span class="item-name">Veg Fried Rice</span><span class="item-price">₹120</span></div><p class="item-desc">Rice tossed with fresh vegetables and sauces.</p></div>
                <div class="menu-item"><div class="item-header"><span class="item-name">Egg Fried Rice</span><span class="item-price">₹120</span></div><p class="item-desc">Rice tossed with egg and light seasoning.</p></div>
                <div class="menu-item"><div class="item-header"><span class="item-name">Chicken Fried Rice</span><span class="item-price">₹150</span></div><p class="item-desc">Rice tossed with chicken and savory sauces.</p></div>
                <div class="menu-item"><div class="item-header"><span class="item-name">Beef Fried Rice</span><span class="item-price">₹150</span></div><p class="item-desc">Rice tossed with beef pieces and classic seasoning.</p></div>
                <div class="menu-item"><div class="item-header"><span class="item-name">Mixed Fried Rice</span><span class="item-price">₹180</span></div><p class="item-desc">Rice tossed with mixed meats and shrimp.</p></div>
                <div class="menu-item"><div class="item-header"><span class="item-name">Veg Noodles</span><span class="item-price">₹120</span></div><p class="item-desc">Noodles tossed with seasonal vegetables.</p></div>
                <div class="menu-item"><div class="item-header"><span class="item-name">Egg Noodles</span><span class="item-price">₹120</span></div><p class="item-desc">Noodles tossed with scrambled egg.</p></div>
                <div class="menu-item"><div class="item-header"><span class="item-name">Chicken Noodles</span><span class="item-price">₹140</span></div><p class="item-desc">Noodles tossed with chicken slices.</p></div>
                <div class="menu-item"><div class="item-header"><span class="item-name">Beef Noodles</span><span class="item-price">₹140</span></div><p class="item-desc">Noodles tossed with savory beef pieces.</p></div>
                <div class="menu-item"><div class="item-header"><span class="item-name">Mixed Noodles</span><span class="item-price">₹160</span></div><p class="item-desc">Noodles tossed with mixed meats and seafood.</p></div>
            </div>
        </div>
        
        <div class="menu-category">
            <h3>Curries & Gravies</h3>
            <div class="menu-grid">
                <div class="menu-item"><div class="item-header"><span class="item-name">Kadala Curry</span><span class="item-price">₹40</span></div><p class="item-desc">Black chickpeas curry, a classic pairing.</p></div>
                <div class="menu-item"><div class="item-header"><span class="item-name">Pease Curry</span><span class="item-price">₹40</span></div><p class="item-desc">Green peas cooked in a thick gravy.</p></div>
                <div class="menu-item"><div class="item-header"><span class="item-name">Potato Curry</span><span class="item-price">₹30</span></div><p class="item-desc">Simple yet comforting potato gravy.</p></div>
                <div class="menu-item"><div class="item-header"><span class="item-name">Pease Masala</span><span class="item-price">₹40</span></div><p class="item-desc">Spicy green peas masala.</p></div>
                <div class="menu-item"><div class="item-header"><span class="item-name">Tomato Fry</span><span class="item-price">₹60</span></div><p class="item-desc">Spicy and tangy thick tomato preparation.</p></div>
                <div class="menu-item"><div class="item-header"><span class="item-name">Mashroom Masala</span><span class="item-price">₹100</span></div><p class="item-desc">Mushrooms cooked in a creamy, aromatic masala.</p></div>
            </div>
        </div>
        
    </section>

    <section id="about" class="info-section">
        <h2 class="section-title" style="color:var(--text-light)">Visit Us</h2>
        <div class="info-grid">
            <div class="hours">
                <h3>Opening Hours</h3>
                <p>**Dine-in:** 10:00 am - 11:00 pm (Daily)</p>
                <p>**Delivery:** 11:00 am - 10:00 pm</p>
                <p>**Takeout:** 11:30 am - 11:00 pm</p>
            </div>
            <div class="location">
                <h3>Location</h3>
                <p>Ambalakadav Kettezhathkadav Rd, Nettoor,</p>
                <p>Maradu, Kochi, Ernakulam, Kerala 682040</p>
            </div>
            <div class="contact">
                <h3>Contact</h3>
                <p>**Phone:** <a href="tel:08593923750" style="color: var(--primary-color); font-weight: bold;">08593923750</a></p>
            </div>
        </div>
    </section>

    <footer>
        <p>&copy; 2025 Hotel Misbah. All rights reserved.</p>
    </footer>

    <script>
        // Smooth scrolling for navigation links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
            });
        });
    </script>
</body>
</html>

<!--
**hotelmisbah/Hotelmisbah** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
