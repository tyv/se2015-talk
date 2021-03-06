## N
Привет! Меня зовут Юра Ткаченко
Я занимаюсь фронтенд разроботкой уже больше 12 лет.

И признаться, до сих пор засиживаюсь по ночам или выходным,
чтобы не потерять темп.

## N
Потому что в мире фронтенда ты или бежишь вперед,
или остаешься за бортом.

Иногда начинает казаться, что все под контролем и можно выдохнуть,
но это ошибка — и я попробую рассказать почему.

## N
Мы все,
ну покрайней мере такие мамонты как я,
помним каким был фронтенд.

## Каким был JavaScript
Таким.

Снежинки — вот что он делал.

## Каким был CSS
СSS не было вообще, все стили писали атрибутами элементов.

### N
В начале 2000-х была волна "разделяй и властвуй".

Когда все призывали использовать CSS и отделять
представление от контента.

Появились поплуряные проекты про CSS.
Браузеры соревнуются кто из них лучше поддерживает CSS3.

## N
Когда с CSS все начало выравниваться и
верстать таблицами стало уж совсем моветон,

В игру всупает javascript
как единственный **дейтсвительно работающий**
язык программирования, доступный на клиенте.

## N
Наступает переломный момент для индустрии и
фронтенд становится профессией.
Количество фронтенда-разработчиков на проекте
сравнивается или превышает количество бекенда.

## N
И, главное, о чем мы будем говорить —
развивается инфраструктура.

## N
Ладно, хватит трясти песком, давайте подобьем
что у нас сейчас есть.

Мы пережили ряд толчков,
которые сильно повлияли на индустрию:

* поддержка CSS3
* jQuery и куча плагинов
* повяляется V8 и идет гонка js-движков
* node.js
* MVC-фреймворки
* и сейчас виртуальный дом и React

## N
Сейчас события, которые обычно занимали
несколько лет проходят за несколько месяцев

Что очевидно усложняет архитектуру проекта.

## N
Сегодня — тренд отказа от jQuery.
Самый крутой пример, умешается в 1 твит.

## N
Мы очень быстро пережили (я надеюсь пережили)
бум MVC фреймворков: knockout, backbone, angular..

Теперь MVC не очень модно и все любят Flux.

## Вымирает профессия верстальщика
Я — верстальщик.
Я очень много занимался CSS и в мир JS пришел поздно.
Но нужно признать что CSS теперь вообще not a big deal.

Он занимает ровно свою нишу — способ разукрасить страницу.

Да CSS богат и это мощный способ оформлять страницу
С ним можно вытворять многое, что по инерции делается на JS.

Но тем не менее CSS больше не магия, и работает он хорошо везде.

## N
Все сейчас модульно.
Некоторые давно это придумали,
остальной мир только дошел до этого.

У нас есть куча инструментов:
сборщики и менеджеры пакетов

js и css самые поплуряные языки на github

## N

Итак, 10 лет назад у нас был только один CSS файл и
js-файл со снежинками.

Сегодня у нас огромная инфраструктура.

## N
Казалось бы — что может пойти не так?
Ответ — примерно всё.

## N
Каждый новый проект начинается с нуля,
с новой инфраструктурой.

Посмотрите на списки.
Разница между стеками — пол года!
Ни капли стабильности.

### N

Опенсорс — отдельная история.

Разработчики часто бросают свои проекты.
Очень больно, если вы использовали такую библиотеку.

### N

Например, Stylus бы окончательно умер,
если бы Рома Комаров и Миша Корепанов,
которые развивают проект.

#### N
Сейчас на github 1500 deprecated javascript репозиториев.
Сколько вынужденных рефаткорингов это вызвало?

#### N
Вы вынуждены обновляться постоянно
Новые библиотеки работают только в новом окружении,
если вы все еще на node.js 0.10 — поздравляю, у вас проблемы.

#### N
Нескольо примеров, пока я пишу этот доклад,
Дэн абрамов обновляет Реакт Роутер и
делает его несвместимым.

#### N
Выходит Node.js 4.0.0 и ломается сборка sass

#### N
Ломается популярный фреймворк soket.io

### Что еще сломается?

#### N
Все знают эту картинку.
А у вас деплой :)
Недоступность github или npm — большая проблема.

#### будут конфликты библиотек
Я встречал переопределенный Array.prototype.filter библиотекой

Часто можно найти две похожие библиотеки,
одна старая, другая новая.

Это мы называем стабильность.

##### разные версии опреционок или node.js в разработке и на сервере сборки или на тестинге/продакшене

##### N
Обновление одной библиотеки
всегда тянет за собой кучу кофликтов.

Прийдется обновлять много всего сразу.

##### N
Особенно круто когда это все приезжает на клиент.
Вы может быть тоже встречали две версии jQuery на проекте?
Или lodash и underscore?

## N
Все что я перечислил (а это далеко не все проблемы) —
так развивается и растет организм фронтенд-разработки

Сейчас у него юношеский период,
он пробует алкоголь и наркотики,
его музыкальные вкусы меняются пару раз в день,
будущее для него радука по которой бегают розовые пони.

Но это мы растем,
**так и должно быть**.

## Но очевидный вопрос «Что делать?»
Конечно готового решения нет.

Есть несколько хороших практик,
которые помогут избежать головной боли
или хотя бы начать реагировать быстро.

### Из обязательных

1. Комитеть node_modules и bower_components в репозиторий.
Не надейтесь что npm и github будут всегда доступны.

2. Выктились в продакшн с ошибками,
должна быть под рукой предыдущая сборка,
не тег в репозитории, а готовый собранный пакет,
чтобы вы могли в любой момент откатиться на предудщую версию.

3. Jenkins или TeamCity — настроить сборку на каждый пуш
в релизную ветку и вы будете уверены, что не сломали сборку.
Автодеплой в тестинг поможет вовремя находить ошибки.

### Что желательно сделать
1. Обновлять используемые библиотеки. Это болезненно, так как требует хорошоего покрытия тестами.
2. Вычищать мертвеющие библиотеки: еще более тяжело, так как ваш проект может быть полностью построен на такой. Но не делать этого — будет еще хуже.
3. Не стоит использовать 2 разных менеджера зависимостей.
4. Вводите практитки в компании: code review и code style — две головы лучше.

### Для  повышения стабильности
1. npm-shrinkwrap: зафиксирует версии пакетов по всему дереву зависимостей: убедитесь, что у вас все работает как надо, сделайте npm-shrinkwrap и добавьте сгенерированный npm-shrinkwrap.json в ваше приложение. Далее при npm i вы будете использовать конкртеное дерево пакетов
2. Монитрьте window.performance метрики и обшибки на клиенте, чтобы понимать что происходит и настройте оповещения если все плохо, для этого есть инструменты такие как New Relic или Sentry.
3. Автоматическое тестирование деградации скорости. Это сложно, но возможно.
4. Тестируйте деплой новой версии на маленький % пользователей.

### N
Это все равно не даст вам 100% гарантии.
Но эти правила, получены "потом и кровью" и
Чем больше проект, тем больше этих правил нужно использовать.

## Не бойтесь изобретать
Когда вы сталкивайтесь с проблемой и не находите готово решения —
делайте свое и делитесь с миром,
уверен, что найдутся многие, кто скажут вам спасибо.

## N
А сейчас за то, что терпели меня, говорю спасибо я —
вы прекрасная аудиторя.

Вопросы?

