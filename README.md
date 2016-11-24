# Субъективный JS

Остросюжетный гайд по языку.

## От автора

Данная книга предназначена для самостоятельного изучения JS как второго (третьего...) языка.
От читателя ожидается базовое понимание Computer Science. Основной акцент сделан на особенности JS,
выделяющие его среди остальных языков, неочевидные и малоочевидные вещи.

Автор текста имеет опыт коммерческого программирования на трёх языках, некоммерческого – на 15+.
Его целью является создание информативного, но захватывающего гайда для "самого себя в прошлом".
Основная идея – изучение по аналогии – дополняется взглядом на язык с разных ракурсов:
парадигм, истории, конкуренции, контр-примеров и поиска истины.

## [Мотивация](./content/0.1.motivation.md)

## [Переводы терминов](./content/0.2.translations.md)

## Вступление

JS часто воспринимается как простой язык и учится как [набор трюков](https://github.com/loverajoel/jstips),
заменяющих реальное знание. – Я знаю JS! – утверждает персонаж, использующий `alert` для отладки...
Несложно встретить и противоположный взгляд, по которому JS – это полностью
сломанный язык, непроходимая PITA. Мнение подкрепляется специально отобранными "ужасающими" примерами
(не встречающимися на практике).

Оба мнения расходятся с реальностью. JavaScript (в редакции ES 2016-2017) – это сравнительно
сложный язык, обладающий огромной грамматикой. Выразительные возможности JavaScript находятся на одном уровне с Python и Ruby.

JavaScript сложно выучить на однообразных задачах, возникающих в коммерческих проектах.
В то же время, значительный процент "знаний" составляют deprecated синтаксические единицы и паттерны.
В повседневной практике следует ограничивать себя отобранным подмножеством языка.

Официальное название спецификации JavaScript: EcmaScript. Разница связана с лицензиями и не представляет
особого интереса. Мы будем использовать термин JS или JavaScript в качестве названия языка и
ES5, ES6, ES2015, ES2016 для ссылок на конкретные версии.

Все версии языка, на данный момент, обладают 100% обратной совместимости.
Ни авторы ES, ни сообщество пока не смогли выработать удовлетворительного механизма удаления фич.
Небольшие исключения типа `"use strict"` можно вынести за скобки.

Ситуацию спасает практически полное отсутствие стандартных библиотек в языке. Да, да – это огромный плюс!
Python сообщество показало всем убедительный контр-пример. "Batteries included", вначале, играет всем на пользу.
Затем, из-за увязки обновления библиотек с выпуском новых версий языка, – превращает всё в археологический музей.
Стандартные пакеты Python забагованы, устарели, разлагаются. Но, вопреки всеобщей ненависти, продолжают использоваться, как "стандартные"...

JS, безусловно, страдает от противоположной крайности, однако появление Node и NPM в корне изменило ситуацию.
Проблем с поиском библиотек в экосистеме практически нет. Вероятно, даже число научных библиотек в JS превысит оное в Python,
в обозримом будущем.

Проблема с "избытком альтернатив" является меньшим злом. Конкуренция – двигатель прогресса, а
культура написания документации в JS сообществе находится на сравнительно высоком уровне
Достаточно сказать, что на титульных страницах документаций нередко можно встретить перечень отличий от "конкурентов".
Положа руку на сердце – о таком уровне большинство программистских сообществ могут лишь мечтать.
Возьмите PHP с его бесчисленными "фреймворками", ничем не отличающимися друг от друга.
Возьмите выдохшийся Java. Возьмите тот же Python. И так далее.

## Как читать эту книгу

Данная книга посвящёна JavaScript и не затрагивает вопросы API (DOM, HTTP, и т.д.). Однако, примеры кода
будут содержать `console.log`, которая не является частью языка. Впрочем, и NodeJS и Браузеры
предоставляют данную функцию и, вероятно, её стандартизация – вопрос времени.
Также, при необходимости показать функцию из сторонней библиотеки, мы будем использовать синтаксис CommonJS.
Окончательная стандартизация ES модулей ожидается в 2017 году, после чего материал будет обновлён.

Желающим запускать примеры предлагается:

* установить [NodeJS](https://nodejs.org/en/) (и редактор, если вы форматировали диск)
* копировать тексты примеров в отдельные файлы
* запускать файлы из консоли командой вида `$ node exampleX.js`

Автор книги стремился сделать ВСЕ примеры максимально простыми и понятными с первого взгляда.
Если вы испытываете сложность с пониманием какого-либо абзаца или примера при последовательном чтении –
открывайте соотв. [Issue](https://github.com/ivan-kleshnin/subjective-js/issues).

## Содержание

### 1. Основы

#### [1.1 Примеры синтаксиса](./content/1.1.syntax-examples.md)

#### [1.2 Инструкции, Декларации, Выражения](./content/1.2.statements-declarations-expressions.md)

#### [1.3 Элементы первого порядка](./content/1.3.first-class-elements.md)

## 2. Система типов

### [2.1 Слабая динамическая типизация](./content/2.1.weak-typing.md)

### [2.2 Примитивы и Объекты](./content/2.2.primitives-and-objects.md)

### [2.3 Проверка типов](./content/2.3.type-checking.md)

### [2.4 Обёрточные классы](./content/2.4.wrapper-classes.md)

### [2.5 Коэрция типов](./content/2.4.type-coercion.md)

### [2.6 Практические правила](./content/2.4.practical-rules.md)

## 3. Переменные и скоупинг

### [3.1 Скоупинг](./content/2.1.scoping.md)

### [3.2 Хойстинг](./content/2.2.hoisting.md)

## 4. Встроенные типы

### [4.1 Undefined и Null](./content/3.1.undefined-and-null.md)

### [4.2 Булеаны](./content/3.2.boolean.md)

### [4.3 Числа](./content/3.3.number.md)

### [4.4 Строки](./content/3.4.string.md)

### [4.5 Записи](./content/3.5.object.md)

### [4.6 Массивы](./content/3.6.array.md)

### [4.7 Даты](./content/3.7.date.md)

### [4.8 Регулярки](./content/3.8.regex.md)

## 5. Прототипная модель (TODO)

## 6. Динамический this (TODO)

## Книги

* [Speaking JavaScript](http://speakingjs.com/es5/index.html)
* [Exploring ES6](http://exploringjs.com/es6/index.html)
* [Exploring ES2016-ES2017](https://leanpub.com/exploring-es2016-es2017/read)
