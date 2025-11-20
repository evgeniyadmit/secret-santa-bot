🎄 **Secret Santa Telegram Bot** (The English description is located below this one)

Ссылка на бот в самом Telegram: https://t.me/santasecretpresentsbot



***Универсальный Telegram-бот для проведения игры «Тайный Санта» в любых компаниях, командах, университетах или семейных чатах.***



Бот позволяет провести честный и автоматический розыгрыш подарков:

&nbsp;• никто не получает сам себя

&nbsp;• каждый человек получает ровно одного получателя

&nbsp;• организатор задаёт список участников

&nbsp;• участники сами вводят свои имена

&nbsp;• бот учитывает разные варианты написания (ё/е, регистр, пробелы)

&nbsp;• результат стабилен: один участник → один человек

Бот поддерживает **много игр одновременно через game code**, а не "одна игра на один запуск".

Бот написан на Python + aiogram 3 и готов к использованию на Replit, VDS или любом Python-сервере.





✨ **Возможности**



👑 *Для организатора:*



&nbsp;• команда /newgame создаёт новую игру и выдаёт код игры (например, A7F9), который нужно отправить участникам.

&nbsp;• бот ожидает список участников

&nbsp;• имена принимаются построчно:



Юлия Павликова

Евгения Дмитриева

Елена Мещерякова


**Код игры используется участниками, чтобы присоединиться именно к вашей игре.**


&nbsp;• бот очищает список, удаляет дубликаты

&nbsp;• автоматически создаёт честное распределение «кто кому дарит»



🎁 *Для участника:*



&nbsp;• пишет /start

&nbsp;**вводит код игры от организатора**

&nbsp;• вводит своё имя и фамилию

&nbsp;• получает кнопку «🎁 Получить имя»

&nbsp;• бот сообщает, кому он дарит подарок

&nbsp;• нажимать кнопку можно сколько угодно — результат фиксированный





🧠 **Умная обработка имён**



*Бот нормализует текст:*



&nbsp;• ё = е

&nbsp;• регистр не важен (анГЕлина киСЕЛЕва)

&nbsp;• лишние пробелы не мешают

&nbsp;• принимает русские имена в любом виде



*Пример вводов, которые считаются одним и тем же человеком:*



Ангелина Киселева

ангелина киселЕва

АНГЕЛИНА    КИСЕЛЁВА



🏗 **Архитектура (в двух словах)**



&nbsp;• Game — объект текущей игры (список участников, раздача пар, сессии игроков)

&nbsp;• make\_derangement() — создание перестановки без самопар

&nbsp;• normalize\_name() — умная нормализация имени

&nbsp;• aiogram Router — обработка команд

&nbsp;• один запуск бота = одна игра (как обычный Secret Santa)


**Бот поддерживает неограниченное количество игр одновременно: каждая игра имеет свой game_id (короткий код), а участники привязаны к нужной игре по этому коду.**


🎮 **Команды**



Команда Описание

/start Начать участие

/help Инструкция

/newgame Создать новую игру (только организатор)

/reset Полный сброс игры





🚀 **Как запустить локально**



*1. Установите зависимости*



pip install aiogram==3.4.1 python-dotenv aiohttp aiofiles



*2. Создайте файл .env:*



BOT\_TOKEN=ВАШ\_ТОКЕН



*3. Запустите бота:*



python main.py





📦 **Список файлов репозитория**



main.py

pyproject.toml

.env.example

.gitignore

README.md



.env НЕ публикуется — токен хранится локально.





❤️ **Автор**



Бот разработан для массового использования: корпоративы, школьные группы, университеты, семейные чаты и любые события, где нужен честный и красивый Secret Santa.

Ссылка на бот: https://t.me/santasecretpresentsbot

*Для связи с создателем: @angel\_eugeniya (TELEGRAM)*





❄ Приятного использования!



**ENGLISH:**



🎄 **Secret Santa Telegram Bot**

Bot link: https://t.me/santasecretpresentsbot

**An universal Telegram bot for running Secret Santa games for companies, teams, school groups, university classrooms, communities, or families.**

The bot automates the entire process:

✔ nobody gets themselves
✔ each participant receives exactly one recipient
✔ organizer sends one message with the participants list
✔ participants join via game code
✔ bot handles name normalization (ё/e, case, spaces)
✔ each user always receives the same fixed recipient
✔ supports multiple games simultaneously

Built with Python + aiogram 3, ready to run on Replit, VDS, Docker, or any Python server.



✨ **Features**

👑 *For organizers*
 • /newgame — create a new game and receive a game code (e.g. A7F9)
 • send a single message with the full participants list
 • names must be one per line:


Yulia Pavlikova
Evgenia Dmitrieva
Elena Meshcheryakova


 • the bot:
 • cleans the list
 • removes duplicates
 • supports 2+ participants
 • generates a fair derangement (nobody gets themselves)

**After that, the organizer shares the bot link + game code with participants.**


🎁 *For participants*
 • send /start
 • enter the game code from the organizer (e.g. A7F9)
 • enter your first and last name
 • press 🎁 Get recipient
 • the bot tells you who you should give a gift to
 • you can press the button as many times as you want — the result never changes


🧠 **Smart name processing**

The bot normalizes names:
 • ё = е
 • case-insensitive
 • multiple spaces → one
 • accepts Russian names in any reasonable form

All of the following are treated as the same person:

Ангелина Киселева
ангелина киселева
АНГЕЛИНА КИСЕЛЁВА


🏗 **Architecture (explained simply)**

 • Game — a single Secret Santa game tied to a game code
 • games[code] — storage of all active games
 • make_derangement() — generates a fair assignment (nobody gets themselves)
 • normalize_name() — normalizes user input
 • aiogram Router — processes commands and messages
 • The bot supports unlimited parallel games — each company has its own code.



🎮 **Commands**

*Command Description*
/start Join a game; enter game code
/help Full instructions
/newgame Create a new game (organizer only)
/reset Reset the organizer’s active game



🚀 **How to run locally**

*1. Install dependencies*

pip install aiogram==3.4.1 python-dotenv aiohttp aiofiles

*2. Create a .env file*

BOT_TOKEN=YOUR_TELEGRAM_BOT_TOKEN

*3. Run the bot*

python main.py



📦 **Repository structure**

main.py
pyproject.toml
.env.example
.gitignore
README.md

 • main.py — bot logic
 • .env.example — template for environment variables
 • .env — NOT included; stores your real token
 • .gitignore — prevents committing secrets



❤️ **Author**

This bot was created for public, large-scale usage: companies, school groups, university teams, family chats, and any events where Secret Santa is needed.

Bot link: https://t.me/santasecretpresentsbot

*Contact: @angel_eugeniya (Telegram)*

❄️ Enjoy your Secret Santa experience!





