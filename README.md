# my-pet-project

<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Приют для домашних животных</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f4f4f4;
            color: #333;
        }
        header {
            background-color: #4CAF50;
            padding: 20px;
            text-align: center;
            color: white;
        }
        nav {
            display: flex;
            justify-content: center;
            padding: 10px 0;
            background-color: #333;
        }
        nav a {
            margin: 0 15px;
            color: white;
            text-decoration: none;
            font-weight: bold;
        }
        .banner {
            position: relative;
            height: 300px;
            background-color: #ddd;
            text-align: center;
            color: white;
            background-image: url('banner-image.jpg');
            background-size: cover;
            background-position: center;
            display: flex;
            align-items: center;
            justify-content: center;
        }
        .banner h2 {
            font-size: 36px;
            margin: 0;
        }
        .content {
            padding: 20px;
            max-width: 1200px;
            margin: 0 auto;
        }
        .about, .contacts {
            background-color: white;
            padding: 20px;
            margin-bottom: 20px;
            border-radius: 5px;
            box-shadow: 0 0 10px rgba(0,0,0,0.1);
        }
        .about h2, .contacts h2 {
            margin-top: 0;
        }
        .slider {
            position: relative;
            overflow: hidden;
            border-radius: 5px;
            box-shadow: 0 0 10px rgba(0,0,0,0.1);
            margin-bottom: 20px;
        }
        .slides {
            display: flex;
            transition: transform 0.5s ease-in-out;
        }
        .slide {
            min-width: 100%;
            box-sizing: border-box;
            background-color: #ccc;
            padding: 40px;
            text-align: center;
            font-size: 24px;
        }
        .animals-adopted {
            background-color: white;
            padding: 20px;
            margin-bottom: 20px;
            border-radius: 5px;
            box-shadow: 0 0 10px rgba(0,0,0,0.1);
        }
        .animals-adopted h2 {
            text-align: center;
            margin-top: 0;
        }
        .animals-list {
            display: flex;
            justify-content: space-around;
            flex-wrap: wrap;
        }
        .animal {
            width: 30%;
            margin-bottom: 20px;
            background-color: #f9f9f9;
            padding: 15px;
            text-align: center;
            border-radius: 5px;
            box-shadow: 0 0 10px rgba(0,0,0,0.1);
        }
        .animal img {
            max-width: 100%;
            border-radius: 5px;
        }
        footer {
            background-color: #333;
            color: white;
            text-align: center;
            padding: 10px 0;
            margin-top: 20px;
        }
    </style>
</head>
<body>

    <header>
        <h1>Приют для домашних животных</h1>
    </header>

    <nav>
        <a href="#cats">Кошки</a>
        <a href="#dogs">Собаки</a>
    </nav>

    <div class="banner">
        <h2>Добро пожаловать в наш приют</h2>
    </div>

    <div class="content">

        <div class="about">
            <h2>О нашем приюте</h2>
            <p>Наш приют существует для того, чтобы помогать бездомным животным находить новые дома и заботливых хозяев. Мы предоставляем временное убежище, медицинскую помощь и любовь всем нашим подопечным.</p>
        </div>

        <div class="slider">
            <div class="slides">
                <div class="slide">Слайд 1</div>
                <div class="slide">Слайд 2</div>
                <div class="slide">Слайд 3</div>
            </div>
        </div>

        <div class="animals-adopted">
            <h2>Животные, нашедшие семью</h2>
            <div class="animals-list">
                <div class="animal">
                    <img src="cat1.jpg" alt="Кошка 1">
                    <p>Мурка нашла новый дом!</p>
                </div>
                <div class="animal">
                    <img src="dog1.jpg" alt="Собака 1">
                    <p>Бобик теперь живет с новой семьей!</p>
                </div>
                <div class="animal">
                    <img src="cat2.jpg" alt="Кошка 2">
                    <p>Маша обрела дом!</p>
                </div>
            </div>
        </div>

        <div class="contacts">
            <h2>Контакты</h2>
            <p>Адрес: ул. Примерная, 123, Москва</p>
            <p>Телефон: +7 (495) 123-45-67</p>
            <p>Email: info@priut.com</p>
        </div>

    </div>

    <footer>
        <p>&copy; 2024 Приют для домашних животных. Все права защищены.</p>
    </footer>

    <script>
        // Слайдер
        let currentSlide = 0;
        const slides = document.querySelectorAll('.slide');
        const totalSlides = slides.length;

        function showSlide(index) {
            const slidesContainer = document.querySelector('.slides');
            if (index >= totalSlides) {
                currentSlide = 0;
            } else if (index < 0) {
                currentSlide = totalSlides - 1;
            } else {
                currentSlide = index;
            }
            const offset = -currentSlide * 100;
            slidesContainer.style.transform = `translateX(${offset}%)`;
        }

        setInterval(() => {
            showSlide(currentSlide + 1);
        }, 3000);
    </script>

</body>
</html>
