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
}

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: 'Inter', -apple-system, BlinkMacSystemFont, sans-serif;
    background: linear-gradient(135deg, var(--dark-bg) 0%, var(--darker-bg) 100%);
    color: var(--text-light);
    line-height: 1.6;
    overflow-x: hidden;
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
    font-weight: 800;
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
}

/* Main sections */
main {
    margin-top: 85px;
}

#header1 {
    min-height: 100vh;
    display: flex;
    align-items: center;
    background: linear-gradient(135deg, var(--dark-bg) 0%, var(--darker-bg) 100%);
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
}

.download-btn:hover {
    transform: translateY(-3px);
    box-shadow: 0 15px 40px rgba(0, 255, 255, 0.5);
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
}

.footer_block_1_text_2 a {
    color: var(--primary-color);
    text-decoration: none;
    font-weight: 600;
}

.footer_block_1_text_2 a:hover {
    text-decoration: underline;
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

/* Modal */
.modal-content {
    background: var(--card-bg);
    border: 2px solid var(--primary-color);
    border-radius: 20px;
}

.modal-header {
    border-bottom: 2px solid var(--border-color);
    padding: 25px 30px;
}

.modal-title {
    color: var(--text-light);
    font-weight: 700;
    font-size: 1.5rem;
}

.close {
    color: var(--text-light);
    opacity: 0.8;
    font-size: 2rem;
}

.close:hover {
    color: var(--primary-color);
    opacity: 1;
}

/* Responsive */
@media (max-width: 768px) {
    .header_title {
        font-size: 2.8rem;
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
}

/* Animations */
.animate__fadeInUp {
    animation-duration: 0.8s;
}

.animate__fadeInLeft {
    animation-duration: 0.8s;
}

.animate__fadeInRight {
    animation-duration: 0.8s;
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
    <a href="#main" id="back-to-top" class="back-to-top" title="Наверх">▲</a>
    
    <div id="header" class="animate__animated animate__fadeInDown">
        <div class="container">
            <div class="row">
                <nav class="navbar navbar-expand-md bg-transparent w-100">
                    <a class="navbar-brand" href="#main">
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
                        <div class="header_title animate__animated animate__fadeInUp">
                            AMYR HACK<br>Лучшее Решение
                        </div>
                        <div class="header_text animate__animated animate__fadeInUp">
                            Представляем уникальный продукт с широким функционалом и легкой настройкой, а также быстрой и отзывчивой техподдержкой. Получите преимущество в игре уже сегодня.
                        </div>
                        <div class="header_btn">
                            <a href="#" class="download-btn animate__animated animate__fadeInLeft">СКАЧАТЬ</a>
                            <a href="#advantages" class="animate__animated animate__fadeInRight">УЗНАТЬ БОЛЬШЕ</a>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <section id="advantages">
            <div class="container">
                <div class="container-title animate__animated animate__fadeInUp">
                    <div class="container_title_top">НАШИ</div>
                    <div class="container_title_bot">ПРЕИМУЩЕСТВА</div>
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
                    <div class="container_title_top">КРАТКАЯ</div>
                    <div class="container_title_bot">ИНСТРУКЦИЯ</div>
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
                    <div class="container_title_top">ФУНКЦИОНАЛ</div>
                    <div class="container_title_bot">ПРОДУКТА</div>
                </div>
                
                <div class="row">
                    <div class="col-12 col-md-6 col-lg-4">
                        <div class="functionality_card animate__animated animate__fadeInUp">
                            <div class="functionality_placeholder">
                                ESP Vision
                            </div>
                            <div class="functionality_text">ESP</div>
                        </div>
                    </div>
                    <div class="col-12 col-md-6 col-lg-4">
                        <div class="functionality_card animate__animated animate__fadeInUp">
                            <div class="functionality_placeholder">
                                Auto Aim
                            </div>
                            <div class="functionality_text">AIMBOT</div>
                        </div>
                    </div>
                    <div class="col-12 col-md-6 col-lg-4">
                        <div class="functionality_card animate__animated animate__fadeInUp">
                            <div class="functionality_placeholder">
                                Movement
                            </div>
                            <div class="functionality_text">BUNNY HOP</div>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <section id="social">
            <div class="container">
                <div class="container-title animate__animated animate__fadeInUp">
                    <div class="container_title_top">НАШИ</div>
                    <div class="container_title_bot">КОНТАКТЫ</div>
                </div>
                
                <div class="row justify-content-center">
                    <div class="col-12 col-md-6 col-lg-4">
                        <div class="social_card animate__animated animate__fadeInUp">
                            <a href="#" aria-label="Телеграм"><i class="fab fa-telegram-plane"></i></a>
                            <div class="social_text">Телеграм</div>
                        </div>
                    </div>
                    <div class="col-12 col-md-6 col-lg-4">
                        <div class="social_card animate__animated animate__fadeInUp">
                            <a href="#" aria-label="Discord"><i class="fab fa-discord"></i></a>
                            <div class="social_text">Discord</div>
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
                        <div class="footer_block_1_text_1">AMYR HACK © 2020-2025</div>
                        <div class="footer_block_1_text_2">Все права защищены!</div>
                    </div>
                </div>
                <div class="col-12 col-md-4 mb-4">
                    <div class="footer_block">
                        <div class="footer_block_1_text_1">Документация:</div>
                        <div class="footer_block_1_text_2">
                            <a href="#">Пользовательское соглашение</a>
                        </div>
                    </div>
                </div>
                <div class="col-12 col-md-4 mb-4">
                    <div class="footer_block">
                        <div class="footer_block_1_text_1">Социальные сети:</div>
                        <div class="footer_block_social">
                            <a href="#" aria-label="Телеграм"><i class="fab fa-telegram-plane"></i></a>
                            <a href="#" aria-label="Discord"><i class="fab fa-discord"></i></a>
                            <a href="#" aria-label="Email"><i class="fas fa-envelope"></i></a>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </footer>

    <!-- Modal -->
    <div class="modal fade" id="imageModal" tabindex="-1" role="dialog" aria-labelledby="imageModalLabel" aria-hidden="true">
        <div class="modal-dialog modal-lg modal-dialog-centered" role="document">
            <div class="modal-content">
                <div class="modal-header">
                    <h5 class="modal-title" id="imageModalLabel">Изображение</h5>
                    <button type="button" class="close" data-dismiss="modal" aria-label="Закрыть">
                        <span aria-hidden="true">&times;</span>
                    </button>
                </div>
                <div class="modal-body">
                    <img id="modalImage" src="" alt="" class="img-fluid">
                </div>
            </div>
        </div>
    </div>

    <script src="https://cdnjs.cloudflare.com/ajax/libs/jquery/3.6.0/jquery.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/bootstrap/4.6.2/js/bootstrap.min.js"></script>
    
    <script>
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

        // Download button functionality with improved UX
        document.querySelector('.download-btn').addEventListener('click', function(e) {
            e.preventDefault();
            
            // Show loading state
            const originalText = this.textContent;
            this.textContent = 'ЗАГРУЗКА...';
            this.style.pointerEvents = 'none';
            
            // Simulate download process
            setTimeout(() => {
                alert('Функция скачивания будет доступна в ближайшее время!');
                this.textContent = originalText;
                this.style.pointerEvents = 'auto';
            }, 1500);
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
                    // Unobserve after animation to improve performance
                    observer.unobserve(entry.target);
                }
            });
        }, observerOptions);

        // Observe all cards for animation
        document.addEventListener('DOMContentLoaded', function() {
            const animatedElements = document.querySelectorAll('.advantage-card, .functionality_card, .social_card');
            animatedElements.forEach(el => observer.observe(el));
        });

        // Modal functionality (if needed for future images)
        function openModal(imageSrc, altText = 'Изображение') {
            const modal = document.getElementById('imageModal');
            const modalImage = document.getElementById('modalImage');
            modalImage.src = imageSrc;
            modalImage.alt = altText;
            $('#imageModal').modal('show');
        }

        // Social links functionality (placeholder)
        document.querySelectorAll('.social_card a, .footer_block_social a').forEach(link => {
            link.addEventListener('click', function(e) {
                e.preventDefault();
                const platform = this.querySelector('i').classList.contains('fa-telegram-plane') ? 'Telegram' : 
                               this.querySelector('i').classList.contains('fa-discord') ? 'Discord' : 'Email';
                alert(`Ссылка на ${platform} будет добавлена в ближайшее время!`);
            });
        });

        // Keyboard navigation support
        document.addEventListener('keydown', function(e) {
            if (e.key === 'Escape') {
                $('#imageModal').modal('hide');
            }
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

        // Apply debouncing to scroll events
        const debouncedScrollHandler = debounce(() => {
            // Custom scroll animations can be added here
        }, 10);

        window.addEventListener('scroll', debouncedScrollHandler);

        // Add loading animation to page
        window.addEventListener('load', function() {
            document.body.style.opacity = '1';
            document.body.style.transition = 'opacity 0.5s ease-in-out';
        });

        // Initialize page with loading state
        document.body.style.opacity = '0';
    </script>
</body>
</html>
