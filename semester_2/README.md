**Дедлайн**: 02.02.2025 23:59

Что необходимо сделать: реализовать своего тг-бота ИЛИ реализовать мини-исследование данных

## Формат сдачи

Формат сдачи - публичный GitHub репозиторий, содержащий файлы проекта. Структура репозитория зависит от выбранного формата проекта.

## Возможные варианты проектов:

### 1. Исследование данных (максимум 10 баллов)

Репозиторий должен иметь следующий формат (минимум):

```
├── README.md <- Файл с описанием проекта
├── requirements.txt <- Список зависимостей
|── report.jpynb <- отчет о проделанной работе (об этом ниже)
|── scripts <- все ваши `.py` скрипты лежат здесь
|  |──...
├── data
|  |──... <- добытые вами данные
└── ...
```

Создайте проект, покрывающий следующие этапы (каждый из которых должен быть отражён в вашем `report.ipynb` ноутбуке):

#### 1. Сбор данных с веб-сайтов (веб-скрэппинг) (4 балла)
На данном этапе вам необходимо собрать данные с любого источника, не предоставляющего их в готовом формате (например, json, csv, xlsx). 
- Используйте инструменты Python: `requests`, `BeautifulSoup`, `scrapy`, `selenium` или другие подходящие библиотеки.
- **Примечание:** Если вы используете готовый датасет, баллы за данный этап не начисляются.

#### 2. Очистка и обработка данных (4 балла)
На этом этапе вам нужно провести следующие шаги:
- Устранить пропуски и аномалии в данных.
- Привести данные к удобному для анализа виду (например, pandas DataFrame).
- Выполнить минимальный разведывательный анализ данных (EDA), включающий:
  - Статистические описания.
  - Оценку количества пропусков, выбросов и уникальных значений.
  - Пример структуры данных (первые несколько строк, `.head()`).

#### 3. Анализ и визуализация данных (4 балла)
Этот этап предполагает выполнение основного анализа и создание визуализаций:
- Выполните основные аналитические шаги (например, выявите тренды, закономерности, корреляции).
- Создайте как минимум 3 качественные визуализации (например, графики на основе `matplotlib`, `seaborn`, `plotly`).
- Визуализации должны быть оформлены с подписями, заголовками и легендами (где это необходимо).

#### 4. Заключение и выводы (2 балла)
- Сформулируйте ключевые выводы по результатам анализа.
- Обсудите, что удалось обнаружить и какие действия можно предпринять на основе результатов.

---

### 2. Telegram-бот (максимум 10 баллов)

Репозиторий должен иметь следующий формат (пример):

```
├── README.md          <- Файл с описанием проекта
├── requirements.txt   <- Список зависимостей
├── bot.py             <- Основной файл с реализацией бота
├── modules            <- Пакет с вспомогательными модулями
│   ├── __init__.py
│   ├── handlers.py    <- Обработчики команд и сообщений
│   ├── utils.py       <- Утилиты, например, для обработки данных
│   └── ...
└── ...
```


#### Требования к боту:
- Реализация функционала хотя бы для 3 команд. Например:
  - `/start` — приветственное сообщение с описанием возможностей бота.
  - `/help` — справка по доступным командам.
  - `/custom` — пользовательская команда, реализующая уникальную логику (на ваш выбор).
- Возможность обработки сообщений от пользователей (например, текстовых или медиафайлов).
- Использование хотя бы одной сторонней библиотеки, кроме `python-telegram-bot` (например, для обработки данных, получения информации с веб-сайтов, работы с API).
- Логирование действий бота (например, запись входящих сообщений в консоль или файл).

---

Критерии оценивания:

#### 1. Функциональность бота (4 балла)  
На этом этапе ваш бот должен выполнять основные функции:  
- Реализуйте минимум **3 команды**, каждая из которых выполняет полезное действие.  
- Бот должен корректно обрабатывать ввод пользователя и выдавать понятные ответы или выполнять заданные операции.  
- Реализуйте обработку ошибок (например, на случай, если пользователь ввёл неверную команду).  
- Примеры команд:
  - `/start` — приветствие и объяснение, что делает бот.  
  - `/help` — информация о доступных командах.  
  - Любая кастомная команда, связанная с тематикой вашего проекта.  

#### 2. Интеграция внешних данных или API (4 балла)  
- Бот должен работать с внешними данными или API.  
- Примеры:
  - Получение данных о погоде (например, через API OpenWeatherMap).  
  - Сбор новостей, котировок, курсов валют и т.п.  
  - Любая другая полезная информация, полученная из внешнего источника.  
- Реализуйте **минимум 2 сценария**, в которых бот использует эти данные (например, две разные кнопки/команды, использование которых ведёт к использование данных из внешних источников)

#### 3. Заключение и демонстрация (2 балла)  
- Подготовьте README.md, в котором описаны:  
  - Основная идея бота.  
  - Инструкция по запуску.  
  - Список функционала.  
- Приложите демонстрацию работы бота (например, GIF, скриншоты или ссылку на тестовую версию).

---

## Важно для обоих форматов

В корне вашего репозитория должен присутствовать `README.md` файл, в котором указаны:
- Ваши ФИО
- Номер ИСУ
