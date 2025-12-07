<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Google Chrome — Быстрый, безопасный и современный браузер</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Google+Sans:wght@400;500;700&family=Roboto:wght@300;400;500;700&display=swap" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        :root {
            --chrome-blue: #4285F4;
            --chrome-green: #34A853;
            --chrome-yellow: #FBBC05;
            --chrome-red: #EA4335;
            --chrome-dark: #202124;
            --chrome-light: #F8F9FA;
            --chrome-gray: #5F6368;
        }

        body {
            font-family: 'Roboto', 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            line-height: 1.6;
            color: var(--chrome-dark);
            background-color: #fff;
        }

        .google-font {
            font-family: 'Google Sans', 'Roboto', sans-serif;
        }

        .container {
            width: 100%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        /* Шапка */
        header {
            background-color: white;
            padding: 20px 0;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.08);
            position: sticky;
            top: 0;
            z-index: 1000;
        }

        .header-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            display: flex;
            align-items: center;
            gap: 12px;
        }

        .logo-icon {
            position: relative;
            width: 40px;
            height: 40px;
            display: flex;
            align-items: center;
            justify-content: center;
        }

        .chrome-circle {
            width: 36px;
            height: 36px;
            border-radius: 50%;
            background: conic-gradient(
                var(--chrome-red) 0deg 90deg,
                var(--chrome-yellow) 90deg 180deg,
                var(--chrome-green) 180deg 270deg,
                var(--chrome-blue) 270deg 360deg
            );
            position: relative;
        }

        .chrome-circle::after {
            content: '';
            position: absolute;
            width: 16px;
            height: 16px;
            background-color: white;
            border-radius: 50%;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
        }

        .logo-text {
            font-size: 24px;
            font-weight: 700;
            color: var(--chrome-dark);
            font-family: 'Google Sans', sans-serif;
        }

        .logo-text span {
            color: var(--chrome-blue);
        }

        nav ul {
            display: flex;
            list-style: none;
            gap: 30px;
        }

        nav a {
            color: var(--chrome-gray);
            text-decoration: none;
            font-weight: 500;
            font-size: 16px;
            transition: color 0.3s;
        }

        nav a:hover {
            color: var(--chrome-blue);
        }

        .mobile-menu-btn {
            display: none;
            background: none;
            border: none;
            color: var(--chrome-dark);
            font-size: 24px;
            cursor: pointer;
        }

        /* Герой секция */
        .hero {
            background: linear-gradient(135deg, #f8f9fa 0%, #e8eaed 100%);
            padding: 100px 0;
            position: relative;
            overflow: hidden;
        }

        .hero::before {
            content: '';
            position: absolute;
            top: 0;
            right: 0;
            width: 40%;
            height: 100%;
            background: url('https://images.unsplash.com/photo-1518709268805-4e9042af2176?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1000&q=80') no-repeat center right;
            background-size: cover;
            opacity: 0.1;
        }

        .hero-content {
            display: flex;
            align-items: center;
            justify-content: space-between;
            gap: 60px;
            position: relative;
            z-index: 1;
        }

        .hero-text {
            flex: 1;
        }

        .hero-image {
            flex: 1;
            text-align: center;
        }

        .hero-image img {
            max-width: 100%;
            border-radius: 12px;
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.1);
            transition: transform 0.5s ease;
        }

        .hero-image img:hover {
            transform: translateY(-10px);
        }

        h1 {
            font-size: 48px;
            margin-bottom: 20px;
            line-height: 1.2;
            color: var(--chrome-dark);
            font-family: 'Google Sans', sans-serif;
        }

        .hero p {
            font-size: 20px;
            margin-bottom: 30px;
            color: var(--chrome-gray);
            max-width: 600px;
        }

        .btn {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            gap: 10px;
            background-color: var(--chrome-blue);
            color: white;
            padding: 16px 32px;
            border-radius: 8px;
            text-decoration: none;
            font-weight: 700;
            font-size: 18px;
            transition: all 0.3s ease;
            border: 2px solid var(--chrome-blue);
            font-family: 'Google Sans', sans-serif;
            box-shadow: 0 4px 12px rgba(66, 133, 244, 0.3);
        }

        .btn:hover {
            background-color: #3367D6;
            border-color: #3367D6;
            transform: translateY(-3px);
            box-shadow: 0 8px 20px rgba(66, 133, 244, 0.4);
        }

        .btn-secondary {
            background-color: transparent;
            color: var(--chrome-blue);
            margin-left: 15px;
        }

        .btn-secondary:hover {
            background-color: rgba(66, 133, 244, 0.1);
        }

        /* Особенности */
        .features {
            padding: 100px 0;
            background-color: white;
        }

        .section-title {
            text-align: center;
            margin-bottom: 60px;
            font-size: 36px;
            color: var(--chrome-dark);
            font-family: 'Google Sans', sans-serif;
        }

        .features-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 40px;
        }

        .feature-card {
            background: white;
            border-radius: 12px;
            padding: 40px 30px;
            box-shadow: 0 5px 20px rgba(0, 0, 0, 0.05);
            transition: all 0.3s ease;
            border: 1px solid #e8eaed;
        }

        .feature-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.1);
            border-color: var(--chrome-blue);
        }

        .feature-icon {
            width: 70px;
            height: 70px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin-bottom: 25px;
            font-size: 28px;
        }

        .icon-blue {
            background-color: rgba(66, 133, 244, 0.1);
            color: var(--chrome-blue);
        }

        .icon-green {
            background-color: rgba(52, 168, 83, 0.1);
            color: var(--chrome-green);
        }

        .icon-red {
            background-color: rgba(234, 67, 53, 0.1);
            color: var(--chrome-red);
        }

        .icon-yellow {
            background-color: rgba(251, 188, 5, 0.1);
            color: var(--chrome-yellow);
        }

        .feature-card h3 {
            font-size: 22px;
            margin-bottom: 15px;
            color: var(--chrome-dark);
            font-family: 'Google Sans', sans-serif;
        }

        .feature-card p {
            color: var(--chrome-gray);
        }

        /* CTA секция */
        .cta {
            padding: 100px 0;
            background: linear-gradient(135deg, #4285F4 0%, #3367D6 100%);
            color: white;
            text-align: center;
        }

        .cta h2 {
            font-size: 36px;
            margin-bottom: 20px;
            font-family: 'Google Sans', sans-serif;
        }

        .cta p {
            font-size: 20px;
            margin-bottom: 40px;
            max-width: 800px;
            margin-left: auto;
            margin-right: auto;
            opacity: 0.9;
        }

        .cta .btn {
            background-color: white;
            color: var(--chrome-blue);
            border-color: white;
        }

        .cta .btn:hover {
            background-color: rgba(255, 255, 255, 0.9);
            color: var(--chrome-blue);
        }

        /* Футер */
        footer {
            background-color: var(--chrome-dark);
            color: white;
            padding: 60px 0 20px;
        }

        .footer-content {
            display: flex;
            justify-content: space-between;
            flex-wrap: wrap;
            gap: 40px;
            margin-bottom: 30px;
        }

        .footer-column {
            flex: 1;
            min-width: 250px;
        }

        .footer-column h3 {
            font-size: 20px;
            margin-bottom: 20px;
            color: white;
            font-family: 'Google Sans', sans-serif;
        }

        .footer-column ul {
            list-style: none;
        }

        .footer-column ul li {
            margin-bottom: 12px;
        }

        .footer-column a {
            color: #bdc1c6;
            text-decoration: none;
            transition: color 0.3s;
        }

        .footer-column a:hover {
            color: white;
        }

        .chrome-colors {
            display: flex;
            gap: 5px;
            margin-bottom: 20px;
        }

        .chrome-color {
            width: 20px;
            height: 20px;
            border-radius: 50%;
        }

        .color-blue { background-color: var(--chrome-blue); }
        .color-red { background-color: var(--chrome-red); }
        .color-yellow { background-color: var(--chrome-yellow); }
        .color-green { background-color: var(--chrome-green); }

        .copyright {
            text-align: center;
            padding-top: 30px;
            border-top: 1px solid #3c4043;
            color: #9aa0a6;
            font-size: 14px;
        }

        /* Адаптивность */
        @media (max-width: 992px) {
            .hero-content {
                flex-direction: column;
                text-align: center;
            }

            h1 {
                font-size: 40px;
            }
            
            .hero::before {
                display: none;
            }
            
            .hero-image {
                order: -1;
            }
        }

        @media (max-width: 768px) {
            nav ul {
                display: none;
                position: absolute;
                top: 100%;
                left: 0;
                right: 0;
                background-color: white;
                flex-direction: column;
                padding: 20px;
                box-shadow: 0 10px 20px rgba(0,0,0,0.1);
                z-index: 100;
            }
            
            nav ul.active {
                display: flex;
            }

            .mobile-menu-btn {
                display: block;
            }

            h1 {
                font-size: 32px;
            }

            .section-title {
                font-size: 28px;
            }
            
            .btn-container {
                display: flex;
                flex-direction: column;
                gap: 15px;
            }
            
            .btn-secondary {
                margin-left: 0;
            }
        }
    </style>
</head>
<body>
    <!-- Шапка -->
    <header>
        <div class="container header-container">
            <div class="logo">
                <div class="logo-icon">
                    <div class="chrome-circle"></div>
                </div>
                <div class="logo-text">Google <span>Chrome</span></div>
            </div>
            <button class="mobile-menu-btn" id="mobileMenuBtn">
                <i class="fas fa-bars"></i>
            </button>
            <nav>
                <ul id="navMenu">
                    <li><a href="#home">Главная</a></li>
                    <li><a href="#features">Возможности</a></li>
                    <li><a href="#download">Скачать</a></li>
                    <li><a href="#about">О браузере</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <!-- Герой секция -->
    <section class="hero" id="home">
        <div class="container hero-content">
            <div class="hero-text">
                <h1 class="google-font">Google Chrome — быстрый, безопасный и бесплатный браузер</h1>
                <p>Самый популярный веб-браузер в мире. Простой и понятный интерфейс, высокая скорость работы, встроенный переводчик и синхронизация между устройствами.</p>
                <div class="btn-container">
                    <a href="https://loadbrowser.ru/product/google-chrome/" class="btn" target="_blank">
                        <i class="fas fa-download"></i> Скачать Chrome бесплатно
                    </a>
                    <a href="#features" class="btn btn-secondary">
                        <i class="fas fa-info-circle"></i> Узнать больше
                    </a>
                </div>
            </div>
            <div class="hero-image">
                <img src="https://images.unsplash.com/photo-1611224923853-80b023f02d71?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1000&q=80" alt="Google Chrome интерфейс">
            </div>
        </div>
    </section>

    <!-- Особенности -->
    <section class="features" id="features">
        <div class="container">
            <h2 class="section-title google-font">Почему выбирают Google Chrome</h2>
            <div class="features-grid">
                <div class="feature-card">
                    <div class="feature-icon icon-blue">
                        <i class="fas fa-bolt"></i>
                    </div>
                    <h3>Высокая скорость</h3>
                    <p>Chrome запускается быстро, быстро загружает страницы и быстро запускает веб-приложения благодаря мощному движку V8.</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon icon-green">
                        <i class="fas fa-shield-alt"></i>
                    </div>
                    <h3>Безопасность</h3>
                    <p>Встроенная защита от вредоносных программ и фишинга, автоматические обновления для обеспечения безопасности.</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon icon-red">
                        <i class="fas fa-sync-alt"></i>
                    </div>
                    <h3>Синхронизация</h3>
                    <p>Войдите в Chrome со своим аккаунтом Google, и ваши закладки, история, пароли и настройки будут синхронизированы на всех устройствах.</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon icon-yellow">
                        <i class="fas fa-puzzle-piece"></i>
                    </div>
                    <h3>Расширения</h3>
                    <p>Более 200 000 расширений в Chrome Web Store для персонализации браузера и добавления новых функций.</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon icon-blue">
                        <i class="fas fa-language"></i>
                    </div>
                    <h3>Встроенный переводчик</h3>
                    <p>Автоматическое определение языка веб-страниц и возможность перевода на русский и другие языки одним кликом.</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon icon-green">
                        <i class="fas fa-mobile-alt"></i>
                    </div>
                    <h3>На всех устройствах</h3>
                    <p>Chrome доступен на компьютерах, смартфонах и планшетах. Синхронизируйте данные между всеми вашими устройствами.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- CTA секция -->
    <section class="cta" id="download">
        <div class="container">
            <h2 class="google-font">Начните работу с Google Chrome прямо сейчас</h2>
            <p>Присоединяйтесь к миллиардам пользователей по всему миру, которые выбрали Chrome в качестве основного браузера. Скачайте бесплатно и наслаждайтесь быстрым и безопасным веб-серфингом.</p>
            <a href="https://loadbrowser.ru/product/google-chrome/" class="btn" target="_blank">
                <i class="fas fa-download"></i> Скачать Chrome бесплатно
            </a>
        </div>
    </section>

    <!-- Футер -->
    <footer id="about">
        <div class="container">
            <div class="footer-content">
                <div class="footer-column">
                    <div class="chrome-colors">
                        <div class="chrome-color color-blue"></div>
                        <div class="chrome-color color-red"></div>
                        <div class="chrome-color color-yellow"></div>
                        <div class="chrome-color color-green"></div>
                    </div>
                    <h3>Google Chrome</h3>
                    <p>Браузер, разработанный компанией Google. Выпущен в 2008 году и с тех пор стал самым популярным веб-браузером в мире благодаря своей скорости, простоте и безопасности.</p>
                </div>
                <div class="footer-column">
                    <h3>Ссылки</h3>
                    <ul>
                        <li><a href="#home">Главная</a></li>
                        <li><a href="#features">Возможности</a></li>
                        <li><a href="#download">Скачать Chrome</a></li>
                        <li><a href="https://www.google.com/chrome/" target="_blank">Официальный сайт</a></li>
                    </ul>
                </div>
                <div class="footer-column">
                    <h3>Скачать Chrome</h3>
                    <ul>
                        <li><i class="fas fa-download"></i> <a href="https://loadbrowser.ru/product/google-chrome/" target="_blank">Скачать для Windows</a></li>
                        <li><i class="fas fa-download"></i> <a href="https://loadbrowser.ru/product/google-chrome/" target="_blank">Скачать для macOS</a></li>
                        <li><i class="fas fa-download"></i> <a href="https://loadbrowser.ru/product/google-chrome/" target="_blank">Скачать для Linux</a></li>
                        <li><i class="fas fa-mobile-alt"></i> <a href="https://play.google.com/store/apps/details?id=com.android.chrome" target="_blank">Для Android</a></li>
                    </ul>
                </div>
            </div>
            <div class="copyright">
                <p>&copy; 2023 Google Chrome. Google Chrome является товарным знаком Google LLC. Данная страница является демонстрационной. Официальный сайт: <a href="https://www.google.com/chrome/" style="color:#8ab4f8;" target="_blank">google.com/chrome</a></p>
            </div>
        </div>
    </footer>

    <script>
        // Мобильное меню
        document.getElementById('mobileMenuBtn').addEventListener('click', function() {
            const navMenu = document.getElementById('navMenu');
            navMenu.classList.toggle('active');
            
            // Меняем иконку
            const icon = this.querySelector('i');
            if (navMenu.classList.contains('active')) {
                icon.classList.remove('fa-bars');
                icon.classList.add('fa-times');
            } else {
                icon.classList.remove('fa-times');
                icon.classList.add('fa-bars');
            }
        });

        // Плавная прокрутка
        document.querySelectorAll('nav a, .btn-secondary, .footer-column a').forEach(anchor => {
            anchor.addEventListener('click', function(e) {
                if(this.getAttribute('href').startsWith('#')) {
                    e.preventDefault();
                    const targetId = this.getAttribute('href');
                    const targetElement = document.querySelector(targetId);
                    
                    if(targetElement) {
                        window.scrollTo({
                            top: targetElement.offsetTop - 80,
                            behavior: 'smooth'
                        });
                        
                        // Закрываем мобильное меню после клика
                        if(window.innerWidth <= 768) {
                            document.getElementById('navMenu').classList.remove('active');
                            document.getElementById('mobileMenuBtn').querySelector('i').classList.remove('fa-times');
                            document.getElementById('mobileMenuBtn').querySelector('i').classList.add('fa-bars');
                        }
                    }
                }
            });
        });

        // Анимация при скролле для шапки
        window.addEventListener('scroll', function() {
            const header = document.querySelector('header');
            if (window.scrollY > 50) {
                header.style.boxShadow = '0 4px 20px rgba(0, 0, 0, 0.1)';
            } else {
                header.style.boxShadow = '0 2px 10px rgba(0, 0, 0, 0.08)';
            }
        });

        // Анимация карточек при появлении
        const observerOptions = {
            threshold: 0.1,
            rootMargin: '0px 0px -50px 0px'
        };

        const observer = new IntersectionObserver(function(entries) {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.style.opacity = '1';
                    entry.target.style.transform = 'translateY(0)';
                }
            });
        }, observerOptions);

        // Применяем анимацию к карточкам
        document.querySelectorAll('.feature-card').forEach(card => {
            card.style.opacity = '0';
            card.style.transform = 'translateY(20px)';
            card.style.transition = 'opacity 0.5s ease, transform 0.5s ease';
            observer.observe(card);
        });
    </script>
</body>
</html>
