[imdex.html.html](https://github.com/user-attachments/files/25683603/imdex.html.html)
<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Chibabchich Premium</title>
    <script src="https://telegram.org/js/telegram-web-app.js"></script>
    <style>
        :root { --bg: var(--tg-theme-bg-color); --text: var(--tg-theme-text-color); --hint: var(--tg-theme-hint-color); --button: var(--tg-theme-button-color); }
        body { background: var(--bg); color: var(--text); font-family: 'Segoe UI', sans-serif; margin: 0; padding: 15px; }
        .header { text-align: left; margin-bottom: 20px; }
        .card { background: var(--tg-theme-secondary-bg-color); border-radius: 15px; padding: 15px; margin-bottom: 15px; box-shadow: 0 4px 10px rgba(0,0,0,0.1); border: 1px solid var(--hint); }
        .card img { width: 100%; border-radius: 10px; margin-bottom: 10px; }
        .card h3 { margin: 5px 0; font-size: 18px; }
        .card p { color: var(--hint); font-size: 14px; margin: 5px 0; }
        .btn { background: var(--button); color: white; border: none; width: 100%; padding: 12px; border-radius: 10px; font-weight: bold; margin-top: 10px; }
        .ref-box { background: rgba(0,0,0,0.05); padding: 10px; border-radius: 10px; font-size: 12px; margin-top: 20px; }
    </style>
</head>
<body>
    <div class="header">
        <h2 id="welcome">Привет!</h2>
        <p>Доступные розыгрыши 👇</p>
    </div>

    <div id="contest-list">
        <div class="card">
            <img src="https://via.placeholder.com/300x150" alt="Приз">
            <h3>Розыгрыш #1</h3>
            <p>🎁 Приз: iPhone 15 Pro</p>
            <p>👥 Участников: 124</p>
            <button class="btn" onclick="joinContest(1)">Участвовать</button>
        </div>
    </div>

    <div class="ref-box">
        <b>Твоя реферальная ссылка:</b><br>
        <span id="ref-link">Загрузка...</span>
    </div>

    <script>
        const tg = window.Telegram.WebApp;
        tg.expand();
        document.getElementById("welcome").innerText = Привет, ${tg.initDataUnsafe.user.first_name}!;
        document.getElementById("ref-link").innerText = https://t.me/ТВОЙ_БОТ?start=${tg.initDataUnsafe.user.id};

        function joinContest(id) {
            tg.sendData(join_request_${id}); // Отправляем данные боту
        }
    </script>
</body>
</html>
