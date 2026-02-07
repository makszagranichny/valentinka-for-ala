<!DOCTYPE html>
<html lang="ru">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Валентинка для Али 💘</title>
  <style>
    * { box-sizing: border-box; margin: 0; padding: 0; }
    body {
      margin: 0;
      min-height: 100vh;
      display: flex;
      align-items: center;
      justify-content: center;
      background: linear-gradient(45deg, #ff6b9d, #ff8e8e, #ffcc70);
      background-size: 300% 300%;
      animation: gradient 8s ease infinite;
      font-family: 'Arial', sans-serif;
      color: white;
      text-align: center;
      padding: 20px;
      position: relative;
      overflow-x: hidden;
    }
    
    @keyframes gradient {
      0% { background-position: 0% 50%; }
      50% { background-position: 100% 50%; }
      100% { background-position: 0% 50%; }
    }
    
    .container {
      max-width: 500px;
      width: 100%;
      margin: 0 auto;
    }
    
    .card {
      background: rgba(255, 255, 255, 0.15);
      backdrop-filter: blur(10px);
      border-radius: 25px;
      padding: 30px 25px;
      box-shadow: 0 15px 35px rgba(0, 0, 0, 0.2);
      border: 1px solid rgba(255, 255, 255, 0.2);
      position: relative;
      z-index: 2;
    }
    
    .avatar {
      width: 180px;
      height: 180px;
      border-radius: 50%;
      object-fit: cover;
      border: 5px solid rgba(255, 255, 255, 0.7);
      margin: 0 auto 20px;
      display: block;
      box-shadow: 0 10px 25px rgba(0, 0, 0, 0.3);
    }
    
    h1 {
      font-size: 32px;
      margin-bottom: 10px;
      text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.3);
      color: #fff;
    }
    
    .subtitle {
      font-size: 18px;
      margin-bottom: 25px;
      opacity: 0.9;
    }
    
    .question {
      font-size: 22px;
      margin: 25px 0;
      padding: 15px;
      background: rgba(255, 255, 255, 0.1);
      border-radius: 15px;
      font-weight: bold;
    }
    
    .buttons {
      display: flex;
      justify-content: center;
      gap: 20px;
      margin: 30px 0 20px;
      flex-wrap: wrap;
    }
    
    button {
      padding: 15px 30px;
      font-size: 18px;
      font-weight: bold;
      border: none;
      border-radius: 50px;
      cursor: pointer;
      transition: all 0.3s ease;
      min-width: 130px;
      position: relative;
      overflow: hidden;
      z-index: 1;
    }
    
    .yes-btn {
      background: linear-gradient(45deg, #ff3366, #ff6699);
      color: white;
      box-shadow: 0 5px 15px rgba(255, 51, 102, 0.4);
    }
    
    .yes-btn:hover {
      transform: scale(1.05);
      box-shadow: 0 8px 20px rgba(255, 51, 102, 0.6);
    }
    
    .yes-btn:active {
      transform: scale(0.98);
    }
    
    .no-btn {
      background: rgba(255, 255, 255, 0.25);
      color: white;
      border: 2px solid rgba(255, 255, 255, 0.4);
      position: relative;
    }
    
    .no-btn:hover {
      background: rgba(255, 255, 255, 0.35);
    }
    
    .no-btn.moving {
      transition: all 0.5s ease;
    }
    
    .result {
      margin: 25px 0;
      font-size: 26px;
      font-weight: bold;
      color: #ffeb3b;
      text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5);
      display: none;
      animation: pulse 2s infinite;
    }
    
    @keyframes pulse {
      0% { transform: scale(1); }
      50% { transform: scale(1.05); }
      100% { transform: scale(1); }
    }
    
    .my-photos {
      display: none;
      flex-wrap: wrap;
      justify-content: center;
      gap: 15px;
      margin-top: 25px;
      animation: fadeIn 1s ease;
    }
    
    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(20px); }
      to { opacity: 1; transform: translateY(0); }
    }
    
    .my-photos img {
      width: 160px;
      height: 160px;
      border-radius: 15px;
      object-fit: cover;
      border: 4px solid white;
      box-shadow: 0 8px 20px rgba(0, 0, 0, 0.3);
      transition: transform 0.3s ease;
    }
    
    .my-photos img:hover {
      transform: scale(1.05);
    }
    
    .hearts-container {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      pointer-events: none;
      z-index: 1;
    }
    
    .heart {
      position: absolute;
      font-size: 24px;
      animation: floatUp linear forwards;
      opacity: 0.8;
    }
    
    @keyframes floatUp {
      0% {
        transform: translateY(100vh) rotate(0deg);
        opacity: 1;
      }
      100% {
        transform: translateY(-100px) rotate(360deg);
        opacity: 0;
      }
    }
    
    footer {
      margin-top: 30px;
      font-size: 14px;
      opacity: 0.7;
    }
    
    /* Мобильная адаптация */
    @media (max-width: 600px) {
      .card { padding: 25px 20px; }
      .avatar { width: 150px; height: 150px; }
      h1 { font-size: 28px; }
      .question { font-size: 20px; }
      button { padding: 14px 25px; font-size: 17px; min-width: 120px; }
      .my-photos img { width: 140px; height: 140px; }
    }
    
    @media (max-width: 400px) {
      .buttons { flex-direction: column; align-items: center; }
      button { width: 100%; max-width: 250px; }
    }
  </style>
</head>
<body>
  <div class="hearts-container" id="heartsContainer"></div>
  
  <div class="container">
    <div class="card">
      <!-- ФОТО ДЕВУШКИ (АЛИ) -->
      <img src="https://images.unsplash.com/photo-1494790108755-2616b612b786?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=80" 
           alt="Аля" class="avatar" id="girlPhoto">
      
      <h1>Аля 💕</h1>
      <div class="subtitle">Этот сайт создан специально для тебя!</div>
      
      <div class="question" id="question">
        Ты будешь моей валентинкой? 💘
      </div>
      
      <div class="buttons">
        <button class="yes-btn" id="yesBtn" onclick="sayYes()">ДА! 💖</button>
        <button class="no-btn" id="noBtn" onclick="sayNo()">Нет 🙈</button>
      </div>
      
      <div class="result" id="result">
        УРА! Ты сделала меня счастливым! 💘
      </div>
      
      <!-- ВАШИ ФОТОГРАФИИ (появятся после нажатия ДА) -->
      <div class="my-photos" id="myPhotos">
        <div class="photo-container">
          <img src="https://images.unsplash.com/photo-1507003211169-0a1dd7228f2d?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=80" 
               alt="Моё фото 1">
          <p style="margin-top: 8px; font-size: 14px;">Это я 😊</p>
        </div>
        <div class="photo-container">
          <img src="https://images.unsplash.com/photo-1506794778202-cad84cf45f1d?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=80" 
               alt="Моё фото 2">
          <p style="margin-top: 8px; font-size: 14px;">И это тоже я 😎</p>
        </div>
      </div>
      
      <footer>
        Создано с любовью 💝 | Открыто с любого устройства
      </footer>
    </div>
  </div>

  <script>
    // Настройки (МОЖНО ИЗМЕНИТЬ)
    const CONFIG = {
      girlName: "Аля",                      // Имя девушки
      girlPhoto: "her_photo.jpg",           // Фото девушки (загрузите файл или укажите ссылку)
      myPhoto1: "my_photo1.jpg",            // Ваше фото 1
      myPhoto2: "my_photo2.jpg",            // Ваше фото 2
      soundYes: "yes_sound.mp3",            // Звук при согласии (опционально)
    };
    
    // Элементы страницы
    const questionEl = document.getElementById('question');
    const yesBtn = document.getElementById('yesBtn');
    const noBtn = document.getElementById('noBtn');
    const resultEl = document.getElementById('result');
    const myPhotosEl = document.getElementById('myPhotos');
    const heartsContainer = document.getElementById('heartsContainer');
    const girlPhotoEl = document.getElementById('girlPhoto');
    
    let noClickCount = 0;
    const noMessages = [
      "Точно нет? 🥺",
      "Подумай ещё разочек! 💖",
      "Может, передумаешь? 😊",
      "Я буду самым лучшим! 🌟",
      "Ну пожааалуйста! 🥰",
      "Это последний шанс! 😉",
      "Ты уверена? Посмотри на меня внимательно! 😄"
    ];
    
    // Загрузка фото (если нужно поменять ссылки)
    // girlPhotoEl.src = CONFIG.girlPhoto; // Раскомментировать если есть фото
    // document.querySelectorAll('.my-photos img')[0].src = CONFIG.myPhoto1;
    // document.querySelectorAll('.my-photos img')[1].src = CONFIG.myPhoto2;
    
    // Создание сердечек
    function createHeart() {
      const heart = document.createElement('div');
      heart.className = 'heart';
      heart.innerHTML = '💖';
      heart.style.left = Math.random() * 100 + 'vw';
      heart.style.fontSize = (Math.random() * 20 + 20) + 'px';
      heart.style.animationDuration = (Math.random() * 3 + 3) + 's';
      
      heartsContainer.appendChild(heart);
      
      setTimeout(() => {
        heart.remove();
      }, 5000);
    }
    
    // Создаем случайные сердечки
    setInterval(createHeart, 500);
    
    // Обработка наведения на кнопку "Нет"
    noBtn.addEventListener('mouseenter', function() {
      if (noClickCount < 3) {
        const btnWidth = this.offsetWidth;
        const btnHeight = this.offsetHeight;
        
        const maxX = window.innerWidth - btnWidth - 50;
        const maxY = window.innerHeight - btnHeight - 50;
        
        const randomX = Math.floor(Math.random() * maxX);
        const randomY = Math.floor(Math.random() * maxY);
        
        this.style.position = 'fixed';
        this.style.left = randomX + 'px';
        this.style.top = randomY + 'px';
        this.classList.add('moving');
        
        setTimeout(() => {
          this.classList.remove('moving');
        }, 500);
      }
    });
    
    // Функция согласия
    function sayYes() {
      // Воспроизведение звука (если есть)
      try {
        const audio = new Audio(CONFIG.soundYes);
        audio.play().catch(e => console.log("Звук не удалось воспроизвести"));
      } catch(e) {}
      
      // Прячем вопрос и кнопки
      questionEl.style.display = 'none';
      document.querySelector('.buttons').style.display = 'none';
      
      // Показываем результат
      resultEl.style.display = 'block';
      
      // Показываем ВАШИ фотографии
      myPhotosEl.style.display = 'flex';
      
      // Меняем заголовок
      document.querySelector('h1').innerHTML = CONFIG.girlName + ' 💘<br>Моя Валентинка!';
      
      // Создаем много сердечек
      for (let i = 0; i < 50; i++) {
        setTimeout(() => createHeart(), i * 100);
      }
      
      // Конфетти эффект
      createConfetti();
    }
    
    // Функция отказа
    function sayNo() {
      noClickCount++;
      
      if (noClickCount <= noMessages.length) {
        questionEl.textContent = noMessages[noClickCount - 1];
        
        // Увеличиваем кнопку "Да"
        const scale = 1 + (noClickCount * 0.1);
        yesBtn.style.transform = `scale(${scale})`;
        
        // Меняем цвет кнопки "Да"
        yesBtn.style.background = `linear-gradient(45deg, #ff${255 - (noClickCount * 20)}66, #ff${255 - (noClickCount * 15)}99)`;
        
        // После 3 нажатий фиксируем кнопку "Нет"
        if (noClickCount >= 3) {
          noBtn.style.position = 'static';
          noBtn.style.left = 'auto';
          noBtn.style.top = 'auto';
          noBtn.textContent = 'Может, всё-таки ДА? 😉';
          noBtn.style.background = 'rgba(255, 255, 255, 0.4)';
        }
      } else {
        questionEl.innerHTML = 'Ладно... Но я буду ждать! 💘<br><small>(Кнопка "ДА" всё ещё работает!)</small>';
      }
    }
    
    // Эффект конфетти
    function createConfetti() {
      const confettiCount = 100;
      const colors = ['#ff3366', '#ff6699', '#ff9966', '#ffcc00', '#66ccff', '#9966ff'];
      
      for (let i = 0; i < confettiCount; i++) {
        const confetti = document.createElement('div');
        confetti.className = 'heart';
        confetti.innerHTML = ['💖', '💝', '💕', '💘', '❤️', '🧡'][Math.floor(Math.random() * 6)];
        confetti.style.left = Math.random() * 100 + 'vw';
        confetti.style.color = colors[Math.floor(Math.random() * colors.length)];
        confetti.style.fontSize = (Math.random() * 25 + 15) + 'px';
        confetti.style.animationDuration = (Math.random() * 2 + 2) + 's';
        
        heartsContainer.appendChild(confetti);
        
        setTimeout(() => {
          confetti.remove();
        }, 5000);
      }
    }
    
    // Инструкция для пользователя
    console.log("💝 Валентинка для Али готова!");
    console.log("📱 Отправьте ей эту ссылку: " + window.location.href);
    console.log("🖼️ Чтобы поменять фото, измените ссылки в коде");
  </script>
</body>
</html>
