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
    
    .avatar.error {
      border-color: #ff6b6b;
      background: rgba(255, 107, 107, 0.1);
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
    
    .my-photos img.error {
      border-color: #ff6b6b;
      filter: grayscale(50%);
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
    
    .error-message {
      color: #ff6b6b;
      background: rgba(255, 255, 255, 0.1);
      padding: 10px;
      border-radius: 10px;
      margin: 10px 0;
      font-size: 14px;
      display: none;
    }
    
    .success-message {
      color: #4caf50;
      background: rgba(255, 255, 255, 0.1);
      padding: 10px;
      border-radius: 10px;
      margin: 10px 0;
      font-size: 14px;
      display: none;
    }
    
    .loading {
      display: inline-block;
      width: 20px;
      height: 20px;
      border: 3px solid rgba(255,255,255,.3);
      border-radius: 50%;
      border-top-color: #fff;
      animation: spin 1s ease-in-out infinite;
    }
    
    @keyframes spin {
      to { transform: rotate(360deg); }
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
    
    .debug-info {
      position: fixed;
      bottom: 10px;
      right: 10px;
      background: rgba(0,0,0,0.7);
      color: white;
      padding: 10px;
      border-radius: 5px;
      font-size: 12px;
      z-index: 100;
      display: none;
    }
  </style>
</head>
<body>
  <div class="hearts-container" id="heartsContainer"></div>
  <div class="debug-info" id="debugInfo"></div>
  
  <div class="container">
    <div class="card">
      <!-- ФОТО АЛИ -->
      <img src="" alt="Аля" class="avatar" id="girlPhoto">
      <div id="photoError" class="error-message"></div>
      <div id="photoSuccess" class="success-message"></div>
      
      <h1 id="girlName">Загрузка...</h1>
      <div class="subtitle" id="subtitle">Идет загрузка валентинки...</div>
      
      <div class="question" id="question">
        Ты будешь моей валентинкой? 💘
      </div>
      
      <div class="buttons">
        <button class="yes-btn" id="yesBtn" onclick="sayYes()" disabled>ДА! 💖</button>
        <button class="no-btn" id="noBtn" onclick="sayNo()" disabled>Нет 🙈</button>
      </div>
      
      <div class="result" id="result">
        УРА! Ты сделала меня счастливым! 💘
      </div>
      
      <!-- ВАШИ ФОТОГРАФИИ -->
      <div class="my-photos" id="myPhotos">
        <div class="photo-container">
          <img src="" alt="Моё фото 1" id="myPhoto1">
          <p style="margin-top: 8px; font-size: 14px;">Это я 😊</p>
        </div>
        <div class="photo-container">
          <img src="" alt="Моё фото 2" id="myPhoto2">
          <p style="margin-top: 8px; font-size: 14px;">И это тоже я 😎</p>
        </div>
      </div>
      
      <footer>
        Создано с любовью 💝 | Открыто с любого устройства
      </footer>
    </div>
  </div>

  <script>
    // ⚙️ НАСТРОЙКИ - ИЗМЕНЕНО ПОД ВАШИ ФАЙЛЫ!
    const CONFIG = {
      girlName: "Аля",                      // Имя девушки
      girlPhoto: "alya.jpg",                // Фото Али - файл alya.jpg
      myPhoto1: "my1.jpg",                  // Ваше фото 1 - файл my1.jpg
      myPhoto2: "my2.jpg",                  // Ваше фото 2 - файл my2.jpg
      soundYes: "",                         // Звук при согласии
    };
    
    // Проверяем, в какой папке лежат файлы
    function detectFilePath(filename) {
      // Сначала пробуем напрямую
      return filename;
    }
    
    // Элементы страницы
    const questionEl = document.getElementById('question');
    const yesBtn = document.getElementById('yesBtn');
    const noBtn = document.getElementById('noBtn');
    const resultEl = document.getElementById('result');
    const myPhotosEl = document.getElementById('myPhotos');
    const heartsContainer = document.getElementById('heartsContainer');
    const girlPhotoEl = document.getElementById('girlPhoto');
    const myPhoto1El = document.getElementById('myPhoto1');
    const myPhoto2El = document.getElementById('myPhoto2');
    const girlNameEl = document.getElementById('girlName');
    const subtitleEl = document.getElementById('subtitle');
    const photoErrorEl = document.getElementById('photoError');
    const photoSuccessEl = document.getElementById('photoSuccess');
    const debugInfo = document.getElementById('debugInfo');
    
    let noClickCount = 0;
    let photosLoaded = 0;
    const totalPhotos = 3;
    let isAllPhotosLoaded = false;
    
    const noMessages = [
      "Точно нет? 🥺",
      "Подумай ещё разочек! 💖",
      "Может, передумаешь? 😊",
      "Я буду самым лучшим! 🌟",
      "Ну пожааалуйста! 🥰",
      "Это последний шанс! 😉",
      "Ты уверена? Посмотри на меня внимательно! 😄"
    ];
    
    // Показываем отладочную информацию
    function showDebugInfo() {
      const baseUrl = window.location.origin + window.location.pathname.replace(/\/[^\/]*$/, '/');
      debugInfo.innerHTML = `
        Файлы ищутся по путям:<br>
        1. ${baseUrl}${CONFIG.girlPhoto}<br>
        2. ${baseUrl}${CONFIG.myPhoto1}<br>
        3. ${baseUrl}${CONFIG.myPhoto2}<br>
        Загружено: ${photosLoaded}/${totalPhotos}
      `;
      debugInfo.style.display = 'block';
    }
    
    // Функция загрузки фото
    function loadPhoto(imgElement, photoUrl, photoName) {
      return new Promise((resolve) => {
        const img = new Image();
        const timer = setTimeout(() => {
          if (!img.complete) {
            console.error(`Таймаут загрузки: ${photoName}`);
            resolve(false);
          }
        }, 15000);
        
        img.onload = () => {
          clearTimeout(timer);
          imgElement.src = photoUrl;
          imgElement.alt = photoName;
          photosLoaded++;
          checkAllPhotosLoaded();
          console.log(`✅ Загружено: ${photoName}`);
          resolve(true);
        };
        
        img.onerror = () => {
          clearTimeout(timer);
          imgElement.classList.add('error');
          photosLoaded++;
          checkAllPhotosLoaded();
          console.error(`❌ Ошибка: ${photoName} - ${photoUrl}`);
          resolve(false);
        };
        
        // Пробуем загрузить
        img.src = photoUrl;
        
        // Показываем отладочную информацию
        showDebugInfo();
      });
    }
    
    // Проверка загрузки всех фото
    function checkAllPhotosLoaded() {
      if (photosLoaded === totalPhotos) {
        isAllPhotosLoaded = true;
        yesBtn.disabled = false;
        noBtn.disabled = false;
        yesBtn.textContent = 'ДА! 💖';
        noBtn.textContent = 'Нет 🙈';
        
        photoSuccessEl.textContent = '✅ Все фото загружены! Можно нажимать кнопки!';
        photoSuccessEl.style.display = 'block';
        photoErrorEl.style.display = 'none';
        
        girlNameEl.innerHTML = CONFIG.girlName + ' 💕';
        subtitleEl.innerHTML = 'Этот сайт создан специально для тебя!';
        
        console.log('✅ Все фото успешно загружены!');
      } else {
        photoErrorEl.innerHTML = `Загружено фото: ${photosLoaded}/${totalPhotos} <span class="loading"></span>`;
        photoErrorEl.style.display = 'block';
      }
    }
    
    // Загрузка всех фото с проверкой нескольких путей
    async function loadAllPhotos() {
      photoErrorEl.innerHTML = 'Начинаю загрузку фото... <span class="loading"></span>';
      photoErrorEl.style.display = 'block';
      photoSuccessEl.style.display = 'none';
      
      console.log('📷 Начинаю загрузку фото с именами:');
      console.log('1. Фото Али:', CONFIG.girlPhoto);
      console.log('2. Ваше фото 1:', CONFIG.myPhoto1);
      console.log('3. Ваше фото 2:', CONFIG.myPhoto2);
      
      // Пробуем разные пути
      const paths = {
        girl: [CONFIG.girlPhoto, `Loveyou/${CONFIG.girlPhoto}`, `/${CONFIG.girlPhoto}`],
        photo1: [CONFIG.myPhoto1, `Loveyou/${CONFIG.myPhoto1}`, `/${CONFIG.myPhoto1}`],
        photo2: [CONFIG.myPhoto2, `Loveyou/${CONFIG.myPhoto2}`, `/${CONFIG.myPhoto2}`]
      };
      
      // Загружаем фото Али
      let girlLoaded = false;
      for (const path of paths.girl) {
        if (await loadPhoto(girlPhotoEl, path, `Фото Али (${path})`)) {
          girlLoaded = true;
          break;
        }
      }
      
      // Загружаем ваши фото
      let photo1Loaded = false;
      for (const path of paths.photo1) {
        if (await loadPhoto(myPhoto1El, path, `Ваше фото 1 (${path})`)) {
          photo1Loaded = true;
          break;
        }
      }
      
      let photo2Loaded = false;
      for (const path of paths.photo2) {
        if (await loadPhoto(myPhoto2El, path, `Ваше фото 2 (${path})`)) {
          photo2Loaded = true;
          break;
        }
      }
      
      // Если не все фото загрузились, показываем помощь
      if (!girlLoaded || !photo1Loaded || !photo2Loaded) {
        const baseUrl = window.location.origin + window.location.pathname.replace(/\/[^\/]*$/, '/');
        photoErrorEl.innerHTML = `
          ⚠️ Проблема с загрузкой фото!<br><br>
          <strong>Проверьте ссылки:</strong><br>
          1. <a href="${baseUrl}alya.jpg" target="_blank">${baseUrl}alya.jpg</a><br>
          2. <a href="${baseUrl}my1.jpg" target="_blank">${baseUrl}my1.jpg</a><br>
          3. <a href="${baseUrl}my2.jpg" target="_blank">${baseUrl}my2.jpg</a><br><br>
          Если фото открываются по этим ссылкам, обновите страницу.
        `;
      }
    }
    
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
    
    // Обработка наведения на кнопку "Нет"
    noBtn.addEventListener('mouseenter', function() {
      if (noClickCount < 3 && isAllPhotosLoaded) {
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
      if (!isAllPhotosLoaded) {
        alert('Пожалуйста, подождите, пока загрузятся все фото...');
        return;
      }
      
      // Воспроизведение звука
      try {
        if (CONFIG.soundYes) {
          const audio = new Audio(CONFIG.soundYes);
          audio.play().catch(e => console.log("Звук не удалось воспроизвести"));
        }
      } catch(e) {}
      
      // Прячем элементы
      questionEl.style.display = 'none';
      document.querySelector('.buttons').style.display = 'none';
      photoErrorEl.style.display = 'none';
      photoSuccessEl.style.display = 'none';
      debugInfo.style.display = 'none';
      
      // Показываем результат
      resultEl.style.display = 'block';
      
      // Показываем ВАШИ фотографии
      myPhotosEl.style.display = 'flex';
      
      // Меняем заголовок
      girlNameEl.innerHTML = CONFIG.girlName + ' 💘<br>Моя Валентинка!';
      subtitleEl.innerHTML = 'Теперь ты можешь посмотреть на нас вместе! 🥰';
      
      // Создаем много сердечек
      for (let i = 0; i < 50; i++) {
        setTimeout(() => createHeart(), i * 100);
      }
      
      // Конфетти эффект
      createConfetti();
    }
    
    // Функция отказа
    function sayNo() {
      if (!isAllPhotosLoaded) return;
      
      noClickCount++;
      
      if (noClickCount <= noMessages.length) {
        questionEl.textContent = noMessages[noClickCount - 1];
        
        // Увеличиваем кнопку "Да"
        const scale = 1 + (noClickCount * 0.1);
        yesBtn.style.transform = `scale(${scale})`;
        
        // Меняем цвет кнопки "Да"
        const redValue = 255 - (noClickCount * 20);
        const pinkValue = 255 - (noClickCount * 15);
        yesBtn.style.background = `linear-gradient(45deg, #ff${redValue}66, #ff${pinkValue}99)`;
        
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
    
    // Запуск при загрузке страницы
    window.addEventListener('load', function() {
      // Создаем несколько сердечек
      for (let i = 0; i < 5; i++) {
        setTimeout(() => createHeart(), i * 300);
      }
      
      // Загружаем фото
      loadAllPhotos();
      
      // Показываем отладочную информацию
      debugInfo.style.display = 'block';
      
      // Создаем сердечки каждые 500мс
      setInterval(createHeart, 500);
    });
    
    // Открываем ссылки на фото при клике на отладочную информацию
    debugInfo.addEventListener('click', function() {
      const baseUrl = window.location.origin + window.location.pathname.replace(/\/[^\/]*$/, '/');
      window.open(`${baseUrl}${CONFIG.girlPhoto}`, '_blank');
    });
  </script>
</body>
</html>
