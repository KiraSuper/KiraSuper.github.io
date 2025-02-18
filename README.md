
<!DOCTYPE html>
<html lang="pl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Natalia Rypińska - Psycholog | Olsztyn</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Arial', sans-serif;
        }
        body {
            line-height: 1.6;
            color: #333;
            background-color: #f8f9fa;
        }

        /* Menu nawigacyjne */
        .menu-btn {
            position: fixed;
            left: 20px;
            top: 20px;
            z-index: 1000;
            cursor: pointer;
            background: #007bff;
            padding: 10px;
            border-radius: 5px;
            color: white;
        }

        .side-menu {
            position: fixed;
            left: -250px;
            top: 0;
            width: 250px;
            height: 100%;
            background: #fff;
            box-shadow: 2px 0 5px rgba(0,0,0,0.1);
            transition: 0.3s;
            z-index: 999;
            padding-top: 20px;
        }

        .side-menu.active {
            left: 0;
        }

        .side-menu a {
            display: block;
            padding: 15px;
            text-decoration: none;
            color: #333;
            border-bottom: 1px solid #eee;
        }

        /* Styl sekcji */
        .page {
            display: none;
            padding: 60px 20px;
            max-width: 1200px;
            margin: 0 auto;
        }

        .page.active {
            display: block;
        }

        /* Ozdobne czterolistne kończyny */
        .left-decoration, .right-decoration {
            position: absolute;
            width: 120px;
            height: 100%;
            top: 100px;
            opacity: 0.5;
            pointer-events: none;
        }

        /* Obrazki w sekcjach */
        .service-item img {
            width: 50px;
            height: 50px;
            margin-right: 15px;
            vertical-align: middle;
        }

        /* Styl responsywności */
        @media (max-width: 768px) {
            .left-decoration, .right-decoration {
                display: none;
            }
        }
    </style>
</head>
<body>

    <!-- Przycisk menu -->
    <div class="menu-btn" onclick="toggleMenu()">☰ Menu</div>

    <!-- Menu boczne -->
    <nav class="side-menu">
        <a href="#home" onclick="showPage('home')">Strona główna</a>
        <a href="#about" onclick="showPage('about')">O mnie</a>
        <a href="#contact" onclick="showPage('contact')">Umów się</a>
    </nav>

    <!-- Strona główna -->
    <section id="home" class="page active">
        <div class="left-decoration"></div>
        <div class="right-decoration"></div>
        <h2>Rodzaje terapii</h2>
        <div class="service-item">
            <img src="consultation.svg" alt="Konsultacje">
            <h3>Konsultacje psychologiczne</h3>
            <p>Indywidualne spotkania...</p>
        </div>
        
        <div class="service-item">
            <img src="social-skills.svg" alt="Trening Umiejętności Społecznych">
            <h3>Trening Umiejętności Społecznych</h3>
            <p>Zajęcia grupowe...</p>
        </div>
        
        <div class="service-item">
            <img src="family-support.svg" alt="Wsparcie dla rodziców">
            <h3>Wsparcie dla rodziców</h3>
            <p>Konsultacje i warsztaty...</p>
        </div>
    </section>

    <!-- O mnie -->
    <section id="about" class="page">
        <h2>O mnie</h2>
        <div class="experience-item">
            <h3>Wykształcenie</h3>
            <img src="education.svg" alt="Wykształcenie">
        </div>
        
        <div class="experience-item">
            <h3>Umiejętności</h3>
            <img src="skills.svg" alt="Umiejętności">
        </div>
        
        <div class="experience-item">
            <h3>Zainteresowania</h3>
            <img src="music.svg" alt="Muzyka">
        </div>
    </section>

    <!-- Umów się -->
    <section id="contact" class="page">
        <h2>Umów się</h2>
        <img src="heart.svg" alt="Serduszko">
        <img src="heart.svg" alt="Serduszko" style="position: relative; left: -20px;">
        <img src="heart.svg" alt="Serduszko" style="position: relative; top: 30px; left: 50%; transform: translateX(-50%);">
    </section>

    <script>
        function toggleMenu() {
            document.querySelector('.side-menu').classList.toggle('active');
        }

        function showPage(pageId) {
            document.querySelectorAll('.page').forEach(page => {
                page.classList.remove('active');
            });
            document.getElementById(pageId).classList.add('active');
            toggleMenu();
        }
    </script>

</body>
</html>
