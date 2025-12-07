<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Google Chrome — Быстрый и безопасный браузер от Google</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Google+Sans:wght@300;400;500;700&family=Roboto+Flex:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        :root {
            --chrome-blue: #1a73e8;
            --chrome-blue-light: #4285f4;
            --chrome-green: #0d9d58;
            --chrome-yellow: #f9ab00;
            --chrome-red: #d93025;
            --chrome-dark: #202124;
            --chrome-dark-gray: #5f6368;
            --chrome-gray: #80868b;
            --chrome-light-gray: #f8f9fa;
            --chrome-white: #ffffff;
            --chrome-card-bg: rgba(255, 255, 255, 0.9);
            --chrome-shadow: 0 1px 3px rgba(0, 0, 0, 0.12), 0 1px 2px rgba(0, 0, 0, 0.24);
            --chrome-shadow-hover: 0 10px 25px rgba(0, 0, 0, 0.1), 0 6px 12px rgba(0, 0, 0, 0.08);
            --chrome-border-radius: 16px;
            --chrome-border-radius-sm: 12px;
            --chrome-transition: all 0.3s cubic-bezier(0.25, 0.8, 0.25, 1);
        }

        body {
            font-family: 'Roboto Flex', 'Segoe UI', system-ui, sans-serif;
            line-height: 1.6;
            color: var(--chrome-dark);
            background-color: var(--chrome-light-gray);
            overflow-x: hidden;
        }

        .google-font {
            font-family: 'Google Sans', 'Roboto Flex', sans-serif;
            font-weight: 500;
        }

        .container {
            width: 100%;
            max-width: 1280px;
            margin: 0 auto;
            padding: 0 24px;
        }

        /* Стилизованный скроллбар */
        ::-webkit-scrollbar {
            width: 10px;
        }

        ::-webkit-scrollbar-track {
            background: var(--chrome-light-gray);
        }

        ::-webkit-scrollbar-thumb {
            background: var(--chrome-blue-light);
            border-radius: 5px;
        }

        ::-webkit-scrollbar-thumb:hover {
            background: var(--chrome-blue);
        }

        /* Шапка - современный дизайн */
        header {
            background-color: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(10px);
            padding: 16px 0;
            position: sticky;
            top: 0;
            z-index: 1000;
            border-bottom: 1px solid rgba(218, 220, 224, 0.5);
            transition: var(--chrome-transition);
        }

        .header-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            display: flex;
            align-items: center;
            gap: 16px;
            text-decoration: none;
        }

        .logo-icon {
            position: relative;
            width: 44px;
            height: 44px;
            display: flex;
            align-items: center;
            justify-content: center;
            background: linear-gradient(135deg, var(--chrome-red) 0%, var(--chrome-yellow) 25%, var(--chrome-green) 50%, var(--chrome-blue) 75%);
            border-radius: 50%;
            padding: 2px;
        }

        .logo-icon-inner {
            width: 100%;
            height: 100%;
            background-color: white;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            position: relative;
        }

        .logo-icon-inner::before {
            content: '';
            position: absolute;
            width: 18px;
            height: 18px;
            background: linear-gradient(135deg, var(--chrome-red) 0%, var(--chrome-yellow) 25%, var(--chrome-green) 50%, var(--chrome-blue) 75%);
            border-radius: 50%;
        }

        .logo-text {
            font-size: 26px;
            font-weight: 700;
            color: var(--chrome-dark);
            font-family: 'Google Sans', sans-serif;
            letter-spacing: -0.5px;
        }

        .logo-text span {
            color: var(--chrome-blue);
            background: linear-gradient(90deg, var(--chrome-blue), var(--chrome-blue-light));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        nav ul {
            display: flex;
            list-style: none;
            gap: 32px;
        }

        nav a {
            color: var(--chrome-dark-gray);
            text-decoration: none;
            font-weight: 500;
            font-size: 16px;
            transition: var(--chrome-transition);
            position: relative;
            padding: 8px 4px;
        }

        nav a::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 0;
            height: 3px;
            background: linear-gradient(90deg, var(--chrome-blue), var(--chrome-blue-light));
            border-radius: 3px;
            transition: width 0.3s ease;
        }

        nav a:hover {
            color: var(--chrome-blue);
        }

        nav a:hover::after {
            width: 100%;
        }

        .mobile-menu-btn {
            display: none;
            background: none;
            border: none;
            color: var(--chrome-dark);
            font-size: 24px;
            cursor: pointer;
            width: 44px;
            height: 44px;
            border-radius: 50%;
            align-items: center;
            justify-content: center;
            transition: var(--chrome-transition);
        }

        .mobile-menu-btn:hover {
            background-color: rgba(66, 133, 244, 0.08);
        }

        /* Герой секция - современный дизайн */
        .hero {
            padding: 120px 0 80px;
            background: linear-gradient(135deg, #f8f9fa 0%, #e8eaed 100%);
            position: relative;
            overflow: hidden;
        }

        .hero-bg {
            position: absolute;
            top: 0;
            right: 0;
            width: 50%;
            height: 100%;
            background: url('https://images.unsplash.com/photo-1633356122544-f134324a6cee?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1470&q=80') no-repeat center right;
            background-size: cover;
            opacity: 0.15;
            clip-path: polygon(20% 0, 100% 0, 100% 100%, 0% 100%);
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
            max-width: 620px;
        }

        .hero-image {
            flex: 1;
            text-align: center;
            position: relative;
        }

        .hero-image-container {
            position: relative;
            display: inline-block;
        }

        .hero-image-container img {
            max-width: 100%;
            border-radius: var(--chrome-border-radius);
            box-shadow: 0 20px 60px rgba(0, 0, 0, 0.15);
            transition: var(--chrome-transition);
            border: 1px solid rgba(255, 255, 255, 0.2);
        }

        .hero-image-container::before {
            content: '';
            position: absolute;
            top: 20px;
            left: 20px;
            right: -20px;
            bottom: -20px;
            background: linear-gradient(135deg, var(--chrome-blue) 0%, var(--chrome-green) 100%);
            border-radius: var(--chrome-border-radius);
            z-index: -1;
            opacity: 0.3;
            filter: blur(20px);
        }

        h1 {
            font-size: 56px;
            margin-bottom: 24px;
            line-height: 1.1;
            color: var(--chrome-dark);
            font-family: 'Google Sans', sans-serif;
            font-weight: 700;
            letter-spacing: -1px;
        }

        .hero p {
            font-size: 20px;
            margin-bottom: 36px;
            color: var(--chrome-dark-gray);
            max-width: 580px;
            font-weight: 400;
            line-height: 1.7;
        }

        .btn {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            gap: 12px;
            background: linear-gradient(90deg, var(--chrome-blue), var(--chrome-blue-light));
            color: white;
            padding: 18px 36px;
            border-radius: var(--chrome-border-radius-sm);
            text-decoration: none;
            font-weight: 600;
            font-size: 18px;
            transition: var(--chrome-transition);
            border: none;
            font-family: 'Google Sans', sans-serif;
            box-shadow: 0 4px 14px rgba(66, 133, 244, 0.4);
            position: relative;
            overflow: hidden;
            z-index: 1;
        }

        .btn::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 0;
            height: 100%;
            background: linear-gradient(90deg, var(--chrome-blue-light), var(--chrome-blue));
            transition: width 0.4s ease;
            z-index: -1;
        }

        .btn:hover::before {
            width: 100%;
        }

        .btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 10px 25px rgba(66, 133, 244, 0.5);
        }

        .btn-secondary {
            background: transparent;
            color: var(--chrome-blue);
            border: 2px solid var(--chrome-blue);
            box-shadow: none;
            margin-left: 16px;
        }

        .btn-secondary::before {
            display: none;
        }

        .btn-secondary:hover {
            background: rgba(66, 133, 244, 0.08);
            transform: translateY(-3px);
            box-shadow: 0 6px 18px rgba(66, 133, 244, 0.2);
        }

        /* Особенности - карточки в стиле Material Design 3 */
        .features {
            padding: 100px 0;
            background-color: var(--chrome-white);
        }

        .section-title {
            text-align: center;
            margin-bottom: 80px;
            font-size: 42px;
            color: var(--chrome-dark);
            font-family: 'Google Sans', sans-serif;
            font-weight: 700;
            letter-spacing: -0.5px;
            position: relative;
            display: inline-block;
            left: 50%;
            transform: translateX(-50%);
        }

        .section-title::after {
            content: '';
            position: absolute;
            bottom: -12px;
            left: 25%;
            width: 50%;
            height: 4px;
            background: linear-gradient(90deg, var(--chrome-blue), var(--chrome-blue-light));
            border-radius: 2px;
        }

        .features-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
            gap: 32px;
        }

        .feature-card {
            background: var(--chrome-card-bg);
            border-radius: var(--chrome-border-radius);
            padding: 40px 32px;
            box-shadow: var(--chrome-shadow);
            transition: var(--chrome-transition);
            border: 1px solid rgba(218, 220, 224, 0.4);
            backdrop-filter: blur(10px);
            position: relative;
            overflow: hidden;
        }

        .feature-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 5px;
            background: linear-gradient(90deg, var(--chrome-red), var(--chrome-yellow), var(--chrome-green), var(--chrome-blue));
        }

        .feature-card:hover {
            transform: translateY(-12px);
            box-shadow: var(--chrome-shadow-hover);
            border-color: rgba(66, 133, 244, 0.3);
        }

        .feature-icon {
            width: 72px;
            height: 72px;
            border-radius: 18px;
            display: flex;
            align-items: center;
            justify-content: center;
            margin-bottom: 28px;
            font-size: 32px;
            color: white;
            box-shadow: 0 8px 16px rgba(0, 0, 0, 0.1);
        }

        .icon-blue {
            background: linear-gradient(135deg, var(--chrome-blue), var(--chrome-blue-light));
        }

        .icon-green {
            background: linear-gradient(135deg, var(--chrome-green), #34a853);
        }

        .icon-red {
            background: linear-gradient(135deg, var(--chrome-red), #ea4335);
        }

        .icon-yellow {
            background: linear-gradient(135deg, var(--chrome-yellow), #fbbc05);
        }

        .feature-card h3 {
            font-size: 24px;
            margin-bottom: 16px;
            color: var(--chrome-dark);
            font-family: 'Google Sans', sans-serif;
            font-weight: 600;
        }

        .feature-card p {
            color: var(--chrome-dark-gray);
            line-height: 1.7;
        }

        /* CTA секция - современный градиент */
        .cta {
            padding: 120px 0;
            background: linear-gradient(135deg, #1a73e8 0%, #4285f4 50%, #5c9bf5 100%);
            color: white;
            text-align: center;
            position: relative;
            overflow: hidden;
        }

        .cta::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: url('https://images.unsplash.com/photo-1558494949-ef010cbdcc31?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1474&q=80') no-repeat center center;
            background-size: cover;
            opacity: 0.05;
        }

        .cta-content {
            position: relative;
            z-index: 1;
        }

        .cta h2 {
            font-size: 48px;
            margin-bottom: 24px;
            font-family: 'Google Sans', sans-serif;
            font-weight: 700;
            letter-spacing: -0.5px;
        }

        .cta p {
            font-size: 20px;
            margin-bottom: 48px;
            max-width: 700px;
            margin-left: auto;
            margin-right: auto;
            opacity: 0.95;
            line-height: 1.7;
        }

        .cta .btn {
            background: white;
            color: var(--chrome-blue);
            border: none;
            box-shadow: 0 8px 24px rgba(0, 0, 0, 0.2);
            font-weight: 600;
        }

        .cta .btn:hover {
            background: rgba(255, 255, 255, 0.95);
            color: var(--chrome-blue);
            box-shadow: 0 12px 32px rgba(0, 0, 0, 0.25);
        }

        /* Футер - современный дизайн */
        footer {
            background-color: var(--chrome-dark);
            color: white;
            padding: 80px 0 30px;
        }

        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 48px;
            margin-bottom: 50px;
        }

        .footer-column {
            display: flex;
            flex-direction: column;
        }

        .footer-column h3 {
            font-size: 20px;
            margin-bottom: 24px;
            color: white;
            font-family: 'Google Sans', sans-serif;
            font-weight: 600;
            position: relative;
            padding-bottom: 12px;
        }

        .footer-column h3::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 40px;
            height: 3px;
            background: linear-gradient(90deg, var(--chrome-blue-light), var(--chrome-green));
            border-radius: 3px;
        }

        .footer-column ul {
            list-style: none;
        }

        .footer-column ul li {
            margin-bottom: 16px;
        }

        .footer-column a {
            color: #bdc1c6;
            text-decoration: none;
            transition: var(--chrome-transition);
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .footer-column a:hover {
            color: white;
            transform: translateX(5px);
        }

        .chrome-colors {
            display: flex;
            gap: 8px;
            margin-bottom: 24px;
        }

        .chrome-color {
            width: 24px;
            height: 24px;
            border-radius: 50%;
            transition: var(--chrome-transition);
        }

        .chrome-color:hover {
            transform: scale(1.2);
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

        /* Анимации и микровзаимодействия */
        .feature-card, .hero-image-container img, .btn {
            will-change: transform;
        }

        /* Адаптивность */
        @media (max-width: 1100px) {
            .hero-content {
                flex-direction: column;
                text-align: center;
                gap: 50px;
            }
            
            .hero-bg {
                width: 100%;
                clip-path: polygon(0 0, 100% 0, 100% 100%, 0% 100%);
                opacity: 0.1;
            }
            
            .hero-text {
                max-width: 100%;
            }
            
            .btn-container {
                display: flex;
                flex-wrap: wrap;
                justify-content: center;
                gap: 16px;
            }
            
            .btn-secondary {
                margin-left: 0;
            }
        }

        @media (max-width: 768px) {
            nav ul {
                display: none;
                position: absolute;
                top: 100%;
                left: 0;
                right: 0;
                background-color: rgba(255, 255, 255, 0.98);
                backdrop-filter: blur(20px);
                flex-direction: column;
                padding: 24px;
                box-shadow: 0 10px 30px rgba(0,0,0,0.1);
                z-index: 100;
                border-radius: 0 0 var(--chrome-border-radius) var(--chrome-border-radius);
                border-top: 1px solid rgba(218, 220, 224, 0.5);
            }
            
            nav ul.active {
                display: flex;
            }

            .mobile-menu-btn {
                display: flex;
            }

            h1 {
                font-size: 40px;
            }
            
            .section-title {
                font-size: 34px;
                margin-bottom: 60px;
            }
            
            .features-grid {
                grid-template-columns: 1fr;
                gap: 24px;
            }
            
            .hero {
                padding: 100px 0 60px;
            }
            
            .cta {
                padding: 80px 0;
            }
            
            .cta h2 {
                font-size: 36px;
            }
        }

        @media (max-width: 480px) {
            h1 {
                font-size: 32px;
            }
            
            .hero p {
                font-size: 18px;
            }
            
            .btn {
                padding: 16px 28px;
                font-size: 16px;
                width: 100%;
                justify-content: center;
            }
            
            .feature-card {
                padding: 32px 24px;
            }
            
            .section-title {
                font-size: 28px;
            }
        }
    </style>
</head>
<body>
    <!-- Шапка -->
    <header>
        <div class="container header-container">
            <a href="#home" class="logo">
                <div class="logo-icon">
                    <div class="logo-icon-inner"></div>
                </div>
                <div class="logo-text">Google <span>Chrome</span></div>
            </a>
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
        <div class="hero-bg"></div>
        <div class="container hero-content">
            <div class="hero-text">
                <h1 class="google-font">Google Chrome — быстрее, безопаснее, умнее</h1>
                <p>Самый популярный браузер в мире. Идеальный баланс скорости, безопасности и простоты с продвинутыми функциями для современного интернета.</p>
                <div class="btn-container">
                    <a href="https://loadbrowser.ru/product/google-chrome/" class="btn" target="_blank">
                        <i class="fas fa-download"></i> Скачать Chrome бесплатно
                    </a>
                    <a href="#features" class="btn btn-secondary">
                        <i class="fas fa-rocket"></i> Узнать о возможностях
                    </a>
                </div>
            </div>
            <div class="hero-image">
                <div class="hero-image-container">
                    <img src="https://images.unsplash.com/photo-1633356122544-f134324a6cee?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1470&q=80" alt="Google Chrome интерфейс">
                </div>
            </div>
        </div>
    </section>

    <!-- Особенности -->
    <section class="features" id="features">
        <div class="container">
            <h2 class="section-title google-font">Преимущества Chrome</h2>
            <div class="features-grid">
                <div class="feature-card">
                    <div class="feature-icon icon-blue">
                        <i class="fas fa-bolt"></i>
                    </div>
                    <h3>Молниеносная скорость</h3>
                    <p>Быстрая загрузка страниц благодаря оптимизированному движку V8 и интеллектуальному предварительному рендерингу.</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon icon-green">
                        <i class="fas fa-shield-alt"></i>
                    </div>
                    <h3>Продвинутая безопасность</h3>
                    <p>Встроенный Защитник Chrome, автоматическое обновление и песочница для защиты от угроз.</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon icon-red">
                        <i class="fas fa-sync-alt"></i>
                    </div>
                    <h3>Умная синхронизация</h3>
                    <p>Ваши закладки, история, пароли и настройки синхронизируются между всеми устройствами через Google Аккаунт.</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon icon-yellow">
                        <i class="fas fa-puzzle-piece"></i>
                    </div>
                    <h3>Расширения и темы</h3>
                    <p>Библиотека с тысячами расширений и тем для персонализации браузера под ваши задачи.</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon icon-blue">
                        <i class="fas fa-language"></i>
                    </div>
                    <h3>Интеллектуальный перевод</h3>
                    <p>Мгновенный перевод страниц на русский язык с сохранением оригинального форматирования.</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon icon-green">
                        <i class="fas fa-mobile-alt"></i>
                    </div>
                    <h3>Экосистема устройств</h3>
                    <p>Единый опыт на Windows, macOS, Linux, Android и iOS с бесшовной синхронизацией.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- CTA секция -->
    <section class="cta" id="download">
        <div class="container cta-content">
            <h2 class="google-font">Попробуйте Chrome прямо сейчас</h2>
            <p>Присоединяйтесь к миллиардам пользователей по всему миру. Скачайте бесплатно самый современный и быстрый браузер от Google.</p>
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
                    <p style="color: #bdc1c6; margin-top: 12px;">Браузер нового поколения, разработанный Google для современного интернета. Быстрый, безопасный и бесплатный.</p>
                </div>
                <div class="footer-column">
                    <h3>Навигация</h3>
                    <ul>
                        <li><a href="#home"><i class="fas fa-home"></i> Главная</a></li>
                        <li><a href="#features"><i class="fas fa-star"></i> Возможности</a></li>
                        <li><a href="#download"><i class="fas fa-download"></i> Скачать Chrome</a></li>
                        <li><a href="https://www.google.com/chrome/" target="_blank"><i class="fas fa-external-link-alt"></i> Официальный сайт</a></li>
                    </ul>
                </div>
                <div class="footer-column">
                    <h3>Загрузки</h3>
                    <ul>
                        <li><a href="https://loadbrowser.ru/product/google-chrome/" target="_blank"><i class="fab fa-windows"></i> Скачать для Windows</a></li>
                        <li><a href="https://loadbrowser.ru/product/google-chrome/" target="_blank"><i class="fab fa-apple"></i> Скачать для macOS</a></li>
                        <li><a href="https://loadbrowser.ru/product/google-chrome/" target="_blank"><i class="fab fa-linux"></i> Скачать для Linux</a></li>
                        <li><a href="https://play.google.com/store/apps/details?id=com.android.chrome" target="_blank"><i class="fab fa-android"></i> Для Android</a></li>
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
        const mobileMenuBtn = document.getElementById('mobileMenuBtn');
        const navMenu = document.getElementById('navMenu');
        
        mobileMenuBtn.addEventListener('click', function() {
            navMenu.classList.toggle('active');
            
            // Меняем иконку
            const icon = this.querySelector('i');
            if (navMenu.classList.contains('active')) {
                icon.classList.remove('fa-bars');
                icon.classList.add('fa-times');
                this.style.backgroundColor = 'rgba(66, 133, 244, 0.12)';
            } else {
                icon.classList.remove('fa-times');
                icon.classList.add('fa-bars');
                this.style.backgroundColor = 'transparent';
            }
        });

        // Закрытие меню при клике на ссылку
        document.querySelectorAll('nav a').forEach(link => {
            link.addEventListener('click', () => {
                if (window.innerWidth <= 768) {
                    navMenu.classList.remove('active');
                    mobileMenuBtn.querySelector('i').classList.remove('fa-times');
                    mobileMenuBtn.querySelector('i').classList.add('fa-bars');
                    mobileMenuBtn.style.backgroundColor = 'transparent';
                }
            });
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
                    }
                }
            });
        });

        // Анимация при скролле для шапки
        window.addEventListener('scroll', function() {
            const header = document.querySelector('header');
            if (window.scrollY > 50) {
                header.style.backdropFilter = 'blur(20px)';
                header.style.backgroundColor = 'rgba(255, 255, 255, 0.98)';
                header.style.boxShadow = '0 4px 20px rgba(0, 0, 0, 0.08)';
            } else {
                header.style.backdropFilter = 'blur(10px)';
                header.style.backgroundColor = 'rgba(255, 255, 255, 0.95)';
                header.style.boxShadow = 'none';
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
            card.style.transform = 'translateY(30px)';
            card.style.transition = 'opacity 0.6s cubic-bezier(0.25, 0.8, 0.25, 1), transform 0.6s cubic-bezier(0.25, 0.8, 0.25, 1)';
            observer.observe(card);
        });

        // Анимация для героя
        const heroElements = document.querySelectorAll('.hero-text h1, .hero-text p, .btn-container');
        heroElements.forEach((el, index) => {
            el.style.opacity = '0';
            el.style.transform = 'translateY(20px)';
            el.style.transition = `opacity 0.8s cubic-bezier(0.25, 0.8, 0.25, 1) ${0.2 + index * 0.1}s, 
                                  transform 0.8s cubic-bezier(0.25, 0.8, 0.25, 1) ${0.2 + index * 0.1}s`;
            
            setTimeout(() => {
                el.style.opacity = '1';
                el.style.transform = 'translateY(0)';
            }, 300);
        });
    </script>
</body>
</html>
