**Дедлайн**: 02.02.2025 23:59


Что необходимо сделать: реализовать свою программу/сервис/пакет

## Формат сдачи

Формат сдачи - публичный GitHub репозиторий, содержащий файлы проекта. Структура репозитория зависит от выбранного вами формата проекта

## Пример

### Для формата пакета

```
├── README.md          <- Файл, содержащий информацию об авторе проекта, его суть и примеры использования
├── requirements.txt   <- Файл, содержащий все необходимые зависимости
├── package_name       <- Директория, являющаяся вашим пакетом (имя придумываете сами)
│   ├── __init__.py    <- Инициализационный файл. Подробнее смотри внутри __init__.py в директории package_template
│   ├── module_1.py    <- Один из возможных модулей вашей программы. Название придумайте сами
|   ├── exceptions.py  <- Модуль, содержащий написанные вами исключения
|   ├── decorators.py  <- Модуль, содержащий написанные вами декоратора (если они нужны).
|   ...                   по аналогии, модули, сильно подвязанные под структуру вашего проекта, кладите их также в основную директорию проекта.
|   ├── ...
|   ├── utils          <- Не является обязательной директорией, но в случае наличия модулей ОБЩЕГО назначения, 
|   ...                   т.е. таких, которые могли бы существовать и в другом проекте, их можно закинуть сюда
|       ├── __init__.py   <- Чтобы сделать полноценным пакетом
|       ├── validation.py <- Модуль для валидации данных (если нужно)
|       ├── helpers.py    <- Общие вспомогательные функции (если нужно)
|       ├── ...
```

**Примечание**:

Если вам хочется более глубокую структуру, я не против.
Пример более глубокой структуры (специально накидал много всего - вероятно, излишнего в общем случае) для случая выше:

```
├── README.md
├── requirements.txt
├── package_name
│   ├── __init__.py             <- Инициализация основного пакета
│   ├── module_1.py             <- Основной модуль 1
│   ├── module_2.py             <- Основной модуль 2
│   ├── exceptions.py           <- Модуль, содержащий написанные вами исключения
│   ├── decorators.py           <- Модуль, содержащий написанные вами декораторы
│   ├── ...
│   ├── utils                   <- Подпакет для утилит
│   │   ├── __init__.py         <- Делает utils субпакетом
│   │   ├── file_utils.py       <- Функции для работы с файлами
│   │   ├── validation.py       <- Утилиты для проверки данных
│   │   ├── logger.py           <- Настройка логирования
│   │   ├── helpers.py          <- Общие вспомогательные функции
│   │   ├── ...
│   ├── core                    <- Подпакет, содержащий основные элементы логики
│   │   ├── __init__.py         <- Делает core субпакетом
│   │   ├── processing.py       <- Обработка данных
│   │   ├── transformations.py  <- Трансформации и преобразования
│   │   ├── ...
│   ├── features                <- Подпакет для специфичных функций или особенностей
│   │   ├── __init__.py         <- Делает features субпакетом
│   │   ├── feature_1.py        <- Особенность 1
│   │   ├── feature_2.py        <- Особенность 2
│   │   ├── ...
│   └── subpackage_name         <- Пример подпакета (расширяется как нужно)
│       ├── __init__.py
│       ├── sub_module_1.py
│       ├── sub_module_2.py
│   │   ├── ...

```


## Критерии оценивания

### Максимум можно набрать 14 баллов

__Общие критерии оценивания__:

- Отсутствие плагиата (о наличии любых заимствований кода вы **должны** написать в комментариях к этому коду; если вы брали код из интернета/работы другого человека/генерировали нейросетью, укажите источник). Если вы решите выдавать чужие решения за свои, я оставляю за собой право снижать ваш балл сколь угодно сильно


**Сдача вовремя (1 балл)**
- Я поставлю вам один балл за сдачу проекта до дедлайна


**Внутренние особенности кода (4 балла)**
- Ваш код работает без существенных ошибок **(1 балл)**
- В коде присутствуют комментарии **(1 балл)**
- Все функции, кроме функции main в main.py, имеют док-строку **(1 балл)**
- Все `.py` файлы, кроме main.py (или run.py, или app.py, или другое название главного файла, если таковой имеется), имеют док-строку **(1 балл)**

**Оформление репозитория (3 балла)**
- К проекту приложен файл `README.md`, в котором вы подробно описали:
	- Кто автор проекта (ФИО, ису)
	- Про что проект (короткое описание)
	- Описали примеры использования (что пользователь должен сделать, чтобы воспроизвести минимальный функционал, задуманный вами).

**Внутренние особенности проекта** (6 баллов)

- Есть использование хотя бы двух модулей из стандартной библиотеки Python ИЛИ хотя бы одного модуля из стандартной библиотеки и одного модуля/пакета, доступного из PyPI (т.е. можно установить с помощью утилиты pip) (2 балла)\
**Важно**: если вы решили использовать сторонние модули, которые установили с помощью pip, ваш проект **должен** содержать файл requirements.txt 
- Есть хотя бы один написанный вами модуль (2 балла). Не считаюся:
	- `main.py` 
	- `__init__.py` тоже не считается, если вы выбрали формат пакета) 
- Есть хотя бы один написанный вами класс с хотя бы тремя методами (конструктор считается, если вы его реализуете) (2 балла)

**Штрафной критерий**
- В проекте нет однобуквенных переменных, кроме i/j/k (-1 балл за наличие), только если их использование не является оправданным контекстной понятностью

**Субъективная оценка сложности проекта** (до 2 баллов) - бонусные баллы
- 0 - если проект является чем-то, что почти полностью заимствовано из других источников И/ИЛИ по объёму является чем-то относительно маленьким (условно < 100 строк)
- 1 - если проект не содержит существенных заимствований из других источников, НО является чем-то относительно маленьким (условно < 100 строк)
- 2 - если проект не содержит существенных заимствований из других источников И не является чем-то относительно малеьникм (условно > 100 строк)
