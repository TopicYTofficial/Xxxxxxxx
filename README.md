<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Phoenix CM Bot - Полное руководство</title>
    <style>
        body {
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
            line-height: 1.6;
            color: #333;
            max-width: 800px;
            margin: 0 auto;
            padding: 20px;
            background-color: #f8f9fa;
        }
        h1, h2, h3 {
            color: #e67e22;
        }
        h1 {
            text-align: center;
            border-bottom: 3px solid #e67e22;
            padding-bottom: 10px;
        }
        h2 {
            background-color: #fef5e7;
            padding: 10px;
            border-left: 4px solid #e67e22;
            margin-top: 30px;
        }
        .toc {
            background-color: #fff;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
            margin-bottom: 30px;
        }
        .toc a {
            color: #e67e22;
            text-decoration: none;
            display: block;
            padding: 5px 0;
        }
        .toc a:hover {
            text-decoration: underline;
        }
        .command {
            background-color: #fff;
            padding: 15px;
            border-radius: 5px;
            margin-bottom: 15px;
            box-shadow: 0 1px 3px rgba(0,0,0,0.1);
        }
        .command-code {
            background-color: #f8f9fa;
            padding: 10px;
            border-radius: 3px;
            font-family: monospace;
            margin: 10px 0;
            border-left: 3px solid #e67e22;
        }
        .note {
            background-color: #e8f4fd;
            padding: 10px;
            border-radius: 5px;
            border-left: 4px solid #3498db;
            margin: 15px 0;
        }
        .warning {
            background-color: #fde8e8;
            padding: 10px;
            border-radius: 5px;
            border-left: 4px solid #e74c3c;
            margin: 15px 0;
        }
        footer {
            text-align: center;
            margin-top: 50px;
            padding: 20px;
            border-top: 1px solid #ddd;
            color: #7f8c8d;
            font-size: 0.9em;
        }
    </style>
</head>
<body>
    <h1>🕊️ Phoenix CM Bot</h1>
    <p><strong>Многофункциональный бот для управления чатом и развлечений</strong></p>
    <p>Phoenix — это ваш надежный помощник и хранитель порядка в Telegram-чате. Он сочетает в себе мощные инструменты модерации, экономическую систему с валютами, систему репутации, ранги, игры и многое другое.</p>

    <div class="toc">
        <h3>📑 Оглавление</h3>
        <a href="#economy">💰 Экономика</a>
        <a href="#moderation">👑 Модерация</a>
        <a href="#profile">📝 Профиль и анкета</a>
        <a href="#ranks">🎖️ Система рангов</a>
        <a href="#games">🎮 Игры и развлечения</a>
        <a href="#settings">⚙️ Настройки чата</a>
        <a href="#info">ℹ️ Информационные команды</a>
    </div>

    <h2 id="economy">💰 Экономика</h2>
    <p>Внутриигровая экономика с двумя валютами: <strong>Жар коины (🪙)</strong> и <strong>Слезы феникса (💎)</strong>.</p>

    <div class="command">
        <h3>/balance или /bal</h3>
        <p>Показывает ваш текущий баланс и ранг.</p>
        <div class="command-code">/balance</div>
    </div>

    <div class="command">
        <h3>Ферма</h3>
        <p>Собрать урожай жар коинов. Доступно раз в 4 часа.</p>
        <div class="command-code">ферма</div>
    </div>

    <div class="command">
        <h3>Мешок</h3>
        <p>Показать содержимое вашего инвентаря.</p>
        <div class="command-code">мешок</div>
    </div>

    <div class="command">
        <h3>+Мешок / -Мешок</h3>
        <p>Показать или скрыть мешок при запуске команды /start.</p>
        <div class="command-code">+мешок</div>
        <div class="command-code">-мешок</div>
    </div>

    <div class="command">
        <h3>/roulette [ставка] [тип]</h3>
        <p>Сыграть в рулетку. Типы ставок: число (0-36), <em>красное</em>, <em>черное</em>.</p>
        <div class="command-code">/roulette 50 красное</div>
        <div class="command-code">/roulette 10 15</div>
    </div>

    <div class="command">
        <h3>/russianroulette [ставка]</h3>
        <p>Сыграть в русскую рулетку. Шанс проиграть 1 к 6.</p>
        <div class="command-code">/russianroulette 100</div>
    </div>

    <h2 id="moderation">👑 Модерация</h2>
    <p class="note">Команды модерации доступны только администраторам чата.</p>

    <div class="command">
        <h3>Мут [время] [причина]</h3>
        <p>Замутить пользователя (в ответ на его сообщение). Время можно указывать в минутах, часах, днях.</p>
        <div class="command-code">мут 60 мин спам</div>
        <div class="command-code">мут 1 день оскорбления</div>
    </div>

    <div class="command">
        <h3>Размут</h3>
        <p>Размутить пользователя (в ответ на его сообщение).</p>
        <div class="command-code">размут</div>
    </div>

    <div class="command">
        <h3>Варн [причина]</h3>
        <p>Выдать предупреждение пользователю (в ответ на его сообщение).</p>
        <div class="command-code">варн нарушение правил</div>
    </div>

    <div class="command">
        <h3>-Варн</h3>
        <p>Снять предупреждение с пользователя (в ответ на его сообщение).</p>
        <div class="command-code">-варн</div>
    </div>

    <div class="command">
        <h3>Кик [причина]</h3>
        <p>Исключить пользователя из чата (в ответ на его сообщение).</p>
        <div class="command-code">кик спам</div>
    </div>

    <div class="note">
        <p><strong>Система предупреждений:</strong> При достижении максимального лимита варнов (по умолчанию 3) пользователь автоматически получает мут на 24 часа.</p>
    </div>

    <h2 id="profile">📝 Профиль и анкета</h2>

    <div class="command">
        <h3>+Ник [текст]</h3>
        <p>Установить свой никнейм в боте.</p>
        <div class="command-code">+ник Крутой Феникс</div>
    </div>

    <div class="command">
        <h3>+Анкета [текст]</h3>
        <p>Заполнить текст своей анкеты.</p>
        <div class="command-code">+анкета Люблю программирование и печеньки</div>
    </div>

    <div class="command">
        <h3>+Анкета / -Анкета</h3>
        <p>Сделать анкету видимой для других или скрыть ее.</p>
        <div class="command-code">+анкета</div>
        <div class="command-code">-анкета</div>
    </div>

    <div class="command">
        <h3>Анкета</h3>
        <p>Посмотреть свою анкету или анкету пользователя (в ответ на сообщение).</p>
        <div class="command-code">анкета</div>
    </div>

    <h2 id="ranks">🎖️ Система рангов</h2>
    <p>Пользователи имеют ранг от 0 до 5. Администраторы могут повышать или понижать ранги других пользователей, но не могут воздействовать на тех, у кого ранг равен или выше.</p>
    <ul>
        <li><strong>0:</strong> Участник</li>
        <li><strong>1:</strong> Помощник</li>
        <li><strong>2:</strong> Модератор</li>
        <li><strong>3:</strong> Администратор</li>
        <li><strong>4:</strong> Старший администратор</li>
        <li><strong>5:</strong> Создатель</li>
    </ul>

    <div class="command">
        <h3>Повысить [количество]</h3>
        <p>Повысить ранг пользователя (в ответ на сообщение).</p>
        <div class="command-code">повысить</div>
        <div class="command-code">повысить 2</div>
    </div>

    <div class="command">
        <h3>Понизить [количество]</h3>
        <p>Понизить ранг пользователя (в ответ на сообщение).</p>
        <div class="command-code">понизить</div>
        <div class="command-code">понизить 1</div>
    </div>

    <div class="command">
        <h3>!Востановить создателя</h3>
        <p><strong>Только для создателя чата.</strong> Восстанавливает ранг создателя до максимального (5), если он был понижен.</p>
        <div class="command-code">!востановить создателя</div>
    </div>

    <h2 id="games">🎮 Игры и развлечения</h2>

    <div class="command">
        <h3>Феникс шипперим [@user1] и [@user2]</h3>
        <p>Проверить совместимость двух пользователей.</p>
        <div class="command-code">Феникс шипперим @username1 и @username2</div>
    </div>

    <div class="command">
        <h3>Феникс расстрелять [@user]</h3>
        <p>"Расстрелять" пользователя в шутку.</p>
        <div class="command-code">Феникс расстрелять @username</div>
    </div>

    <div class="command">
        <h3>Феникс кто [вопрос с "или"]</h3>
        <p>Случайный выбор из предложенных вариантов.</p>
        <div class="command-code">Феникс кто пойти гулять или сидеть дома</div>
    </div>

    <div class="command">
        <h3>Феникс инфа [вопрос]</h3>
        <p>Узнать вероятность какого-либо события.</p>
        <div class="command-code">Феникс инфа я сдам этот проект вовремя</div>
    </div>

    <h2 id="settings">⚙️ Настройки чата</h2>
    <p class="note">Настройки доступны администраторам чата.</p>

    <div class="command">
        <h3>+Правила [текст]</h3>
        <p>Установить правила чата.</p>
        <div class="command-code">+правила 1. Не спамить 2. Уважать друг друга</div>
    </div>

    <div class="command">
        <h3>+Приветствие [текст]</h3>
        <p>Установить приветственное сообщение для новых участников.</p>
        <div class="command-code">+приветствие Добро пожаловать в наш чат! Ознакомься с правилами.</div>
    </div>

    <p>Бот также имеет автоматические системы:</p>
    <ul>
        <li><strong>Антиспам:</strong> Автоматический мут за слишком частые сообщения.</li>
        <li><strong>Антимат:</strong> Автоматическое удаление сообщений с нецензурной лексикой.</li>
        <li><strong>Антикапс:</strong> Автоматическое удаление сообщений, написанных CAPS LOCK'ом.</li>
        <li><strong>Антиссылки:</strong> Автоматическое удаление сообщений со ссылками (если включено).</li>
    </ul>

    <h2 id="info">ℹ️ Информационные команды</h2>

    <div class="command">
        <h3>/start</h3>
        <p>Главная команда для начала работы с ботом. Показывает вашу анкету и баланс (если они видимы).</p>
        <div class="command-code">/start</div>
    </div>

    <div class="command">
        <h3>/help</h3>
        <p>Показывает это руководство прямо в Telegram.</p>
        <div class="command-code">/help</div>
    </div>

    <div class="command">
        <h3>Кто админ</h3>
        <p>Показывает список текущих администраторов чата.</p>
        <div class="command-code">кто админ</div>
    </div>

    <footer>
        <p>🕊️ Руководство по использованию бота Phoenix CM</p>
        <p>Для связи с разработчиком: <a href="https://t.me/your_username">@your_username</a></p>
    </footer>
</body>
</html>
