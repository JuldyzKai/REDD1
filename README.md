<html lang="kk">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Портфолио</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@300;400;500;700&family=Noto+Sans+SC:wght@400;500;700&display=swap" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Roboto', 'Noto Sans SC', sans-serif;
        }
        
        :root {
            --primary: #0066cc;
            --secondary: #004d99;
            --accent: #f39c12;
            --light: #f5f7fa;
            --dark: #2c3e50;
            --text: #34495e;
            --kazakh-blue: #00a0e3;
            --kazakh-gold: #ffd700;
        }
        
        body {
            background-color: var(--light);
            color: var(--text);
            line-height: 1.6;
            overflow-x: hidden;
        }
        
        .container {
            width: 100%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        /* Навигация */
        header {
            background: linear-gradient(135deg, var(--kazakh-blue) 0%, var(--primary) 100%);
            position: fixed;
            top: 0;
            left: 0;
            right: 0;
            z-index: 1000;
            box-shadow: 0 2px 15px rgba(0, 0, 0, 0.2);
        }
        
        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 15px 0;
        }
        
        .logo {
            font-size: 1.8rem;
            font-weight: 700;
            color: white;
            text-decoration: none;
            display: flex;
            align-items: center;
        }
        
        .logo i {
            margin-right: 10px;
            color: var(--kazakh-gold);
        }
        
        .nav-links {
            display: flex;
            list-style: none;
        }
        
        .nav-links li {
            margin-left: 25px;
        }
        
        .nav-links a {
            text-decoration: none;
            color: rgba(255, 255, 255, 0.9);
            font-weight: 500;
            transition: color 0.3s;
            font-size: 1.1rem;
        }
        
        .nav-links a:hover {
            color: var(--kazakh-gold);
        }
        
        .nav-links a.active {
            color: white;
            font-weight: 600;
        }
        
        .hamburger {
            display: none;
            cursor: pointer;
            color: white;
            font-size: 1.5rem;
        }
        
        /* Герой секция */
        .hero {
            height: 100vh;
            display: flex;
            align-items: center;
            background: linear-gradient(rgba(255, 255, 255, 0.9), rgba(245, 247, 250, 0.9)), 
                        url('https://images.unsplash.com/photo-1509062522246-3755977927d7?ixlib=rb-4.0.3&auto=format&fit=crop&w=1200&q=80') center/cover no-repeat;
            position: relative;
            overflow: hidden;
            padding-top: 70px;
        }
        
        .hero-content {
            max-width: 800px;
            z-index: 2;
            background: rgba(255, 255, 255, 0.85);
            padding: 40px;
            border-radius: 20px;
            box-shadow: 0 15px 40px rgba(0, 0, 0, 0.15);
        }
        
        .hero h1 {
            font-size: 3.2rem;
            margin-bottom: 20px;
            line-height: 1.2;
            color: var(--dark);
        }
        
        .hero h1 span {
            color: var(--primary);
            display: block;
            font-size: 2.8rem;
            margin-top: 10px;
        }
        
        .hero p {
            font-size: 1.3rem;
            margin-bottom: 30px;
            color: var(--text);
            line-height: 1.8;
        }
        
        .hero-btns {
            display: flex;
            gap: 20px;
            margin-top: 40px;
        }
        
        .btn {
            display: inline-flex;
            align-items: center;
            padding: 14px 35px;
            border-radius: 50px;
            text-decoration: none;
            font-weight: 600;
            transition: all 0.3s ease;
            font-size: 1.1rem;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        }
        
        .btn i {
            margin-right: 10px;
        }
        
        .btn-primary {
            background: linear-gradient(to right, var(--primary), var(--kazakh-blue));
            color: white;
        }
        
        .btn-primary:hover {
            transform: translateY(-5px);
            box-shadow: 0 8px 20px rgba(0, 102, 204, 0.3);
        }
        
        .btn-outline {
            border: 2px solid var(--primary);
            color: var(--primary);
        }
        
        .btn-outline:hover {
            background-color: var(--primary);
            color: white;
            transform: translateY(-5px);
        }
        
        .hero-img {
            position: absolute;
            right: 5%;
            top: 50%;
            transform: translateY(-50%);
            width: 35%;
            max-width: 500px;
            z-index: 1;
            border-radius: 20px;
            overflow: hidden;
            box-shadow: 0 20px 50px rgba(0, 0, 0, 0.2);
        }
        
        .hero-img img {
            width: 100%;
            display: block;
        }
        
        /* Секции */
        section {
            padding: 100px 0;
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 70px;
        }
        
        .section-title h2 {
            font-size: 2.8rem;
            color: var(--dark);
            margin-bottom: 20px;
            position: relative;
            display: inline-block;
        }
        
        .section-title h2::after {
            content: '';
            position: absolute;
            bottom: -15px;
            left: 50%;
            transform: translateX(-50%);
            width: 100px;
            height: 5px;
            background: linear-gradient(to right, var(--primary), var(--kazakh-blue));
            border-radius: 10px;
        }
        
        .section-title p {
            color: var(--text);
            max-width: 800px;
            margin: 30px auto 0;
            font-size: 1.2rem;
            line-height: 1.8;
        }
        
        /* Обо мне */
        .about {
            background-color: rgb(249, 232, 251);
        }
        
        .about-content {
            display: flex;
            align-items: center;
            gap: 60px;
        }
        
        .about-img {
            flex: 1;
            border-radius: 20px;
            overflow: hidden;
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.15);
        }
        
        .about-img img {
            width: 100%;
            display: block;
            transition: transform 0.5s ease;
        }
        
        .about-img:hover img {
            transform: scale(1.05);
        }
        
        .about-text {
            flex: 1;
        }
        
        .about-text h3 {
            font-size: 2.2rem;
            margin-bottom: 25px;
            color: var(--primary);
            line-height: 1.3;
        }
        
        .about-text p {
            margin-bottom: 25px;
            color: var(--text);
            font-size: 1.1rem;
            line-height: 1.8;
        }
        
        .info-list {
            list-style: none;
            margin: 35px 0;
        }
        
        .info-list li {
            margin-bottom: 15px;
            display: flex;
            align-items: flex-start;
            font-size: 1.1rem;
        }
        
        .info-list li i {
            color: var(--primary);
            margin-right: 15px;
            font-size: 1.2rem;
            min-width: 25px;
            margin-top: 4px;
        }
        
        .info-list li strong {
            color: var(--dark);
            margin-right: 8px;
        }
        
        /* Әдіс-тәсілдер бөліміне арналған стильдер */
        .skills-container {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(350px, 1fr));
            gap: 35px;
        }
        
        .skill-card {
            background: rgb(212, 249, 255);
            border-radius: 20px;
            padding: 35px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.08);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            border-left: 5px solid var(--primary);
            display: flex;
            flex-direction: column;
        }
        
        .skill-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 40px rgba(0, 0, 0, 0.15);
        }
        
        .skill-icon {
            font-size: 3rem;
            color: var(--primary);
            margin-bottom: 25px;
        }
        
        .skill-card h3 {
            font-size: 1.6rem;
            margin-bottom: 20px;
            color: var(--dark);
        }
        
        .skill-card p {
            color: var(--text);
            margin-bottom: 25px;
            line-height: 1.8;
            flex-grow: 1;
        }
        
        .skill-card .btn {
            align-self: flex-start;
            margin-top: auto;
            padding: 10px 25px;
            font-size: 0.9rem;
        }
        
        .tools-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 10px;
            margin: 15px 0;
        }
        
        .tool-item {
            background: rgba(157, 189, 245, 0.1);
            border-radius: 8px;
            padding: 8px;
            text-align: center;
            font-size: 0.85rem;
            font-weight: 600;
            color: var(--primary);
        }

        /* Достижения */
        .achievements {
            background-color: rgb(249, 249, 249);
        }
        
        .achievements-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(350px, 1fr));
            gap: 35px;
        }
        
        .achievement-card {
            background: linear-gradient(to bottom right, rgb(246, 246, 191), #f8f9fa);
            border-radius: 20px;
            padding: 35px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.08);
            transition: transform 0.3s ease;
            border-left: 5px solid var(--accent);
            display: flex;
            flex-direction: column;
        }
        
        .achievement-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 40px rgba(0, 0, 0, 0.15);
        }
        
        .achievement-icon {
            font-size: 3rem;
            color: var(--accent);
            margin-bottom: 25px;
        }
        
        .achievement-card h3 {
            font-size: 1.6rem;
            margin-bottom: 20px;
            color: var(--dark);
        }
        
        .achievement-card p {
            color: var(--text);
            margin-bottom: 25px;
            line-height: 1.8;
            flex-grow: 1;
        }
        
        .achievement-card .btn {
            align-self: flex-start;
            margin-top: auto;
        }
        
        /* Контакты */
        .contact {
            background: linear-gradient(135deg, var(--primary) 0%, var(--secondary) 100%);
            color: white;
        }
        
        .contact .section-title h2,
        .contact .section-title p {
            color: white;
        }
        
        .contact-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 60px;
        }
        
        .contact-info h3 {
            font-size: 2rem;
            margin-bottom: 35px;
            position: relative;
            padding-bottom: 15px;
        }
        
        .contact-info h3::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 100px;
            height: 4px;
            background-color: var(--kazakh-gold);
        }
        
        .contact-item {
            display: flex;
            align-items: flex-start;
            margin-bottom: 30px;
        }
        
        .contact-item i {
            font-size: 1.8rem;
            color: var(--kazakh-gold);
            margin-right: 20px;
            min-width: 40px;
            margin-top: 5px;
        }
        
        .contact-item-content h4 {
            font-size: 1.4rem;
            margin-bottom: 8px;
            font-weight: 500;
        }
        
        .contact-form {
            background: rgba(255, 255, 255, 0.1);
            padding: 40px;
            border-radius: 20px;
            backdrop-filter: blur(10px);
        }
        
        .form-group {
            margin-bottom: 25px;
        }
        
        .form-group label {
            display: block;
            margin-bottom: 12px;
            font-weight: 500;
            font-size: 1.1rem;
        }
        
        .form-control {
            width: 100%;
            padding: 15px 20px;
            border: none;
            border-radius: 10px;
            background: rgba(255, 255, 255, 0.15);
            color: white;
            font-size: 1.1rem;
        }
        
        .form-control::placeholder {
            color: rgba(255, 255, 255, 0.7);
        }
        
        .form-control:focus {
            outline: none;
            background: rgba(255, 255, 255, 0.2);
        }
        
        textarea.form-control {
            min-height: 180px;
            resize: vertical;
        }
        /* QR-код стильдері */
.qr-code-container {
    text-align: center;
    margin: 25px 0;
    padding: 15px;
    background: rgba(255, 255, 255, 0.1);
    border-radius: 10px;
}

.qr-code {
    width: 150px;
    height: 150px;
    border: 3px solid white;
    border-radius: 8px;
    padding: 5px;
    background: white;
}
        /* Футер */
        footer {
            background-color: var(--dark);
            color: white;
            padding: 40px 0 20px;
            text-align: center;
        }
        
        .footer-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 30px;
        }
        
        .footer-logo {
            font-size: 1.8rem;
            font-weight: 700;
            color: white;
        }
        
        .footer-logo span {
            color: var(--kazakh-gold);
        }
        
        .social-links {
            display: flex;
            gap: 20px;
        }
        
        .social-links a {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            width: 50px;
            height: 50px;
            border-radius: 50%;
            background-color: rgba(255, 255, 255, 0.1);
            color: white;
            font-size: 1.5rem;
            transition: all 0.3s ease;
        }
        
        .social-links a:hover {
            background-color: var(--primary);
            transform: translateY(-5px);
        }
        
        .copyright {
            padding-top: 25px;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            font-size: 1.1rem;
        }
        
        /* Адаптивность */
        @media (max-width: 1100px) {
            .hero-img {
                width: 40%;
            }
            
            .hero-content {
                max-width: 55%;
            }
        }
        
        @media (max-width: 992px) {
            .hero h1 {
                font-size: 2.8rem;
            }
            
            .hero-content {
                max-width: 100%;
                margin-right: 40%;
            }
            
            .hero-img {
                width: 35%;
            }
            
            .about-content {
                flex-direction: column;
            }
            
            .section-title h2 {
                font-size: 2.5rem;
            }
            
            .skills-container {
                grid-template-columns: repeat(2, 1fr);
            }
        }
        
        @media (max-width: 768px) {
            .hamburger {
                display: block;
            }
            
            .nav-links {
                position: absolute;
                top: 100%;
                left: 0;
                right: 0;
                background: var(--primary);
                flex-direction: column;
                align-items: center;
                padding: 20px 0;
                clip-path: polygon(0 0, 100% 0, 100% 0, 0 0);
                transition: clip-path 0.4s ease;
            }
            
            .nav-links.active {
                clip-path: polygon(0 0, 100% 0, 100% 100%, 0 100%);
            }
            
            .nav-links li {
                margin: 15px 0;
            }
            
            .hero {
                flex-direction: column;
                text-align: center;
                padding-top: 70px;
            }
            
            .hero-content {
                max-width: 90%;
                margin: 0 auto;
                padding: 30px;
            }
            
            .hero-btns {
                justify-content: center;
            }
            
            .hero-img {
                position: relative;
                top: auto;
                left: auto;
                transform: none;
                width: 80%;
                margin: 40px auto 0;
                order: -1;
            }
            
            .footer-content {
                flex-direction: column;
                gap: 30px;
            }
            
            .skills-container {
                grid-template-columns: 1fr;
            }
        }
        
        @media (max-width: 576px) {
            .hero h1 {
                font-size: 2.3rem;
            }
            
            .hero h1 span {
                font-size: 2rem;
            }
            
            .section-title h2 {
                font-size: 2rem;
            }
            
            .skills-container, .achievements-grid {
                grid-template-columns: 1fr;
            }
            
            .hero-btns {
                flex-direction: column;
                align-items: center;
            }
            
            .tools-grid {
                grid-template-columns: repeat(2, 1fr);
            }
        }
    </style>
</head>
<body>
    <!-- Навигация -->
    <header>
        <div class="container">
            <nav>
                <a href="#" class="logo"><i class="fas fa-book-open"></i>Мұғалім Портфолиосы</a>
                <ul class="nav-links">
                    <li><a href="#home" class="active">Басты</a></li>
                    <li><a href="#about">Мен туралы</a></li>
                    <li><a href="#skills">Әдіс-тәсілдер</a></li>
                    <li><a href="#achievements">Жетістіктер</a></li>
                    <li><a href="#contact">Байланыс</a></li>
                </ul>
                <div class="hamburger">
                    <i class="fas fa-bars"></i>
                </div>
            </nav>
        </div>
    </header>

    <!-- Герой секция -->
    <section id="home" class="hero">
        <div class="container">
            <div class="hero-content">
                <h1>Сәлем, мен Қайназарова Жұлдыз Есімханқызы<span>Қазақ тілі мен әдебиеті</span> пәнінің мұғалімімін</h1>
                <p>14 жылдық педагогикалық тәжірибесі бар педагогика ғылымдарының магистрі, педагог-сарапшы. Ұлттық құндылықтарды дәріптей отырып, оқушылардың шығармашылық қабілетін дамытуға, әдебиетке деген қызығушылығын арттыруға ерекше мән беремін.</p>
                <div class="hero-btns">
                    <a href="#achievements" class="btn btn-primary"><i class="fas fa-trophy"></i>Жетістіктерім</a>
                    <a href="#contact" class="btn btn-outline"><i class="fas fa-envelope"></i>Байланысу</a>
                </div>
            </div>
            <div class="hero-img">
                <img src="МЕЕ.jpg" alt="Мұғалім портфолиосы">
            </div>
        </div>
    </section>

    <!-- Мен туралы -->
    <section id="about" class="about">
        <div class="container">
            <div class="section-title">
                <h2>Мен туралы</h2>
                <p>Мен жайлы көбірек біліңіз, менің педагогикалық ұстанымдарым және қызметтік жолым</p>
            </div>
            <div class="about-content">
                <div class="about-img">
                    <img src="МАГ.png" alt="Мұғалім портфолиосы">
                </div>
                <div class="about-text">
                    <h3>Педагогика ғылымдарының магистрі, педагог-сарапшы</h3>
                    <p>Менің педагогикалық ұстанымым: <strong>"Әр оқушының бойындағы қабілетті ашу - ұстаздың басты міндеті. Оқушыны заманауи технологиялар арқылы да шабыттандыруға болады."</strong></p>
                    <p>Сабақтарымда заманауи әдіс-тәсілдерді, сонымен қатар <strong>жасанды интеллект (ЖИ)</strong> мүмкіндіктерін және соңғы шыққан түрлі <strong>цифрлық қосымшаларды</strong> кеңінен қолданамын. Бұл оқушылардың белсенділігін арттырып, олардың цифрлық сауаттылығын жетілдіруге ықпал етеді.</p>
                    <ul class="info-list">
                        <li><i class="fas fa-user"></i><strong>Аты-жөні:</strong> Қазақ тілі мен әдебиеті мұғалімі</li>
                        <li><i class="fas fa-graduation-cap"></i><strong>Ғылыми дәрежесі:</strong> Педагогика ғылымдарының магистрі</li>
                        <li><i class="fas fa-chalkboard-teacher"></i><strong>Педагогикалық өтілі:</strong> 14 жыл</li>
                        <li><i class="fas fa-chalkboard-teacher"></i><strong>Еңбек өтілі:</strong> 8 жыл</li>
                        <li><i class="fas fa-certificate"></i><strong>Біліктілік санаты:</strong> Педагог-сарапшы</li>
                        <li><i class="fas fa-map-marker-alt"></i><strong>Орналасқан жері:</strong> Қазақстан, Алматы</li>
                    </ul>
                    <a href="Түйіндеме.docx" class=""><i class="fas fa-download"></i>Резюмені жүктеу</a>
                </div>
            </div>
        </div>
    </section>

    <!-- Әдіс-тәсілдер -->
     <section id="skills" class="skills">
    <div class="container">
        <div class="section-title">
            <h2>Әдіс-тәсілдер</h2>
            <p>Сабақтарда қолданатын заманауи технологиялар мен цифрлық құралдар</p>
        </div>
        <div class="skills-container">
            <!-- 1-карточка -->
            <div class="skill-card">
                <div class="skill-icon"><i class="fas fa-chalkboard-teacher"></i></div>
                <h3>Белсенді оқыту технологиялары</h3>
                <p>Қазақ тілі мен әдебиеті пәнінде баланың деңгейіне қарай икемдеп әдіс-тәсілдерді саралаймын.</p>
                <div class="tools-grid">
                    <a href="https://topiq.kz" target="_blank" class="tool-item">Дамыта оқыту</a>
                    <a href="https://learningapps.org" target="_blank" class="tool-item">СТО технологиясы</a>
                    <a href="https://bilimland.kz" target="_blank" class="tool-item">Модульдік оқыту</a>
                    <a href="https://topiq.kz" target="_blank" class="tool-item">СКО технологиясы</a>
                    <a href="https://learningapps.org" target="_blank" class="tool-item">Бағалау жүйесі</a>
                    <a href="https://bilimland.kz" target="_blank" class="tool-item">Саралап оқыту</a>
                </div>
                <a href="#" class="btn btn-outline"><i class="fas fa-eye"></i>Қарау</a>
            </div>
            
            <!-- 2-карточка -->
            <div class="skill-card">
                <div class="skill-icon"><i class="fas fa-robot"></i></div>
                <h3>Жасанды Интеллект Қолдану</h3>
                <p>Сабақтарда ЖИ құралдарын кеңінен қолданамын: мәтін генерациялау, тест құрастыру, визуализация.</p>
                <div class="tools-grid">
                    <a href="https://chat.openai.com" target="_blank" class="tool-item">Мәтін генерациясы</a>
                    <a href="https://quizlet.com" target="_blank" class="tool-item">Автоматты тестілеу</a>
                    <a href="https://topiq.kz" target="_blank" class="tool-item">Жеке оқу жоспары</a>
                    <a href="https://canva.com" target="_blank" class="tool-item">Визуализация</a>
                    <a href="https://kahoot.com" target="_blank" class="tool-item">Бағалау жүйесі</a>
                    <a href="https://duolingo.com" target="_blank" class="tool-item">Тіл үйрету</a>
                </div>
                <a href="#" class="btn btn-outline"><i class="fas fa-eye"></i>Қарау</a>
            </div>
            
            <!-- 3-карточка -->
            <div class="skill-card">
                <div class="skill-icon"><i class="fas fa-laptop-code"></i></div>
                <h3>Цифрлық Қосымшалар</h3>
                <p>Сабақтарды тиімді және қызықты ету үшін келесі платформаларды қолданамын:</p>
                <div class="tools-grid">
                    <a href="https://padlet.com" target="_blank" class="tool-item">Padlet</a>
                    <a href="https://topiq.kz" target="_blank" class="tool-item">TopIQ</a>
                    <a href="https://learningapps.org" target="_blank" class="tool-item">LearningApps</a>
                    <a href="https://bilimland.kz" target="_blank" class="tool-item">Bilimland</a>
                    <a href="https://miro.com" target="_blank" class="tool-item">Miro</a>
                    <a href="https://canva.com" target="_blank" class="tool-item">canvas></a>
                    <a href="https://kundelik.kz" target="_blank" class="tool-item">Күнделік.кз</a>
                    <a href="https://wordwall.net" target="_blank" class="tool-item">wordwall</a>
                    <a href="https://www.mentimeter.com" target="_blank" class="tool-item">mentimeter</a>
                </div>
                <a href="#" class="btn btn-outline"><i class="fas fa-eye"></i>Қарау</a>
            </div>
        </div>
    </div>
</section>

    <!-- Жетістіктер -->
    <section id="achievements" class="achievements">
        <div class="container">
            <div class="section-title">
                <h2>Кәсіби Жетістіктер</h2>
                <p>Педагогикалық қызметімдегі маңызды жетістіктер</p>
            </div>
            <div class="achievements-grid">
                <div class="achievement-card">
                    <div class="achievement-icon"><i class="fas fa-lightbulb"></i></div>
                    <h3>Әдістемелік Әзірлемелер</h3>
                    <p>Жаңартылған оқу бағдарламасы негізінде заманауи цифрлық технологияларды қолдана отырып, тиімді сабақ үлгілерін әзірледім. ЖИ құралдарын сабаққа кіріктіру арқылы оқыту тәжірибемді жетілдірдім.</p>
                    <a href="https://heyzine.com/flip-book/d439bea668.html" class="btn btn-outline"><i class="fas fa-eye"></i>Қарау</a>
                </div>
                <div class="achievement-card">
                    <div class="achievement-icon"><i class="fas fa-medal"></i></div>
                    <h3>Оқушылардың Жетістіктері</h3>
                    <p>Оқушыларым аудандық, облыстық, республикалық сайыстар мен байқаулар,ғылыми жобаларда орындарға ие болып жүр. Соңғы 3 жылда біраз оқушым аудандық, қалалық, республика көлемінде жүлдегер атанды.</p>
                    <a href="Оқушы.html" class="btn btn-outline"><i class="fas fa-eye"></i>Қарау</a>
                </div>
                <div class="achievement-card">
                    <div class="achievement-icon"><i class="fas fa-chalkboard-teacher"></i></div>
                    <h3>Мұғалім Жетістіктері</h3>
                    <p>Әдістемелік жұмыстарымды әріптестеріммен бөлісіп, қалалық семинарда тәжірибе тарттым. Республикалық деңгейде цифрлық құралдармен жұмыс істеуде атаулы жүлде алдым. Педагогикалық байқаулардың жүлдегерімін.</p>
                    <a href="Өзж.html" class="btn btn-outline"><i class="fas fa-eye"></i>Қарау</a>
                </div>
                <div class="achievement-card">
                    <div class="achievement-icon"><i class="fas fa-users"></i></div>
                    <h3>Конференциялар мен Семинарлар</h3>
                    <p>Республикалық және халықаралық конференцияларға, семинарларға қатысып, өз тәжірибемді бөлістім. Педагогикалық инновацияларға арналған форумдардың үздік докладшысы атандым.</p>
                    <a href="#" class="btn btn-outline"><i class="fas fa-eye"></i>Қарау</a>
                </div>
                <div class="achievement-card">
                    <div class="achievement-icon"><i class="fas fa-graduation-cap"></i></div>
                    <h3>Курстар және Жетілдіру</h3>
                    <p>Соңғы 5 жылда 20-дан астам қосымша біліктілікті арттыру курстарын аяқтадым. Халықаралық деңгейдегі педагогикалық бағдарламаларға қатыстым және сертификаттар алдым.</p>
                    <a href="#" class="btn btn-outline"><i class="fas fa-eye"></i>Қарау</a>
                </div>
            </div>
        </div>
    </section>

    <!-- Контакты -->
    <section id="contact" class="contact">
        <div class="container">
            <div class="section-title">
                <h2>Байланысу</h2>
                <p>Кез келген сұрақтар үшін маған хабарласыңыз</p>
            </div>
            <div class="contact-container">
                <div class="contact-info">
                    <h3>Менімен байланысу</h3>
                    <div class="contact-item">
                        <i class="fas fa-envelope"></i>
                        <div class="contact-item-content">
                            <h4>Электронды пошта</h4>
                            <p>Juldiz8469@gmail.com<br>zhuldyz.kay.84@mail.ru</p>
                        </div>
                    </div>
                    <div class="contact-item">
                        <i class="fas fa-phone-alt"></i>
                        <div class="contact-item-content">
                            <h4>Телефон</h4>
                            <p>+7 (747) 153 76 56</p>
                        </div>
                    </div>
                    <div class="contact-item">
                        <i class="fas fa-map-marker-alt"></i>
                        <div class="contact-item-content">
                            <h4>Мекен-жай</h4>
                            <p>Қазақстан, Алматы қаласы</p>
                        </div>
                    </div>
                    <div class="contact-item">
                        <i class="fas fa-share-alt"></i>
                        <div class="contact-item-content">
                            <h4>Әлеуметтік желілер</h4>
                            <p>Instagram, Facebook, Telegram</p>
                        </div>
                    </div>
                </div>
                <div class="contact-form">
                    <form>
                        <div class="form-group">
                            <label for="name">Аты-жөніңіз</label>
                            <input type="text" id="name" class="form-control" placeholder="Аты-жөніңізді енгізіңіз" required>
                        </div>
                        <div class="form-group">
                            <label for="email">Электронды пошта</label>
                            <input type="email" id="email" class="form-control" placeholder="Электронды поштаңызды енгізіңіз" required>
                        </div>
                        <div class="form-group">
                            <label for="subject">Тақырып</label>
                            <input type="text" id="subject" class="form-control" placeholder="Хабарлама тақырыбы" required>
                        </div>
                        <div class="form-group">
                            <label for="message">Хабарлама</label>
                            <textarea id="message" class="form-control" placeholder="Хабарламаңызды осы жерге жазыңыз..." required></textarea>
                        </div>
                        <button type="submit" class="btn btn-primary"><i class="fas fa-paper-plane"></i>Хабарлама жіберу</button>
                    </form>
                </div>
            </div>
        </div>
    </section>

    <!-- Футер -->
    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-logo">Мұғалім <span>Портфолиосы</span></div>
                <div class="social-links">
                    <a href="#"><i class="fab fa-facebook-f"></i></a>
                    <a href="#"><i class="fab fa-instagram"></i></a>
                    <a href="#"><i class="fab fa-telegram"></i></a>
                    <a href="#"><i class="fab fa-whatsapp"></i></a>
                </div>
            </div>
             <!-- QR-код бөлімін  -->
    <div class="qr-code-container">
        <h3>Портфолиомды сканерлеу</h3>
        <img src="кюар.png" 
             alt="QR Code" 
             class="qr-code">
        <p>Камераны QR-кодқа бағыттаңыз</p>
    </div>
    

            <div class="copyright">
                © 2025 Қазақ тілі мен әдебиеті мұғалімінің портфолиосы. Барлық құқықтар қорғалған.
            </div>
        </div>
    </footer>

    <script>
        // Мобильді навигация
        const hamburger = document.querySelector('.hamburger');
        const navLinks = document.querySelector('.nav-links');
        
        hamburger.addEventListener('click', () => {
            navLinks.classList.toggle('active');
        });
        
        // Активация навигации при прокрутке
        window.addEventListener('scroll', () => {
            const sections = document.querySelectorAll('section');
            const navLinks = document.querySelectorAll('.nav-links a');
            
            let current = '';
            
            sections.forEach(section => {
                const sectionTop = section.offsetTop;
                const sectionHeight = section.clientHeight;
                
                if (pageYOffset >= (sectionTop - 100)) {
                    current = section.getAttribute('id');
                }
            });
            
            navLinks.forEach(link => {
                link.classList.remove('active');
                if (link.getAttribute('href').substring(1) === current) {
                    link.classList.add('active');
                }
            });
        });
        
        // Плавный скролл
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function(e) {
                e.preventDefault();
                
                const targetId = this.getAttribute('href');
                const targetElement = document.querySelector(targetId);
                
                window.scrollTo({
                    top: targetElement.offsetTop - 80,
                    behavior: 'smooth'
                });
                
                // Закрываем мобильное меню при клике
                if (navLinks.classList.contains('active')) {
                    navLinks.classList.remove('active');
                }
            });
        });
        
        // Анимация при загрузке
        window.addEventListener('load', () => {
            const heroContent = document.querySelector('.hero-content');
            heroContent.style.animation = 'fadeInUp 1s ease forwards';
            
            const elements = document.querySelectorAll('.skill-card, .achievement-card');
            elements.forEach((el, index) => {
                setTimeout(() => {
                    el.style.animation = 'fadeIn 0.8s ease forwards';
                }, 300 + index * 200);
            });
        });
        
        // Добавляем стили для анимации
        const style = document.createElement('style');
        style.innerHTML = `
            @keyframes fadeInUp {
                from {
                    opacity: 0;
                    transform: translateY(30px);
                }
                to {
                    opacity: 1;
                    transform: translateY(0);
                }
            }
            
            @keyframes fadeIn {
                from {
                    opacity: 0;
                }
                to {
                    opacity: 1;
                }
            }
            
            .hero-content {
                opacity: 0;
            }
            
            .skill-card, .achievement-card {
                opacity: 0;
            }
        `;
        document.head.appendChild(style);
    </script>
</body>
</html>
