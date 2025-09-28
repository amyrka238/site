<!DOCTYPE html>
<html lang="ru">
<head>
<meta name="author" content="your-site.ru">
<meta name="keywords" content="ваши, ключевые, слова">
<meta name="description" content="Описание вашего сайта">
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/bootstrap/4.6.2/css/bootstrap.min.css">
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/animate.css/4.1.1/animate.min.css">
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Ваш сайт - Главная страница</title>

<style>
:root {
    --primary-color: #00ffff;
    --secondary-color: #0080ff;
    --dark-bg: #1a1a1a;
    --darker-bg: #2d2d2d;
    --text-light: #ffffff;
    --text-gray: #cccccc;
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
    background: rgba(26, 26, 26, 0.95);
    backdrop-filter: blur(10px);
    position: fixed;
    top: 0;
    width: 100%;
    z-index: 1000;
    padding: 10px 0;
    transition: all 0.3s ease;
}

.navbar-brand {
    display: flex;
    align-items: center;
    font-size: 24px;
    font-weight: 700;
    color: var(--primary-color) !important;
    text-decoration: none;
}

.header__logo-img {
    width: 40px;
    height: 40px;
    background: var(--primary-color);
    border-radius: 8px;
    margin-right: 12px;
    display: flex;
    align-items: center;
    justify-content: center;
}

.nav-link {
    color: var(--text-gray) !important;
    font-weight: 500;
    margin: 0 10px;
    transition: all 0.3s ease;
    position: relative;
}

.nav-link:hover,
.nav-link.active {
    color: var(--primary-color) !important;
}

/* Main sections */
main {
    margin-top: 80px;
}

#header1 {
    min-height: 80vh;
    display: flex;
    align-items: center;
    background: linear-gradient(135deg, var(--dark-bg) 0%, var(--darker-bg) 100%);
    position: relative;
}

.header_title {
    font-size: 3.5rem;
    font-weight: 800;
    margin-bottom: 20px;
    background: linear-gradient(45deg, var(--primary-color), var(--secondary-color));
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
}

.header_text {
    font-size: 1.2rem;
    color: var(--text-gray);
    margin-bottom: 40px;
    max-width: 600px;
}

.header_btn {
    display: flex;
    gap: 20px;
    flex-wrap: wrap;
}

.header_btn a {
    padding: 15px 30px;
    border-radius: 12px;
    text-decoration: none;
    font-weight: 600;
    text-transform: uppercase;
    transition: all 0.3s ease;
    border: 2px solid transparent;
}

.download-btn {
    background: linear-gradient(45deg, var(--primary-color), var(--secondary-color));
    color: var(--dark-bg) !important;
}

.download-btn:hover {
    transform: translateY(-2px);
    box-shadow: 0 10px 30px rgba(0, 255, 255, 0.3);
}

.header_btn a:nth-child(2) {
    background: transparent;
    color: var(--primary-color) !important;
    border-color: var(--primary-color);
}

.header_btn a:nth-child(2):hover {
    background: var(--primary-color);
    color: var(--dark-bg) !important;
}

/* Sections */
section {
    padding: 80px 0;
}

.container-title {
    text-align: center;
    margin-bottom: 60px;
}

.container_title_top {
    font-size: 1.2rem;
    color: var(--primary-color);
    font-weight: 600;
    letter-spacing: 2px;
}

.container_title_bot {
    font-size: 3rem;
    font-weight: 800;
    color: var(--text-light);
    margin-top: 10px;
}

/* Cards */
.advantage-card,
.functionality_card,
.social_card {
    background: rgba(45, 45, 45, 0.7);
    border-radius: 16px;
    padding: 30px;
    margin-bottom: 30px;
    transition: all 0.3s ease;
    border: 1px solid rgba(0, 255, 255, 0.1);
}

.advantage-card:hover,
.functionality_card:hover,
.social_card:hover {
    transform: translateY(-5px);
    box-shadow: 0 15px 40px rgba(0, 255, 255, 0.2);
    border-color: var(--primary-color);
}

.number {
    width: 60px;
    height: 60px;
    background: linear-gradient(45deg, var(--primary-color), var(--secondary-color));
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 1.5rem;
    font-weight: 700;
    color: var(--dark-bg);
    margin-bottom: 20px;
}

.advantage-card .title,
.functionality_text,
.social_text {
    font-size: 1.5rem;
    font-weight: 700;
    color: var(--text-light);
    margin-bottom: 15px;
}

.discription {
    color: var(--text-gray);
    line-height: 1.7;
}

/* Functionality images placeholder */
.functionality_card img {
    width: 100%;
    height: 200px;
    background: var(--darker-bg);
    border-radius: 12px;
    margin-bottom: 20px;
    display: flex;
    align-items: center;
    justify-content: center;
    border: 2px dashed var(--primary-color);
}

.functionality_card img::before {
    content: "Изображение";
    color: var(--text-gray);
    font-size: 1rem;
}

/* Social cards */
.social_card {
    text-align: center;
}

.social_card a {
    display: inline-block;
    width: 80px;
    height: 80px;
    background: linear-gradient(45deg, var(--primary-color), var(--secondary-color));
    border-radius: 50%;
    margin-bottom: 20px;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 2rem;
    color: var(--dark-bg);
    text-decoration: none;
    transition: all 0.3s ease;
}

.social_card a:hover {
    transform: scale(1.1);
    box-shadow: 0 10px 30px rgba(0, 255, 255, 0.4);
}

/* Footer */
#footer {
    background: var(--darker-bg);
    padding: 40px 0;
    margin-top: 50px;
    border-top: 1px solid rgba(0, 255, 255, 0.2);
}

.footer_block_1_text_1 {
    font-weight: 600;
    color: var(--text-light);
    margin-bottom: 10px;
}

.footer_block_1_text_2 {
    color: var(--text-gray);
}

.footer_block_1_text_2 a {
    color: var(--primary-color);
    text-decoration: none;
}

.footer_block_social {
    display: flex;
    gap: 15px;
}

.footer_block_social a {
    width: 40px;
    height: 40px;
    background: var(--primary-color);
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    color: var(--dark-bg);
    text-decoration: none;
    transition: all 0.3s ease;
}

.footer_block_social a:hover {
    transform: scale(1.1);
}

/* Back to top */
.back-to-top {
    position: fixed;
    bottom: 30px;
    right: 30px;
    width: 50px;
    height: 50px;
    background: var(--primary-color);
    color: var(--dark-bg);
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    text-decoration: none;
    font-weight: 700;
    opacity: 0;
    visibility: hidden;
    transition: all 0.3s ease;
}

.back-to-top.show {
    opacity: 1;
    visibility: visible;
}

/* Modal */
.modal-content {
    background: var(--darker-bg);
    border: 1px solid var(--primary-color);
    border-radius: 16px;
}

.modal-header {
    border-bottom: 1px solid rgba(0, 255, 255, 0.2);
}

.modal-title {
    color: var(--text-light);
}

.close {
    color: var(--text-light);
    opacity: 0.8;
}

.close:hover {
    color: var(--primary-color);
    opacity: 1;
}

/* Responsive */
@media (max-width: 768px) {
    .header_title {
        font-size: 2.5rem;
    }
    
    .container_title_bot {
        font-size: 2rem;
    }
    
    .header_btn {
        flex-direction: column;
    }
    
    .navbar-toggler {
        border: none;
        color: var(--primary-color);
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
</style>
</head>
<body>
    <a href="#top" id="back-to-top" class="back-to-top" title="Back to top">▲</a>
    
    <div id="header" class="animate__animated animate__fadeInDown">
        <div class="container">
            <div class="row">
                <nav class="navbar navbar-expand-md bg-transparent w-100">
                    <a class="navbar-brand" href="#main">
                        <div class="header__logo-img">
                            <i class="fas fa-code"></i>
                        </div>
                        <div class="header__logo-text">
                            ВАШ САЙТ
                        </div>
                    </a>
                    <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarSupportedContent">
                        <i class="fas fa-bars"></i>
                    </button>
                    <div class="collapse navbar-collapse ml-auto" id="navbarSupportedContent">
                        <ul class="navbar-nav ml-auto font-medium w-100">
                            <li class="nav-item"><a class="nav-link" href="#main">ГЛАВНАЯ</a></li>
                            <li class="nav-item"><a class="nav-link" href="#advantages">ПРЕИМУЩЕСТВА</a></li>
                            <li class="nav-item"><a class="nav-link" href="#instruction">ИНСТРУКЦИЯ</a></li>
                            <li class="nav-item"><a class="nav-link" href="#functionality">ФУНКЦИОНАЛ</a></li>
                            <li class="nav-item"><a class="nav-link" href="#social">КОНТАКТЫ</a></li>
                            <li class="nav-item"><a class="nav-link" href="#help">ПОМОЩЬ</a></li>
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
                            amyr hack - Лучшее Решение
                        </div>
                        <div class="header_text animate__animated animate__fadeInUp">
                            Представляем уникальный продукт с широким функционалом и легкой настройкой, а также быстрой и отзывчивой техподдержкой.
                        </div>
                        <div class="header_btn">
                            <a href="#" class="download-btn animate__animated animate__fadeInLeft">СКАЧАТЬ</a>
                            <a href="#" class="animate__animated animate__fadeInRight">УЗНАТЬ БОЛЬШЕ</a>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <section id="advantages" class="top-50">
            <div class="container">
                <div class="container-title animate__animated animate__fadeInUp">
                    <div class="container_title_top">НАШИ</div>
                    <div class="container_title_bot">ПРЕИМУЩЕСТВА</div>
                </div>
                
                <div class="row">
                    <div class="col-12">
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
                    <div class="col-12">
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
                    <div class="col-12">
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

        <section id="instruction" class="top-100">
            <div class="container">
                <div class="container-title animate__animated animate__fadeInUp">
                    <div class="container_title_top">КРАТКАЯ</div>
                    <div class="container_title_bot">ИНСТРУКЦИЯ</div>
                </div>
                
                <div class="row">
                    <div class="col-12">
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
                    <div class="col-12">
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
                    <div class="col-12">
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

        <section id="functionality" class="top-100">
            <div class="container">
                <div class="container-title animate__animated animate__fadeInUp">
                    <div class="container_title_top">ФУНКЦИОНАЛ</div>
                    <div class="container_title_bot">ПРОДУКТА</div>
                </div>
                
                <div class="row">
                    <div >
                        <div class="functionality_card animate__animated animate__fadeInUp">
                            <div style="width: 100%; height: 200px; background: var(--darker-bg); border-radius: 12px; margin-bottom: 20px; display: flex; align-items: center; justify-content: center; border: 2px dashed var(--primary-color); color: var(--text-gray);">
                                Функция 1
                            </div>
                            <div class="functionality_text">esp</div>
                        </div>
                    </div>
                    <div >
                        <div class="functionality_card animate__animated animate__fadeInUp">
                            <div style="width: 100%; height: 200px; background: var(--darker-bg); border-radius: 12px; margin-bottom: 20px; display: flex; align-items: center; justify-content: center; border: 2px dashed var(--primary-color); color: var(--text-gray);">
                                
                            </div>
                            <div class="functionality_text">aimbot</div>
                        </div>
                    </div>
                    <div >
                        <div class="functionality_card animate__animated animate__fadeInUp">
                            <div style="width: 100%; height: 200px; background: var(--darker-bg); border-radius: 12px; margin-bottom: 20px; display: flex; align-items: center; justify-content: center; border: 2px dashed var(--primary-color); color: var(--text-gray);">
                                Функция 3
                            </div>
                            <div class="functionality_text">BunnyHop</div>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <section id="social" class="top-1000">
            <div class="container">
                <div class="container-title animate__animated animate__fadeInUp">
                    <div class="container_title_top">НАШИ</div>
                    <div class="container_title_bot">КОНТАКТЫ</div>
                </div>
                
                <div class="row">
                    <div >
                        <div class="social_card">
                            <a href="#"><i class="fab fa-telegram-plane"></i></a>
                            <div class="social_text">Телеграм</div>
                        </div>
                    </div>
                    <div >
        </section>

        <div class="container" id="footer">
            <div class="row">
                <div >
                    <div class="footer_block">
                        <div class="footer_block_1_text_1">Ваш Сайт © 2020-2025</div>
                        <div class="footer_block_1_text_2">Все права защищены!</div>
                    </div>
                </div>
                <div >
                    <div class="footer_block">
                        <div class="footer_block_1_text_1">Документация:</div>
                        <div class="footer_block_1_text_2">
                            <a href="#">Пользовательское соглашение</a>
                        </div>
                    </div>
                </div>
                <div >
                    <div class="footer_block">
                        <div class="footer_block_1_text_1">Социальные сети:</div>
                        <div class="footer_block_social">
                            <a href="#"><i class="fab fa-telegram-plane"></i></a>
                            <a href="#"><i class="fab fa-"></i></a>
                            <a href="#"><i class="fas fa-envelope"></i></a>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </main>

    <!-- Modal -->
    <div class="modal fade" id="imageModal" tabindex="-1" role="dialog">
        <div class="modal-dialog modal-lg modal-dialog-centered" role="document">
            <div class="modal-content">
                <div class="modal-header">
                    <h5 class="modal-title">Изображение</h5>
                    <button type="button" class="close" data-dismiss="modal">
                        <span>&times;</span>
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
        // Back to top button
        window.addEventListener('scroll', function() {
            const backToTop = document.getElementById('back-to-top');
            if (window.scrollY > 300) {
                backToTop.classList.add('show');
            } else {
                backToTop.classList.remove('show');
            }
        });

        // Smooth scrolling
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                if (target) {
                    target.scrollIntoView({
                        behavior: 'smooth'
                    });
                }
            });
        });

        // Download button functionality
        document.querySelector('.download-btn').addEventListener('click', function(e) {
            e.preventDefault();
            alert('Здесь будет логика скачивания файла');
        });

        // Modal functionality
        function openModal(image) {
            const modalImage = document.getElementById('modalImage');
            modalImage.src = image.src;
        }

        // Add animations on scroll
        const observerOptions = {
            threshold: 0.1,
            rootMargin: '0px 0px -50px 0px'
        };

        const observer = new IntersectionObserver(function(entries) {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('animate__animated', 'animate__fadeInUp');
                }
            });
        }, observerOptions);

        document.querySelectorAll('.advantage-card, .functionality_card, .social_card').forEach(card => {
            observer.observe(card);
        });
    </script>
</body>
</html>
