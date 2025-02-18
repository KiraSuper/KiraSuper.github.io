
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
            background: linear-gradient(rgba(255,255,255,0.93), rgba(255,255,255,0.93)), 
                        url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='100' height='100' viewBox='0 0 100 100'%3E%3Cpath fill='%2378c272' opacity='0.1' d='M15,20 Q30,5 45,20 T75,20 Q60,35 75,50 T75,80 Q60,65 45,80 T15,80 Q30,65 15,50 T15,20'/%3E%3C/svg%3E");
        }

        /* Menu hamburger */
        .menu-btn {
            position: fixed;
            left: 20px;
            top: 20px;
            z-index: 1000;
            cursor: pointer;
            background: #f8f9fa;
            padding: 10px;
            border-radius: 5px;
        }

        .menu-btn span {
            display: block;
            width: 25px;
            height: 3px;
            background: #333;
            margin: 5px 0;
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
            overflow-y: auto;
            padding: 20px 0;
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

        /* Zdjęcie w okręgu */
        .profile-circle {
            width: 200px;
            height: 200px;
            border-radius: 50%;
            overflow: hidden;
            margin: 40px auto 20px;
            border: 4px solid #fff;
            box-shadow: 0 0 10px rgba(0,0,0,0.1);
        }

        .profile-circle img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }

        /* Dodatkowe zdjęcie na stronie głównej */
        .profile-circle-home {
            width: 150px;
            height: 150px;
            border-radius: 50%;
            overflow: hidden;
            margin: 20px;
            border: 4px solid #fff;
            box-shadow: 0 0 10px rgba(0,0,0,0.1);
            position: absolute;
            bottom: 60px;
            right: 30px;
        }

        .profile-circle-home img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }

        /* Styl pozostałych elementów */
        .page {
            display: none;
            padding: 80px 20px 40px;
            max-width: 1200px;
            margin: 0 auto;
            position: relative;
        }

        .page.active {
            display: block;
        }

        /* Ozdobne listki i kwiaty */
        .left-decoration, .right-decoration {
            position: absolute;
            width: 120px;
            height: 100%;
            top: 100px;
            opacity: 0.5;
            pointer-events: none;
        }

        .left-decoration {
            left: -20px;
            background: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='100' height='600' viewBox='0 0 100 600'%3E%3Cpath fill='%2378c272' opacity='0.3' d='M30,50 Q50,30 70,50 Q90,70 70,90 Q50,110 30,90 Q10,70 30,50 Z'/%3E%3Cpath fill='%2378c272' opacity='0.3' d='M20,200 Q40,180 60,200 Q80,220 60,240 Q40,260 20,240 Q0,220 20,200 Z'/%3E%3Cpath fill='%2378c272' opacity='0.3' d='M25,350 Q45,330 65,350 Q85,370 65,390 Q45,410 25,390 Q5,370 25,350 Z'/%3E%3Cpath fill='%2378c272' opacity='0.3' d='M30,500 Q50,480 70,500 Q90,520 70,540 Q50,560 30,540 Q10,520 30,500 Z'/%3E%3C/svg%3E") repeat-y;
        }

        .right-decoration {
            right: -20px;
            background: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='100' height='600' viewBox='0 0 100 600'%3E%3Cpath fill='%2378c272' opacity='0.3' d='M30,50 Q50,30 70,50 Q90,70 70,90 Q50,110 30,90 Q10,70 30,50 Z'/%3E%3Cpath fill='%23a0d995' opacity='0.3' d='M20,200 Q0,180 20,160 Q40,140 60,160 Q80,180 60,200 Q40,220 20,200 Z'/%3E%3Cpath fill='%2378c272' opacity='0.3' d='M25,350 Q45,330 65,350 Q85,370 65,390 Q45,410 25,390 Q5,370 25,350 Z'/%3E%3Cpath fill='%23a0d995' opacity='0.3' d='M45,500 Q65,480 85,500 Q105,520 85,540 Q65,560 45,540 Q25,520 45,500 Z'/%3E%3C/svg%3E") repeat-y;
        }

        /* Style z Kod1 */
        header {
            background: #f8f9fa;
            padding: 20px;
            text-align: center;
            border-bottom: 2px solid #e9ecef;
        }
        
        section {
            padding: 40px 20px;
            margin: 0 auto;
        }
        
        .hero {
            text-align: center;
            padding: 60px 20px;
            background: #e9f5fe;
        }
        
        footer {
            background: #343a40;
            color: white;
            text-align: center;
            padding: 20px;
            margin-top: 40px;
        }
        
        .contact-info {
            background: #f8f9fa;
            padding: 20px;
            border-radius: 5px;
            margin: 20px 0;
        }
        
        .experience-item {
            margin: 20px 0;
            padding: 15px;
            border-left: 3px solid #007bff;
        }
        
        form {
            max-width: 600px;
            margin: 0 auto;
        }
        
        input, textarea {
            width: 100%;
            padding: 10px;
            margin: 10px 0;
            border: 1px solid #ddd;
            border-radius: 4px;
        }
        
        button {
            background: #007bff;
            color: white;
            padding: 10px 20px;
            border: none;
            border-radius: 4px;
            cursor: pointer;
        }
        
        .banner-image {
            width: 100%;
            max-height: 300px;
            object-fit: cover;
        }
        
        h2 {
            margin-bottom: 20px;
            color: #007bff;
        }
        
        h3 {
            margin-top: 25px;
            margin-bottom: 10px;
            color: #555;
        }
        
        .service-item {
            margin: 20px 0;
            padding: 15px;
            border-left: 3px solid #28a745;
        }
        
        .pricing-table {
            width: 100%;
            border-collapse: collapse;
            margin: 25px 0;
        }
        
        .pricing-table th, .pricing-table td {
            padding: 12px 15px;
            border: 1px solid #ddd;
            text-align: left;
        }
        
        .pricing-table th {
            background-color: #f8f9fa;
            font-weight: bold;
        }
        
        .pricing-table tr:nth-child(even) {
            background-color: #f2f2f2;
        }
        
        /* Dodatkowe dekoracje */
        .flower-decoration {
            width: 150px;
            height: 150px;
            background: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='150' height='150' viewBox='0 0 150 150'%3E%3Ccircle cx='75' cy='75' r='25' fill='%23a0d995' opacity='0.6'/%3E%3Cpath fill='%2378c272' opacity='0.4' d='M75,25 Q90,50 115,50 Q90,65 90,90 Q75,65 50,65 Q65,40 50,15 Q75,40 100,15 Q75,25 75,25 Z'/%3E%3Cpath fill='%2378c272' opacity='0.4' d='M75,125 Q60,100 35,100 Q60,85 60,60 Q75,85 100,85 Q85,110 100,135 Q75,110 50,135 Q75,125 75,125 Z'/%3E%3C/svg%3E");
            position: absolute;
            opacity: 0.8;
        }
        
        .university-image {
            width: 150px;
            height: 150px;
            background: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='150' height='150' viewBox='0 0 150 150'%3E%3Cpath fill='%2378c272' opacity='0.4' d='M75,10 L10,50 L75,90 L140,50 Z'/%3E%3Cpath fill='%2378c272' opacity='0.4' d='M30,55 L30,110 L50,115 L50,55 Z'/%3E%3Cpath fill='%2378c272' opacity='0.4' d='M60,55 L60,120 L80,125 L80,55 Z'/%3E%3Cpath fill='%2378c272' opacity='0.4' d='M90,55 L90,120 L110,115 L110,55 Z'/%3E%3Cpath fill='%2378c272' opacity='0.4' d='M20,130 L130,130 L140,140 L10,140 Z'/%3E%3C/svg%3E");
            position: absolute;
            right: 50px;
            top: 350px;
            opacity: 0.7;
        }
        
        .brain-image {
            width: 150px;
            height: 150px;
            background: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='150' height='150' viewBox='0 0 150 150'%3E%3Cpath fill='%2378c272' opacity='0.5' d='M75,20 Q95,5 110,20 Q125,40 110,60 Q130,75 115,95 Q95,110 75,95 Q55,110 35,95 Q20,75 40,60 Q25,40 40,20 Q55,5 75,20 Z'/%3E%3Cpath fill='%23ffffff' opacity='0.3' d='M75,25 Q90,15 100,25 Q110,40 100,55 Q115,65 105,80 Q90,90 75,80 Q60,90 45,80 Q35,65 50,55 Q40,40 50,25 Q60,15 75,25 Z'/%3E%3C/svg%3E");
            position: absolute;
            right: 50px;
            top: 620px;
            opacity: 0.7;
        }
        
        .heart-image {
            width: 150px;
            height: 150px;
            background: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='150' height='150' viewBox='0 0 150 150'%3E%3Cpath fill='%2378c272' opacity='0.5' d='M75,120 Q40,85 25,65 Q10,45 25,25 Q40,5 60,20 Q70,30 75,40 Q80,30 90,20 Q110,5 125,25 Q140,45 125,65 Q110,85 75,120 Z'/%3E%3C/svg%3E");
            position: absolute;
            right: 50px;
            top: 200px;
            opacity: 0.7;
        }
        
        .smile-image {
            width: 150px;
            height: 150px;
            background: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='150' height='150' viewBox='0 0 150 150'%3E%3Ccircle cx='75' cy='75' r='60' fill='%2378c272' opacity='0.3'/%3E%3Ccircle cx='50' cy='60' r='5' fill='%23333' opacity='0.8'/%3E%3Ccircle cx='100' cy='60' r='5' fill='%23333' opacity='0.8'/%3E%3Cpath fill='none' stroke='%23333' stroke-width='5' opacity='0.8' d='M50,100 Q75,120 100,100'/%3E%3C/svg%3E");
            position: absolute;
            right: 50px;
            top: 150px;
            opacity: 0.7;
        }

        @media (max-width: 768px) {
            nav a {
                display: block;
                margin: 10px 0;
            }
            .left-decoration, .right-decoration, 
            .flower-decoration, .university-image, 
            .brain-image, .heart-image, .smile-image {
                display: none;
            }
            .profile-circle-home {
                position: relative;
                bottom: auto;
                right: auto;
                margin: 20px auto;
            }
        }
    </style>
</head>
<body>
    <!-- Przycisk menu -->
    <div class="menu-btn" onclick="toggleMenu()">
        <span></span>
        <span></span>
        <span></span>
    </div>

    <!-- Wysuwane menu -->
    <nav class="side-menu">
        <div class="profile-circle">
            <img src="twoje-zdjecie.jpg" alt="Natalia Rypińska">
        </div>
        <a href="#home" onclick="showPage('home')">Strona główna</a>
        <a href="#about" onclick="showPage('about')">O mnie</a>
        <a href="#offer" onclick="showPage('offer')">Oferta</a>
        <a href="#contact" onclick="showPage('contact')">Umów się</a>
    </nav>

    <!-- Podstrony -->
    <section id="home" class="page active">
        <div class="left-decoration"></div>
        <div class="right-decoration"></div>
        
        <img src="banner-image.jpg" alt="Gabinet psychologiczny" class="banner-image">
        <h1>Witaj w moim gabinecie</h1>
        <p>Specjalizuję się w konsultacjach psychologicznych dla dzieci, młodzieży i dorosłych. Oferuję profesjonalne wsparcie w radzeniu sobie z trudnościami życiowymi i emocjonalnymi.</p>
        
        <h2>Rodzaje terapii</h2>
        <div class="service-item">
            <h3>Konsultacje psychologiczne</h3>
            <p>Indywidualne spotkania mające na celu diagnozę problemu i określenie planu terapeutycznego.</p>
        </div>
        
        <div class="service-item">
            <h3>Trening Umiejętności Społecznych</h3>
            <p>Zajęcia grupowe dla dzieci i młodzieży, które pomagają rozwinąć kompetencje społeczne.</p>
        </div>
        
        <div class="service-item">
            <h3>Wsparcie dla rodziców</h3>
            <p>Konsultacje i warsztaty dla rodziców potrzebujących pomocy w wychowaniu dzieci.</p>
        </div>
        
        <div class="contact-info">
            <p>📧 n.rypinska99@gmail.com</p>
            <p>📱 511 819 043</p>
            <p>📍 Olsztyn</p>
        </div>
        
        <div class="profile-circle-home">
            <img src="twoje-zdjecie.jpg" alt="Natalia Rypińska">
        </div>
    </section>

    <section id="about" class="page">
        <div class="left-decoration"></div>
        <div class="right-decoration"></div>
        
        <h2>O mnie</h2>
        
        <div class="experience-item">
            <h3>Doświadczenie zawodowe</h3>
            <div class="flower-decoration" style="right: 20px; top: 100px;"></div>
            
            <p><strong>Aktualnie pracuję jako:</strong></p>
            <ul>
                <li>Psycholog w Środowiskowym Domu Samopomocy w Marcinkowie (od 10.2024)</li>
                <li>Psycholog w punktach konsultacyjnych dla dzieci i młodzieży w gminach Purda i Stawiguda (od 09.2024 i 03.2024)</li>
                <li>Psycholog szkolny w Zespole Szkolno-Przedszkolnym w Purdzie (od 09.2024)</li>
                <li>Psycholog w Centrum psychoterapii Dariusz Wasiński w Olsztynie (od 09.2019)</li>
            </ul>
            
            <p><strong>Główne obszary działania:</strong></p>
            <ul>
                <li>Diagnoza psychologiczna i terapia</li>
                <li>Prowadzenie zajęć grupowych i Treningów Umiejętności Społecznych</li>
                <li>Konsultacje indywidualne dla dzieci, młodzieży i dorosłych</li>
                <li>Poradnictwo i wsparcie dla rodziców</li>
                <li>Koordynacja pracy praktykujących studentów</li>
            </ul>
        </div>
        
        <div class="experience-item">
            <h3>Wykształcenie</h3>
            <div class="university-image"></div>
            
            <p><strong>Uczelnia:</strong> Uniwersytet SWPS wydział zamiejscowy w Sopocie</p>
            <p><strong>Kierunek:</strong> psychologia</p>
            <p><strong>Specjalizacja:</strong> kliniczna</p>
            <p><strong>Poziom wykształcenia:</strong> magister</p>
            <p><strong>Okres:</strong> 10.2018 – 09.2023 (5 lat)</p>
        </div>
        
        <div class="experience-item">
            <h3>Umiejętności</h3>
            <div class="brain-image"></div>
            
            <ul>
                <li>Przygotowywanie ćwiczeń oraz zabaw grupowych</li>
                <li>Praca w zespole</li>
                <li>Wysoka empatia</li>
                <li>Wytrwałość w dążeniu do celu</li>
                <li>Kreatywność</li>
                <li>Otwartość punktualność i dobra organizacja czasu</li>
                <li>Dbałość o szczegóły</li>
                <li>Łatwość w nawiązywaniu kontaktów i podtrzymywaniu relacji</li>
            </ul>
        </div>
        
        <div class="experience-item">
            <h3>Znajomość języków</h3>
            <p><strong>angielski:</strong> poziom zaawansowany</p>
            <p><strong>hiszpański:</strong> poziom podstawowy</p>
        </div>
        
        <div class="experience-item">
            <h3>Aktywność dodatkowa</h3>
            <p><strong>Okres:</strong> 05.2020 – 12.2020 (8 mies.)</p>
            <p><strong>Organizacja:</strong> Studenci studentom, Sopot</p>
            <p>Przygotowywanie i prowadzenie warsztatów dla studentów pierwszego roku o tematyce psychologicznej.</p>
        </div>
        
        <div class="experience-item">
            <h3>Zainteresowania</h3>
            <p>Psychologia, muzyka (zarówno słuchanie jak i granie na instrumentach), filozofia, literatura, akrobatyka, taniec, fitness, biologia i neurologia</p>
        </div>
    </section>

    <section id="offer" class="page">
        <div class="left-decoration"></div>
        <div class="right-decoration"></div>
        <div class="heart-image"></div>
        
        <h2>Oferta</h2>
        
        <div class="service-item">
            <h3>Konsultacje psychologiczne</h3>
            <p>Indywidualne spotkania, podczas których wspólnie rozpoznajemy problem i ustalamy plan działania. Konsultacje są przeznaczone dla dzieci, młodzieży i dorosłych.</p>
        </div>
        
        <div class="service-item">
            <h3>Diagnoza psychologiczna</h3>
            <p>Kompleksowa ocena funkcjonowania emocjonalnego, społecznego i poznawczego. Diagnoza obejmuje wywiad, testy psychologiczne oraz szczegółową analizę wyników.</p>
        </div>
        
        <div class="service-item">
            <h3>Interwencja kryzysowa</h3>
            <p>Wsparcie w nagłych, trudnych sytuacjach życiowych, które wymagają szybkiej pomocy psychologicznej.</p>
        </div>
        
        <div class="service-item">
            <h3>Trening Umiejętności Społecznych (TUS)</h3>
            <p>Zajęcia grupowe dla dzieci i młodzieży, które mają na celu rozwój umiejętności społecznych, komunikacyjnych i emocjonalnych.</p>
        </div>
        
        <h3>Cennik usług</h3>
        <table class="pricing-table">
            <thead>
                <tr>
                    <th>Usługa</th>
                    <th>Czas trwania</th>
                    <th>Cena</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td>Konsultacja psychologiczna - pierwsza wizyta</td>
                    <td>60 minut</td>
                    <td>150 zł</td>
                </tr>
                <tr>
                    <td>Konsultacja psychologiczna - kolejna wizyta</td>
                    <td>50 minut</td>
                    <td>130 zł</td>
                </tr>
                <tr>
                    <td>Diagnoza psychologiczna</td>
                    <td>3-4 spotkania</td>
                    <td>500 zł</td>
                </tr>
                <tr>
                    <td>Interwencja kryzysowa</td>
                    <td>90 minut</td>
                    <td>200 zł</td>
                </tr>
                <tr>
                    <td>Trening Umiejętności Społecznych - spotkanie grupowe</td>
                    <td>90 minut</td>
                    <td>120 zł</td>
                </tr>
                <tr>
                    <td>Konsultacja dla rodziców</td>
                    <td>60 minut</td>
                    <td>150 zł</td>
                </tr>
            </tbody>
        </table>
    </section>

    <section id="contact" class="page">
        <div class="left-decoration"></div>
        <div class="right-decoration"></div>
        <div class="smile-image"></div>
        
        <h2>Umów się na wizytę</h2>
        
        <div class="contact-info">
            <h3>Dane kontaktowe</h3>
            <p><strong>Adres gabinetu:</strong> ul. Przykładowa 12/3, 10-700 Olsztyn</p>
            <p><strong>Telefon:</strong> 511 819 043</p>
            <p><strong>Email:</strong> n.rypinska99@gmail.com</p>
            <p><strong>Godziny przyjęć:</strong> Poniedziałek - Piątek 8:00 - 18:00</p>
        </div>
        
        <h3>Formularz kontaktowy</h3>
        <form>
            <input type="text" placeholder="Imię i nazwisko" required>
            <input type="email" placeholder="Email" required>
            <input type="tel" placeholder="Telefon">
            <textarea placeholder="Treść wiadomości" rows="5" required></textarea>
            <button type="submit">Wyślij</button>
        </form>
    </section>

    <footer>
        <p>© 2024 Natalia Rypińska | Wszelkie prawa zastrzeżone</p>
    </footer>

    <script>
        function toggleMenu() {
            document.querySelector('.side-menu').classList.toggle('active');
        }

        function showPage(pageId) {
            // Ukryj wszystkie strony
            document.querySelectorAll('.page').forEach(page => {
                page.classList.remove('active');
            });
            
            // Pokaż wybraną stronę
            document.getElementById(pageId).classList.add('active');
            
            // Zamknij menu po wyborze
            toggleMenu();
        }

        // Zamknij menu po kliknięciu poza nim
        document.addEventListener('click', function(event) {
            const menu = document.querySelector('.side-menu');
            const btn = document.querySelector('.menu-btn');
            
            if (!menu.contains(event.target) && !btn.contains(event.target)) {
                menu.classList.remove('active');
            }
        });
    </script>
</body>
</html>
