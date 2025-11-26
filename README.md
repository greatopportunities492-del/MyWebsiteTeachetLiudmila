<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Learn English with Pleasure</title>
  <style>
    /* Общие стили */
    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    body {
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      background: linear-gradient(135deg, #f5f7fa 0%, #e4edf9 100%);
      color: #333;
      padding: 20px;
      line-height: 1.6;
    }

    header {
      text-align: center;
      margin-bottom: 40px;
      padding: 20px;
    }

    h1 {
      font-size: 2.8rem;
      color: #2c6fbb;
      margin-bottom: 10px;
      text-shadow: 1px 1px 2px rgba(0,0,0,0.05);
    }

    .tagline {
      font-size: 1.2rem;
      color: #5a7d9a;
      max-width: 700px;
      margin: 0 auto;
    }

    /* Сетка курсов */
    .products-grid {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(290px, 1fr));
      gap: 30px;
      max-width: 1200px;
      margin: 0 auto;
    }

    /* Карточка курса */
    .product-card {
      background: white;
      border-radius: 16px;
      box-shadow: 0 6px 20px rgba(0,0,0,0.08);
      overflow: hidden;
      transition: all 0.3s ease;
      display: flex;
      flex-direction: column;
      height: 100%;
    }

    .product-card:hover {
      transform: translateY(-8px);
      box-shadow: 0 10px 25px rgba(0,0,0,0.12);
    }

    .card-icon {
      font-size: 2.2rem;
      text-align: center;
      padding: 20px 0;
      background: #eef6ff;
      color: #2c6fbb;
    }

    .card-content {
      padding: 20px;
      flex-grow: 1;
      display: flex;
      flex-direction: column;
    }

    .card-content h3 {
      margin-bottom: 10px;
      color: #2c6fbb;
    }

    .card-content p {
      font-size: 15px;
      color: #555;
      margin-bottom: 15px;
      flex-grow: 1;
    }

    .price {
      font-weight: bold;
      color: #e74c3c;
      font-size: 1.3rem;
      margin: 8px 0;
    }

    .buy-btn {
      display: block;
      width: 100%;
      padding: 12px;
      background: #2c6fbb;
      color: white;
      border: none;
      border-radius: 8px;
      cursor: pointer;
      font-weight: bold;
      font-size: 16px;
      transition: background 0.2s;
    }

    .buy-btn:hover {
      background: #1e5aa8;
    }

    /* Модальное окно */
    .modal {
      display: none;
      position: fixed;
      z-index: 1000;
      left: 0;
      top: 0;
      width: 100%;
      height: 100%;
      background-color: rgba(0,0,0,0.8);
    }

    .modal-content {
      background: white;
      margin: 5% auto;
      padding: 25px;
      border-radius: 18px;
      width: 90%;
      max-width: 750px;
      position: relative;
      animation: modalFadeIn 0.5s ease-out;
      box-shadow: 0 10px 40px rgba(0,0,0,0.3);
    }

    @keyframes modalFadeIn {
      from { opacity: 0; transform: scale(0.95); }
      to { opacity: 1; transform: scale(1); }
    }

    .close-btn {
      position: absolute;
      top: 15px;
      right: 20px;
      font-size: 28px;
      color: #aaa;
      cursor: pointer;
      font-weight: bold;
    }

    .close-btn:hover {
      color: #2c6fbb;
    }

    /* Карусель */
    .carousel {
      position: relative;
      margin-bottom: 20px;
      border-radius: 12px;
      overflow: hidden;
      height: 280px;
      background: #f8fbff;
    }

    .carousel-images {
      display: flex;
      transition: transform 0.5s ease-in-out;
      height: 100%;
    }

    .carousel-images img {
      min-width: 100%;
      height: 100%;
      object-fit: cover;
    }

    .carousel-nav {
      display: flex;
      justify-content: center;
      margin-top: 12px;
    }

    .carousel-dot {
      width: 10px;
      height: 10px;
      border-radius: 50%;
      background: #ccc;
      margin: 0 6px;
      cursor: pointer;
      transition: background 0.2s;
    }

    .carousel-dot.active {
      background: #2c6fbb;
    }

    .modal-title {
      font-size: 1.8rem;
      color: #2c6fbb;
      margin: 15px 0;
    }

    .modal-description {
      margin: 15px 0;
      color: #444;
    }

    .modal-price {
      font-size: 1.5rem;
      color: #e74c3c;
      font-weight: bold;
      margin: 12px 0;
    }

    .modal-buy-btn {
      padding: 14px 30px;
      background: #2c6fbb;
      color: white;
      border: none;
      border-radius: 8px;
      font-size: 17px;
      font-weight: bold;
      cursor: pointer;
      margin-top: 10px;
    }

    .modal-buy-btn:hover {
      background: #1e5aa8;
    }

    footer {
      text-align: center;
      margin-top: 50px;
      color: #777;
      font-size: 0.95rem;
    }
  </style>
</head>
<body>

  <header>
    <h1>Learn English with Pleasure</h1>
    <p class="tagline">Индивидуальные и групповые занятия с сертифицированным преподавателем. Говорите уверенно, учите легко!</p>
  </header>

  <!-- СЕКЦИЯ С КАРТОЧКАМИ УСЛУГ -->
  <div class="products-grid">

    <!-- Курс 1 -->
    <div class="product-card">
      <div class="card-icon">💬</div>
      <div class="card-content">
        <h3>Разговорный клуб</h3>
        <p>Практикуйте разговорную речь в дружелюбной группе 2 раза в неделю. Темы: путешествия, работа, повседневная жизнь.</p>
        <div class="price">2 500 ₽ / месяц</div>
        <button class="buy-btn" onclick="openModal(0)">Подробнее</button>
      </div>
    </div>

    <!-- Курс 2 -->
    <div class="product-card">
      <div class="card-icon">🎓</div>
      <div class="card-content">
        <h3>Подготовка к ЕГЭ/ОГЭ</h3>
        <p>Интенсивные занятия по формату экзамена: аудирование, чтение, грамматика, эссе. Результат — выше на 30+ баллов!</p>
        <div class="price">4 000 ₽ / 8 уроков</div>
        <button class="buy-btn" onclick="openModal(1)">Подробнее</button>
      </div>
    </div>

    <!-- Курс 3 -->
    <div class="product-card">
      <div class="card-icon">👨‍💻</div>
      <div class="card-content">
        <h3>Индивидуальные уроки</h3>
        <p>Персональная программа под ваши цели: работа, переезд, собеседование или просто любовь к языку.</p>
        <div class="price">1 200 ₽ / урок</div>
        <button class="buy-btn" onclick="openModal(2)">Подробнее</button>
      </div>
    </div>

    <!-- Курс 4 -->
    <div class="product-card">
      <div class="card-icon">✈️</div>
      <div class="card-content">
        <h3>Английский для путешествий</h3>
        <p>Курс из 6 уроков: аэропорт, отель, ресторан, шопинг, экстренные ситуации. Готовы к поездке за 2 недели!</p>
        <div class="price">6 000 ₽ / курс</div>
        <button class="buy-btn" onclick="openModal(3)">Подробнее</button>
      </div>
    </div>

  </div>

  <!-- МОДАЛЬНОЕ ОКНО -->
  <div id="productModal" class="modal">
    <div class="modal-content">
      <span class="close-btn" onclick="closeModal()">&times;</span>

      <div class="carousel">
        <div class="carousel-images" id="modalCarouselImages"></div>
      </div>
      <div class="carousel-nav" id="carouselDots"></div>

      <h2 class="modal-title" id="modalTitle">Course Title</h2>
      <div class="modal-description" id="modalDescription">Full description...</div>
      <div class="modal-price" id="modalPrice">0 ₽</div>
      <button class="modal-buy-btn" id="modalBuyBtn">Записаться</button>
    </div>
  </div>

  <footer>
    <p>© 2025 Learn English with Pleasure — ваш путь к свободному английскому начинается здесь!</p>
  </footer>

  <script>
    // === ДАННЫЕ О КУРСАХ ===
    const courses = [
      {
        title: "Разговорный клуб",
        fullDesc: "Групповые занятия (4–6 человек) 2 раза в неделю по 90 минут. Акцент на свободной речи, произношении и лексике. Темы обсуждения: современные фильмы, работа, хобби, путешествия, культурные различия. Все материалы включены. Уровень: Pre-Intermediate и выше.",
        price: "2 500 ₽ / месяц",
        images: [
          "https://images.unsplash.com/photo-1523580494863-6f3031224c94?ixlib=rb-4.0.3&auto=format&fit=crop&w=600&h=300&q=80",
          "https://images.unsplash.com/photo-1519389950473-47ba0277781c?ixlib=rb-4.0.3&auto=format&fit=crop&w=600&h=300&q=80"
        ],
        buyLink: "#" // ← замените на вашу ссылку (Telegram, форма, WhatsApp и т.д.)
      },
      {
        title: "Подготовка к ЕГЭ/ОГЭ",
        fullDesc: "Программа рассчитана на 2–4 месяца. Включает диагностику, регулярные пробные тесты, разбор ошибок и стратегии выполнения заданий. Работаем с реальными КИМами прошлых лет. Индивидуальный подход и обратная связь после каждого урока.",
        price: "4 000 ₽ / 8 уроков",
        images: [
          "https://images.unsplash.com/photo-1503676260748-184393f5d9d9?ixlib=rb-4.0.3&auto=format&fit=crop&w=600&h=300&q=80",
          "https://images.unsplash.com/photo-1523240795612-9a054b0db644?ixlib=rb-4.0.3&auto=format&fit=crop&w=600&h=300&q=80"
        ],
        buyLink: "#"
      },
      {
        title: "Индивидуальные уроки",
        fullDesc: "Занятия 1 на 1 по Zoom или лично. Программа строится под ваши цели: бизнес-английский, подготовка к собеседованию, улучшение произношения или просто поддержание уровня. Домашние задания по желанию. Гибкое расписание.",
        price: "1 200 ₽ / урок",
        images: [
          "https://images.unsplash.com/photo-1581091226033-d5c48150dbaa?ixlib=rb-4.0.3&auto=format&fit=crop&w=600&h=300&q=80",
          "https://images.unsplash.com/photo-1543269865-cbf427effbad?ixlib=rb-4.0.3&auto=format&fit=crop&w=600&h=300&q=80"
        ],
        buyLink: "#"
      },
      {
        title: "Английский для путешествий",
        fullDesc: "Интенсивный курс из 6 уроков (можно пройти за 1–2 недели). Освоите фразы для аэропорта, отеля, ресторана, шопинга, вызова такси и помощи. Учимся понимать носителей и говорить чётко. Все диалоги — реальные ситуации!",
        price: "6 000 ₽ / курс",
        images: [
          "https://images.unsplash.com/photo-1476514525535-07fb3b4ae5f1?ixlib=rb-4.0.3&auto=format&fit=crop&w=600&h=300&q=80",
          "https://images.unsplash.com/photo-1469474968028-56623f02e42e?ixlib=rb-4.0.3&auto=format&fit=crop&w=600&h=300&q=80"
        ],
        buyLink: "#"
      }
    ];

    // === ПЕРЕМЕННЫЕ ===
    let currentCourseIndex = 0;
    let currentImageIndex = 0;
    const modal = document.getElementById("productModal");
    const carouselImages = document.getElementById("modalCarouselImages");
    const carouselDots = document.getElementById("carouselDots");

    // === ФУНКЦИИ ===
    function openModal(index) {
      currentCourseIndex = index;
      const course = courses[index];

      document.getElementById("modalTitle").textContent = course.title;
      document.getElementById("modalDescription").textContent = course.fullDesc;
      document.getElementById("modalPrice").textContent = course.price;
      document.getElementById("modalBuyBtn").onclick = () => {
        window.location.href = course.buyLink;
      };

      renderCarousel(course.images);
      modal.style.display = "block";
    }

    function closeModal() {
      modal.style.display = "none";
      currentImageIndex = 0;
    }

    function renderCarousel(images) {
      carouselImages.innerHTML = "";
      carouselDots.innerHTML = "";

      images.forEach(src => {
        const img = document.createElement("img");
        img.src = src;
        img.alt = "Course illustration";
        carouselImages.appendChild(img);
      });

      images.forEach((_, i) => {
        const dot = document.createElement("div");
        dot.classList.add("carousel-dot");
        if (i === 0) dot.classList.add("active");
        dot.onclick = () => goToSlide(i);
        carouselDots.appendChild(dot);
      });

      currentImageIndex = 0;
      updateCarousel();
    }

    function goToSlide(index) {
      currentImageIndex = index;
      updateCarousel();
    }

    function updateCarousel() {
      const images = carouselImages.children;
      if (images.length > 0) {
        carouselImages.style.transform = `translateX(-${currentImageIndex * 100}%)`;

        const dots = carouselDots.children;
        for (let i = 0; i < dots.length; i++) {
          dots[i].classList.toggle("active", i === currentImageIndex);
        }
      }
    }

    window.onclick = function(event) {
      if (event.target === modal) {
        closeModal();
      }
    };
  </script>

</body>
</html>

