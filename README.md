<!DOCTYPE html>
<html lang="ru">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="author" content="amyr hack">
<meta name="keywords" content="hack, cheat, gaming, aimbot, esp">
<meta name="description" content="amyr hack - лучшее решение для геймеров">
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/bootstrap/4.6.2/css/bootstrap.min.css">
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/animate.css/4.1.1/animate.min.css">
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
<link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@400;700;900&family=JetBrains+Mono:wght@300;400;600&display=swap" rel="stylesheet">
<title>amyr hack - Главная страница</title>

<style>
:root {
    --primary-color: #00ffff;
    --secondary-color: #0080ff;
    --accent-color: #ff0080;
    --dark-bg: #0a0a0a;
    --darker-bg: #1a1a1a;
    --card-bg: #1f1f1f;
    --text-light: #ffffff;
    --text-gray: #cccccc;
    --border-color: rgba(0, 255, 255, 0.2);
    --matrix-green: #00ff41;
    --neon-pink: #ff006f;
    --cyber-blue: #00f5ff;
}

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: 'Orbitron', -apple-system, BlinkMacSystemFont, sans-serif;
    background: var(--dark-bg);
    color: var(--text-light);
    line-height: 1.6;
    overflow-x: hidden;
    cursor: none;
}

/* Custom Cursor */
.cursor {
    position: fixed;
    width: 20px;
    height: 20px;
    border: 2px solid var(--primary-color);
    border-radius: 50%;
    background: rgba(0, 255, 255, 0.1);
    pointer-events: none;
    z-index: 9999;
    mix-blend-mode: difference;
    transition: transform 0.1s ease;
}

.cursor-trail {
    position: fixed;
    width: 8px;
    height: 8px;
    background: var(--primary-color);
    border-radius: 50%;
    pointer-events: none;
    z-index: 9998;
    opacity: 0.7;
}

/* Matrix Rain Background */
#matrix-canvas {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    z-index: -2;
    opacity: 0.1;
}

/* Particles Background */
#particles-js {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    z-index: -1;
}

/* Glitch Effect */
@keyframes glitch {
    0% { transform: translate(0); }
    20% { transform: translate(-2px, 2px); }
    40% { transform: translate(-2px, -2px); }
    60% { transform: translate(2px, 2px); }
    80% { transform: translate(2px, -2px); }
    100% { transform: translate(0); }
}

@keyframes glitch-color {
    0% { 
        text-shadow: 0.05em 0 0 #ff006f, -0.05em -0.025em 0 #00f5ff, 0.025em 0.05em 0 #ffff00;
    }
    15% { 
        text-shadow: 0.05em 0 0 #00f5ff, -0.05em -0.025em 0 #ff006f, 0.025em 0.05em 0 #ffff00;
    }
    49% { 
        text-shadow: 0.05em 0 0 #ffff00, -0.05em -0.025em 0 #ff006f, 0.025em 0.05em 0 #00f5ff;
    }
    50% { 
        text-shadow: 0.05em 0 0 #ff006f, -0.05em -0.025em 0 #ffff00, 0.025em 0.05em 0 #00f5ff;
    }
    99% { 
        text-shadow: 0.05em 0 0 #00f5ff, -0.05em -0.025em 0 #ff006f, 0.025em 0.05em 0 #ffff00;
    }
    100% { 
        text-shadow: 0.05em 0 0 #ff006f, -0.05em -0.025em 0 #00f5ff, 0.025em 0.05em 0 #ffff00;
    }
}

.glitch-text {
    animation: glitch 0.3s, glitch-color 0.1s;
    animation-iteration-count: infinite;
    animation-timing-function: linear;
    animation-direction: alternate-reverse;
}

/* Neon Glow Effects */
@keyframes neon-glow {
    0%, 100% {
        text-shadow: 
            0 0 5px var(--primary-color),
            0 0 10px var(--primary-color),
            0 0 15px var(--primary-color),
            0 0 20px var(--primary-color);
    }
    50% {
        text-shadow: 
            0 0 2px var(--primary-color),
            0 0 5px var(--primary-color),
            0 0 8px var(--primary-color),
            0 0 12px var(--primary-color);
    }
}

.neon-text {
    animation: neon-glow 2s ease-in-out infinite alternate;
}

/* Header */
#header {
    background: rgba(10, 10, 10, 0.95);
    backdrop-filter: blur(15px);
    position: fixed;
    top: 0;
    width: 100%;
    z-index: 1000;
    padding: 15px 0;
    transition: all 0.3s ease;
    border-bottom: 1px solid var(--border-color);
}

.navbar-brand {
    display: flex;
    align-items: center;
    font-size: 28px;
    font-weight: 900;
    color: var(--primary-color) !important;
    text-decoration: none;
    text-transform: uppercase;
    letter-spacing: 2px;
}

.header__logo-img {
    width: 45px;
    height: 45px;
    background: linear-gradient(45deg, var(--primary-color), var(--secondary-color));
    border-radius: 10px;
    margin-right: 15px;
    display: flex;
    align-items: center;
    justify-content: center;
    box-shadow: 0 5px 15px rgba(0, 255, 255, 0.3);
}

.header__logo-img i {
    color: var(--dark-bg);
    font-size: 20px;
}

.nav-link {
    color: var(--text-gray) !important;
    font-weight: 600;
    margin: 0 15px;
    transition: all 0.3s ease;
    position: relative;
    text-transform: uppercase;
    font-size: 14px;
    letter-spacing: 1px;
}

.nav-link:hover,
.nav-link.active {
    color: var(--primary-color) !important;
    transform: translateY(-2px);
    text-shadow: 0 0 10px var(--primary-color);
}

.nav-link::after {
    content: '';
    position: absolute;
    bottom: -5px;
    left: 50%;
    width: 0;
    height: 2px;
    background: var(--primary-color);
    transition: all 0.3s ease;
    transform: translateX(-50%);
}

.nav-link:hover::after {
    width: 100%;
    box-shadow: 0 0 10px var(--primary-color);
}

/* Main sections */
main {
    margin-top: 85px;
}

#header1 {
    min-height: 100vh;
    display: flex;
    align-items: center;
    position: relative;
    overflow: hidden;
}

#header1::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background: radial-gradient(ellipse at center, rgba(0, 255, 255, 0.1) 0%, transparent 70%);
    pointer-events: none;
}

.header_title {
    font-size: 4rem;
    font-weight: 900;
    margin-bottom: 30px;
    background: linear-gradient(45deg, var(--primary-color), var(--secondary-color), var(--accent-color));
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
    text-transform: uppercase;
    letter-spacing: 3px;
    line-height: 1.1;
}

.header_text {
    font-size: 1.3rem;
    color: var(--text-gray);
    margin-bottom: 50px;
    max-width: 650px;
    line-height: 1.8;
    font-family: 'JetBrains Mono', monospace;
}

.header_btn {
    display: flex;
    gap: 25px;
    flex-wrap: wrap;
}

.header_btn a {
    padding: 18px 35px;
    border-radius: 15px;
    text-decoration: none;
    font-weight: 700;
    text-transform: uppercase;
    transition: all 0.3s ease;
    border: 2px solid transparent;
    font-size: 16px;
    letter-spacing: 1px;
    position: relative;
    overflow: hidden;
}

.download-btn {
    background: linear-gradient(45deg, var(--primary-color), var(--secondary-color));
    color: var(--dark-bg) !important;
    box-shadow: 0 10px 30px rgba(0, 255, 255, 0.3);
    position: relative;
}

.download-btn::before {
    content: '';
    position: absolute;
    top: 0;
    left: -100%;
    width: 100%;
    height: 100%;
    background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.2), transparent);
    transition: left 0.5s;
}

.download-btn:hover::before {
    left: 100%;
}

.download-btn:hover {
    transform: translateY(-3px);
    box-shadow: 0 15px 40px rgba(0, 255, 255, 0.5);
}

.private-btn {
    background: linear-gradient(45deg, var(--accent-color), var(--neon-pink));
    color: var(--text-light) !important;
    box-shadow: 0 10px 30px rgba(255, 0, 128, 0.4);
    position: relative;
    border: 1px solid var(--accent-color);
}

.private-btn::before {
    content: '';
    position: absolute;
    top: 0;
    left: -100%;
    width: 100%;
    height: 100%;
    background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.15), transparent);
    transition: left 0.5s;
}

.private-btn:hover::before {
    left: 100%;
}

.private-btn:hover {
    transform: translateY(-3px);
    box-shadow: 0 15px 40px rgba(255, 0, 128, 0.6);
    border-color: var(--neon-pink);
}

.private-btn::after {
    content: '👑';
    position: absolute;
    top: -8px;
    right: -8px;
    font-size: 14px;
    background: var(--accent-color);
    border-radius: 50%;
    width: 24px;
    height: 24px;
    display: flex;
    align-items: center;
    justify-content: center;
    box-shadow: 0 2px 10px rgba(255, 0, 128, 0.5);
}

.header_btn a:nth-child(2) {
    background: transparent;
    color: var(--primary-color) !important;
    border-color: var(--primary-color);
}

.header_btn a:nth-child(2):hover {
    background: var(--primary-color);
    color: var(--dark-bg) !important;
    transform: translateY(-3px);
    box-shadow: 0 15px 40px rgba(0, 255, 255, 0.3);
}

/* Sections */
section {
    padding: 100px 0;
    position: relative;
}

.container-title {
    text-align: center;
    margin-bottom: 80px;
}

.container_title_top {
    font-size: 1.3rem;
    color: var(--primary-color);
    font-weight: 700;
    letter-spacing: 3px;
    text-transform: uppercase;
}

.container_title_bot {
    font-size: 3.5rem;
    font-weight: 900;
    color: var(--text-light);
    margin-top: 15px;
    text-transform: uppercase;
    letter-spacing: 2px;
}

/* Cards */
.advantage-card,
.functionality_card,
.social_card {
    background: var(--card-bg);
    border-radius: 20px;
    padding: 40px;
    margin-bottom: 30px;
    transition: all 0.4s ease;
    border: 2px solid var(--border-color);
    position: relative;
    overflow: hidden;
}

.advantage-card::before,
.functionality_card::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background: linear-gradient(45deg, transparent, rgba(0, 255, 255, 0.05), transparent);
    opacity: 0;
    transition: opacity 0.3s ease;
    pointer-events: none;
}

.advantage-card:hover,
.functionality_card:hover,
.social_card:hover {
    transform: translateY(-8px);
    box-shadow: 0 20px 50px rgba(0, 255, 255, 0.3);
    border-color: var(--primary-color);
}

.advantage-card:hover::before,
.functionality_card:hover::before {
    opacity: 1;
}

.number {
    width: 70px;
    height: 70px;
    background: linear-gradient(45deg, var(--primary-color), var(--secondary-color));
    border-radius: 20px;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 1.8rem;
    font-weight: 900;
    color: var(--dark-bg);
    margin-bottom: 25px;
    box-shadow: 0 10px 25px rgba(0, 255, 255, 0.4);
}

.advantage-card .title,
.functionality_text,
.social_text {
    font-size: 1.8rem;
    font-weight: 800;
    color: var(--text-light);
    margin-bottom: 20px;
    text-transform: uppercase;
    letter-spacing: 1px;
}

.discription {
    color: var(--text-gray);
    line-height: 1.8;
    font-size: 1.1rem;
    font-family: 'JetBrains Mono', monospace;
}

/* Functionality cards */
.functionality_card {
    text-align: center;
}

.functionality_placeholder {
    width: 100%;
    height: 250px;
    background: linear-gradient(135deg, var(--darker-bg), var(--dark-bg));
    border-radius: 15px;
    margin-bottom: 25px;
    display: flex;
    align-items: center;
    justify-content: center;
    border: 2px dashed var(--primary-color);
    color: var(--primary-color);
    font-size: 1.2rem;
    font-weight: 600;
    text-transform: uppercase;
    letter-spacing: 1px;
    position: relative;
    overflow: hidden;
}

.functionality_placeholder::before {
    content: '';
    position: absolute;
    top: 0;
    left: -100%;
    width: 100%;
    height: 100%;
    background: linear-gradient(90deg, transparent, rgba(0, 255, 255, 0.1), transparent);
    animation: shimmer 2s infinite;
}

@keyframes shimmer {
    0% { left: -100%; }
    100% { left: 100%; }
}

/* Social cards */
.social_card {
    text-align: center;
    padding: 50px 40px;
}

.social_card a {
    display: inline-block;
    width: 100px;
    height: 100px;
    background: linear-gradient(45deg, var(--primary-color), var(--secondary-color));
    border-radius: 25px;
    margin-bottom: 25px;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 2.5rem;
    color: var(--dark-bg);
    text-decoration: none;
    transition: all 0.3s ease;
    box-shadow: 0 10px 30px rgba(0, 255, 255, 0.3);
}

.social_card a:hover {
    transform: scale(1.1) rotate(5deg);
    box-shadow: 0 15px 40px rgba(0, 255, 255, 0.5);
}

/* Footer */
#footer {
    background: var(--card-bg);
    padding: 60px 0 40px;
    margin-top: 50px;
    border-top: 2px solid var(--border-color);
    position: relative;
}

#footer::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    height: 2px;
    background: linear-gradient(90deg, var(--primary-color), var(--secondary-color), var(--accent-color));
}

.footer_block_1_text_1 {
    font-weight: 700;
    color: var(--text-light);
    margin-bottom: 15px;
    font-size: 1.2rem;
}

.footer_block_1_text_2 {
    color: var(--text-gray);
    font-size: 1rem;
    font-family: 'JetBrains Mono', monospace;
}

.footer_block_1_text_2 a {
    color: var(--primary-color);
    text-decoration: none;
    font-weight: 600;
}

.footer_block_1_text_2 a:hover {
    text-decoration: underline;
    text-shadow: 0 0 10px var(--primary-color);
}

.footer_block_social {
    display: flex;
    gap: 20px;
    justify-content: center;
}

.footer_block_social a {
    width: 50px;
    height: 50px;
    background: linear-gradient(45deg, var(--primary-color), var(--secondary-color));
    border-radius: 15px;
    display: flex;
    align-items: center;
    justify-content: center;
    color: var(--dark-bg);
    text-decoration: none;
    transition: all 0.3s ease;
    font-size: 1.3rem;
}

.footer_block_social a:hover {
    transform: scale(1.1) rotate(-5deg);
    box-shadow: 0 10px 25px rgba(0, 255, 255, 0.4);
}

/* Back to top */
.back-to-top {
    position: fixed;
    bottom: 30px;
    right: 30px;
    width: 60px;
    height: 60px;
    background: linear-gradient(45deg, var(--primary-color), var(--secondary-color));
    color: var(--dark-bg);
    border-radius: 20px;
    display: flex;
    align-items: center;
    justify-content: center;
    text-decoration: none;
    font-weight: 900;
    font-size: 1.2rem;
    opacity: 0;
    visibility: hidden;
    transition: all 0.3s ease;
    box-shadow: 0 10px 30px rgba(0, 255, 255, 0.3);
}

.back-to-top.show {
    opacity: 1;
    visibility: visible;
}

.back-to-top:hover {
    transform: translateY(-5px) scale(1.1);
    box-shadow: 0 15px 40px rgba(0, 255, 255, 0.5);
}

/* Responsive */
@media (max-width: 768px) {
    body { cursor: auto; }
    .cursor, .cursor-trail { display: none; }
    
    .header_title {
        font-size: 2.8rem;
        line-height: 1.2;
    }
    
    .container_title_bot {
        font-size: 2.5rem;
    }
    
    .header_btn {
        flex-direction: column;
        align-items: center;
    }
    
    .header_btn a {
        width: 100%;
        max-width: 300px;
        text-align: center;
    }
    
    .navbar-toggler {
        border: 2px solid var(--primary-color);
        color: var(--primary-color);
        padding: 8px 12px;
        border-radius: 8px;
    }
    
    .navbar-brand {
        font-size: 24px;
    }
    
    section {
        padding: 60px 0;
    }
    
    .advantage-card,
    .functionality_card,
    .social_card {
        padding: 30px;
    }
    
    .container {
        padding-left: 15px;
        padding-right: 15px;
    }
    
    .footer_block_1_text_2 {
        word-break: break-word;
    }
}

/* Custom scrollbar */
::-webkit-scrollbar {
    width: 8px;
}

::-webkit-scrollbar-track {
    background: var(--darker-bg);
}

::-webkit-scrollbar-thumb {
    background: var(--primary-color);
    border-radius: 4px;
}

::-webkit-scrollbar-thumb:hover {
    background: var(--secondary-color);
}
</style>
</head>
<body>
    <!-- Custom Cursor -->
    <div class="cursor" id="cursor"></div>

    <!-- Matrix Background -->
    <canvas id="matrix-canvas"></canvas>
    
    <!-- Particles Background -->
    <div id="particles-js"></div>

    <a href="#main" id="back-to-top" class="back-to-top" title="Наверх">▲</a>
    
    <div id="header" class="animate__animated animate__fadeInDown">
        <div class="container">
            <div class="row">
                <nav class="navbar navbar-expand-md bg-transparent w-100">
                    <a class="navbar-brand neon-text" href="#main">
                        <div class="header__logo-img">
                            <i class="fas fa-code"></i>
                        </div>
                        <div class="header__logo-text">
                            AMYR HACK
                        </div>
                    </a>
                    <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarSupportedContent">
                        <i class="fas fa-bars"></i>
                    </button>
                    <div class="collapse navbar-collapse ml-auto" id="navbarSupportedContent">
                        <ul class="navbar-nav ml-auto font-medium w-100">
                            <li class="nav-item"><a class="nav-link active" href="#main">ГЛАВНАЯ</a></li>
                            <li class="nav-item"><a class="nav-link" href="#advantages">ПРЕИМУЩЕСТВА</a></li>
                            <li class="nav-item"><a class="nav-link" href="#instruction">ИНСТРУКЦИЯ</a></li>
                            <li class="nav-item"><a class="nav-link" href="#functionality">ФУНКЦИОНАЛ</a></li>
                            <li class="nav-item"><a class="nav-link" href="#social">КОНТАКТЫ</a></li>
                        </ul>
                    </div>
                </nav>
            </div>
        </div>
    </div>

    <main>
        <section id="main" class="header1">
            <div class="container">
                <div class="row align-items-center">
                    <div class="col-12 col-md-6">
                        <!-- Место для изображения или графики -->
                    </div>
                    <div class="col-12 col-md-6">
                        <div class="header_title glitch-text animate__animated animate__fadeInUp">
                            AMYR HACK<br>Лучшее Решение
                        </div>
                        <div class="header_text animate__animated animate__fadeInUp">
                            Представляем уникальный продукт с широким функционалом и легкой настройкой, а также быстрой и отзывчивой техподдержкой. Получите преимущество в игре уже сегодня.
                        </div>
                        <div class="header_btn">
                            <a href="https://t.me/amyr_software/58" target="_blank" class="download-btn animate__animated animate__fadeInLeft">СКАЧАТЬ</a>
                            <a href="https://t.me/amyr_software/45" target="_blank" class="private-btn animate__animated animate__fadeInUp">ПОЛУЧИТЬ ПРИВАТНУЮ ВЕРСИЮ</a>
                            <a href="#advantages" class="animate__animated animate__fadeInRight">УЗНАТЬ БОЛЬШЕ</a>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <section id="advantages">
            <div class="container">
                <div class="container-title animate__animated animate__fadeInUp">
                    <div class="container_title_top neon-text">НАШИ</div>
                    <div class="container_title_bot glitch-text">ПРЕИМУЩЕСТВА</div>
                </div>
                
                <div class="row">
                    <div class="col-12 col-lg-4">
                        <div class="advantage-card animate__animated animate__fadeInUp">
                            <div class="text">
                                <div class="number">1</div>
                                <div class="title">Качество</div>
                                <div class="discription">
                                    Мы следим за отзывами наших клиентов, что помогает нам улучшать функционал и развиваться в лучшую сторону. Частые обновления направлены на улучшение старых функций и добавление новых.
                                </div>
                            </div>
                        </div>
                    </div>
                    <div class="col-12 col-lg-4">
                        <div class="advantage-card animate__animated animate__fadeInUp">
                            <div class="text">
                                <div class="number">2</div>
                                <div class="title">Поддержка</div>
                                <div class="discription">
                                    Поддержка проекта работает круглосуточно и готова помочь в решении вопросов и проблем. Наш чат-бот поможет найти решение частых проблем, не дожидаясь ответа специалиста.
                                </div>
                            </div>
                        </div>
                    </div>
                    <div class="col-12 col-lg-4">
                        <div class="advantage-card animate__animated animate__fadeInUp">
                            <div class="text">
                                <div class="number">3</div>
                                <div class="title">Забота о пользователях</div>
                                <div class="discription">
                                    Мы по-настоящему заботимся о наших пользователях! Высококачественная поддержка всегда готова помочь, интерфейс интуитивно понятен, а для постоянных пользователей мы предлагаем бесплатный и качественный продукт.
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <section id="instruction">
            <div class="container">
                <div class="container-title animate__animated animate__fadeInUp">
                    <div class="container_title_top neon-text">КРАТКАЯ</div>
                    <div class="container_title_bot glitch-text">ИНСТРУКЦИЯ</div>
                </div>
                
                <div class="row">
                    <div class="col-12 col-lg-4">
                        <div class="advantage-card animate__animated animate__fadeInUp">
                            <div class="text">
                                <div class="number">1</div>
                                <div class="title">Установка</div>
                                <div class="discription">
                                    Скачайте приложение всего в 1 клик! Просто нажмите "Скачать" и у вас установится приложение, которое мы будем использовать для работы.
                                </div>
                            </div>
                        </div>
                    </div>
                    <div class="col-12 col-lg-4">
                        <div class="advantage-card animate__animated animate__fadeInUp">
                            <div class="text">
                                <div class="number">2</div>
                                <div class="title">Запуск</div>
                                <div class="discription">
                                    Приложение запускается очень просто! Запустите наш лаунчер от имени администратора, после чего нужно нажать кнопку "Запустить". Все необходимые компоненты запустятся автоматически.
                                </div>
                            </div>
                        </div>
                    </div>
                    <div class="col-12 col-lg-4">
                        <div class="advantage-card animate__animated animate__fadeInUp">
                            <div class="text">
                                <div class="number">3</div>
                                <div class="title">Настройки</div>
                                <div class="discription">
                                    Настройка очень простая! Нажмите "Настройки" для загрузки готовых конфигураций. Перенесите файлы в указанную папку и загрузите их в приложении. Готово!
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <section id="functionality">
            <div class="container">
                <div class="container-title animate__animated animate__fadeInUp">
                    <div class="container_title_top neon-text">ФУНКЦИОНАЛ</div>
                    <div class="container_title_bot glitch-text">ПРОДУКТА</div>
                </div>
                
                <div class="row">
                    <div class="col-12 col-md-6 col-lg-4">
                        <div class="functionality_card animate__animated animate__fadeInUp">
                            <div class="functionality_placeholder">
                                ESP Vision
                            </div>
                            <div class="functionality_text neon-text">ESP</div>
                        </div>
                    </div>
                    <div class="col-12 col-md-6 col-lg-4">
                        <div class="functionality_card animate__animated animate__fadeInUp">
                            <div class="functionality_placeholder">
                                Auto Aim
                            </div>
                            <div class="functionality_text neon-text">AIMBOT</div>
                        </div>
                    </div>
                    <div class="col-12 col-md-6 col-lg-4">
                        <div class="functionality_card animate__animated animate__fadeInUp">
                            <div class="functionality_placeholder">
                                Movement
                            </div>
                            <div class="functionality_text neon-text">BUNNY HOP</div>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <section id="social">
            <div class="container">
                <div class="container-title animate__animated animate__fadeInUp">
                    <div class="container_title_top neon-text">НАШИ</div>
                    <div class="container_title_bot glitch-text">КОНТАКТЫ</div>
                </div>
                
                <div class="row justify-content-center">
                    <div class="col-12 col-md-6 col-lg-4">
                        <div class="social_card animate__animated animate__fadeInUp">
                            <a href="https://t.me/amyr_software" target="_blank" aria-label="Наш канал"><i class="fab fa-telegram-plane"></i></a>
                            <div class="social_text neon-text">НАШ КАНАЛ</div>
                        </div>
                    </div>
                    <div class="col-12 col-md-6 col-lg-4">
                        <div class="social_card animate__animated animate__fadeInUp">
                            <a href="https://t.me/Amyr_shik" target="_blank" aria-label="Тех поддержка"><i class="fas fa-headset"></i></a>
                            <div class="social_text neon-text">ПОДДЕРЖКА</div>
                        </div>
                    </div>
                </div>
            </div>
        </section>
    </main>

    <footer id="footer">
        <div class="container">
            <div class="row">
                <div class="col-12 col-md-4 mb-4">
                    <div class="footer_block">
                        <div class="footer_block_1_text_1 neon-text">AMYR HACK © 2025</div>
                        <div class="footer_block_1_text_2">Все права защищены!</div>
                    </div>
                </div>
                <div class="col-12 col-md-4 mb-4">
                    <div class="footer_block">
                        <div class="footer_block_1_text_1">Связь с нами:</div>
                        <div class="footer_block_1_text_2">
                            <a href="https://t.me/amyr_software" target="_blank">Наш канал</a><br>
                            <a href="https://t.me/Amyr_shik" target="_blank">Поддержка</a>
                        </div>
                    </div>
                </div>
                <div class="col-12 col-md-4 mb-4">
                    <div class="footer_block">
                        <div class="footer_block_1_text_1">Социальные сети:</div>
                        <div class="footer_block_social">
                            <a href="https://t.me/amyr_software" target="_blank" aria-label="Наш канал"><i class="fab fa-telegram-plane"></i></a>
                            <a href="https://t.me/Amyr_shik" target="_blank" aria-label="Поддержка"><i class="fas fa-headset"></i></a>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </footer>

    <!-- Scripts -->
    <script src="https://cdnjs.cloudflare.com/ajax/libs/jquery/3.6.0/jquery.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/bootstrap/4.6.2/js/bootstrap.min.js"></script>
    <script src="https://cdn.jsdelivr.net/npm/particles.js@2.0.0/particles.min.js"></script>
    
    <script>
        // Custom Cursor
        const cursor = document.getElementById('cursor');
        const trails = [];
        const trailLength = 5;

        // Create cursor trails
        for (let i = 0; i < trailLength; i++) {
            const trail = document.createElement('div');
            trail.className = 'cursor-trail';
            document.body.appendChild(trail);
            trails.push(trail);
        }

        let mouseX = 0, mouseY = 0;
        let currentX = 0, currentY = 0;

        document.addEventListener('mousemove', (e) => {
            mouseX = e.clientX;
            mouseY = e.clientY;
        });

        function updateCursor() {
            currentX += (mouseX - currentX) * 0.1;
            currentY += (mouseY - currentY) * 0.1;
            
            cursor.style.left = currentX + 'px';
            cursor.style.top = currentY + 'px';

            // Update trails
            trails.forEach((trail, index) => {
                setTimeout(() => {
                    trail.style.left = currentX + 'px';
                    trail.style.top = currentY + 'px';
                    trail.style.opacity = (trailLength - index) / trailLength * 0.7;
                }, index * 50);
            });

            requestAnimationFrame(updateCursor);
        }
        updateCursor();

        // Matrix Rain Effect
        const canvas = document.getElementById('matrix-canvas');
        const ctx = canvas.getContext('2d');

        canvas.width = window.innerWidth;
        canvas.height = window.innerHeight;

        const matrix = "АМУR0123456789АБВГДЕЖЗИЙКЛМНОПРСТУФХЦЧШЩЫЭЮЯabcdefghijklmnopqrstuvwxyz";
        const matrixArray = matrix.split("");

        const fontSize = 10;
        const columns = canvas.width / fontSize;

        const drops = [];
        for (let x = 0; x < columns; x++) {
            drops[x] = 1;
        }

        function drawMatrix() {
            ctx.fillStyle = 'rgba(0, 0, 0, 0.04)';
            ctx.fillRect(0, 0, canvas.width, canvas.height);

            ctx.fillStyle = '#00ff41';
            ctx.font = fontSize + 'px monospace';

            for (let i = 0; i < drops.length; i++) {
                const text = matrixArray[Math.floor(Math.random() * matrixArray.length)];
                ctx.fillText(text, i * fontSize, drops[i] * fontSize);

                if (drops[i] * fontSize > canvas.height && Math.random() > 0.975) {
                    drops[i] = 0;
                }
                drops[i]++;
            }
        }

        setInterval(drawMatrix, 35);

        // Particles.js Configuration
        particlesJS('particles-js', {
            particles: {
                number: { value: 80, density: { enable: true, value_area: 800 }},
                color: { value: "#00ffff" },
                shape: {
                    type: "circle",
                    stroke: { width: 0, color: "#000000" }
                },
                opacity: {
                    value: 0.5,
                    random: false,
                    anim: { enable: false }
                },
                size: {
                    value: 3,
                    random: true,
                    anim: { enable: false }
                },
                line_linked: {
                    enable: true,
                    distance: 150,
                    color: "#00ffff",
                    opacity: 0.4,
                    width: 1
                },
                move: {
                    enable: true,
                    speed: 2,
                    direction: "none",
                    random: false,
                    straight: false,
                    out_mode: "out",
                    bounce: false,
                    attract: { enable: false }
                }
            },
            interactivity: {
                detect_on: "canvas",
                events: {
                    onhover: { enable: true, mode: "repulse" },
                    onclick: { enable: true, mode: "push" },
                    resize: true
                },
                modes: {
                    grab: { distance: 400, line_linked: { opacity: 1 }},
                    bubble: { distance: 400, size: 40, duration: 2, opacity: 8, speed: 3 },
                    repulse: { distance: 200, duration: 0.4 },
                    push: { particles_nb: 4 },
                    remove: { particles_nb: 2 }
                }
            },
            retina_detect: true
        });

        // Smooth scrolling for navigation
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                if (target) {
                    const headerOffset = 100;
                    const elementPosition = target.offsetTop;
                    const offsetPosition = elementPosition - headerOffset;
                    
                    window.scrollTo({
                        top: offsetPosition,
                        behavior: 'smooth'
                    });
                }
            });
        });

        // Active navigation link highlighting
        window.addEventListener('scroll', function() {
            const sections = document.querySelectorAll('section[id]');
            const navLinks = document.querySelectorAll('.nav-link');
            
            let current = '';
            sections.forEach(section => {
                const sectionTop = section.offsetTop;
                const sectionHeight = section.clientHeight;
                if (scrollY >= sectionTop - 200) {
                    current = section.getAttribute('id');
                }
            });

            navLinks.forEach(link => {
                link.classList.remove('active');
                if (link.getAttribute('href') === '#' + current) {
                    link.classList.add('active');
                }
            });
        });

        // Back to top button functionality
        window.addEventListener('scroll', function() {
            const backToTop = document.getElementById('back-to-top');
            if (window.scrollY > 300) {
                backToTop.classList.add('show');
            } else {
                backToTop.classList.remove('show');
            }
        });

        // Header scroll effect
        window.addEventListener('scroll', function() {
            const header = document.getElementById('header');
            if (window.scrollY > 50) {
                header.style.background = 'rgba(10, 10, 10, 0.98)';
                header.style.backdropFilter = 'blur(20px)';
            } else {
                header.style.background = 'rgba(10, 10, 10, 0.95)';
                header.style.backdropFilter = 'blur(15px)';
            }
        });

        // Intersection Observer for animations
        const observerOptions = {
            threshold: 0.1,
            rootMargin: '0px 0px -50px 0px'
        };

        const observer = new IntersectionObserver(function(entries) {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('animate__animated', 'animate__fadeInUp');
                    observer.unobserve(entry.target);
                }
            });
        }, observerOptions);

        // Observe all cards for animation
        document.addEventListener('DOMContentLoaded', function() {
            const animatedElements = document.querySelectorAll('.advantage-card, .functionality_card, .social_card');
            animatedElements.forEach(el => observer.observe(el));
        });

        // Performance optimization: Debounced scroll handler
        function debounce(func, wait) {
            let timeout;
            return function executedFunction(...args) {
                const later = () => {
                    clearTimeout(timeout);
                    func(...args);
                };
                clearTimeout(timeout);
                timeout = setTimeout(later, wait);
            };
        }

        // Glitch effect trigger on hover
        document.querySelectorAll('.glitch-text').forEach(element => {
            element.addEventListener('mouseenter', function() {
                this.style.animationDuration = '0.1s';
            });
            
            element.addEventListener('mouseleave', function() {
                this.style.animationDuration = '2s';
            });
        });

        // Random glitch effect
        setInterval(() => {
            const glitchElements = document.querySelectorAll('.glitch-text');
            const randomElement = glitchElements[Math.floor(Math.random() * glitchElements.length)];
            if (randomElement) {
                randomElement.style.animationDuration = '0.1s';
                setTimeout(() => {
                    randomElement.style.animationDuration = '2s';
                }, 200);
            }
        }, 5000);

        // Dynamic color changes for neon elements
        setInterval(() => {
            const neonElements = document.querySelectorAll('.neon-text');
            const colors = ['#00ffff', '#ff006f', '#00ff41', '#ffff00', '#ff4500'];
            const randomColor = colors[Math.floor(Math.random() * colors.length)];
            
            neonElements.forEach(el => {
                el.style.setProperty('--primary-color', randomColor);
            });
        }, 8000);

        // Resize handling
        window.addEventListener('resize', function() {
            canvas.width = window.innerWidth;
            canvas.height = window.innerHeight;
        });

        // Apply debouncing to scroll events
        const debouncedScrollHandler = debounce(() => {
            // Additional scroll animations can be added here
        }, 10);

        window.addEventListener('scroll', debouncedScrollHandler);
    </script>
</body>
</html>
