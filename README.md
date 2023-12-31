# <a name="head" />qa-portfolio

В портфолио собраны проекты, выполненные во время обучения по специальности Инженер по тестированию в Яндекс.Практикуме.

### [Проектирование тестов](#test-design)<br>

        Тест-анализ | Ассоциативные карты | Блок-схемы

        Тест-дизайн | Классы эквивалентности | Граничные значения
        
        Тестовая документация | Чек-листы | Тест-кейсы

### [Тестирование веб-приложений](#test-web)<br>

        Пользовательский интерфейс | Формы | DevTools | Charles
        
        Таблицы принятия решений | Парное тестирование | Баг-репорты

### [Тестирование мобильных приложений](#test-api)<br>

        Матрица устройств | Эмуляторы | Android Studio

### [Тестирование API](#test-api)<br>

        REST API | JSON | Postman

### [Тестирование баз данных  ](#test-bd)<br>

        Консоль | SQL | PostgreSQL

        
### [Основы автоматизации тестирования ](#test-avto)<br>

        JavaScript | NodeJS | Puppeteer
        
## <a name="test-design" />Проектирование тестов
<details>
<summary>Проект №1</summary>
Зданаие 1 

Тест-анализ: диаграмма связей
Сначала нужно провести тест-анализ. Изучи требования к Яндекс Маршрутам, структурируй всю информацию и представь её в графическом виде — в формате mindmap. Так ты поймёшь, все ли требования на месте и нет ли в них серых зон. 
<details>
<summary>Требования к сервису Яндекс.Маршруты</summary>
 https://docs.google.com/document/d/1QfoY3LzfQUWdg8WC0XpjA49EyKZBbLCcsKteGutfQaM/edit?usp=sharing
</details>

Решение 1

Ассоциативная карта

https://drive.google.com/file/d/1ZEqVmh9R3b15l7QqtCOczf1H2LLw6Wv_/view?usp=sharing

Задание 2

Тест-дизайн: классы эквивалентности
Настало время тест-дизайна. Подготовить классы эквивалентности и тестовые значения для полей «Время начала поездки», «Откуда» и «Куда».

Решение 2

1 лист в таблице


https://docs.google.com/spreadsheets/d/18092eiIfdvr_nGDBCNHG1hYMR94TtexubJqN4vzytbE/edit#gid=1058266973

Задание 3

Повторный тест-анализ: блок-схема
Выбери только один вид транспорта для тестирования: собственный автомобиль, каршеринг или такси. Подготовь для него блок-схему по заданию ниже. Остальные виды транспорта Саша возьмёт на себя.

<details>
<summary>Подробности</summary>
Блок-схема должна иллюстрировать, как скорость собственного автомобиля, или каршеринга, или такси зависит от времени суток. Например, в интервале с 00:01 до 08:00 скорость такси — 50 км/ч, в следующем интервале — 35 км/ч.
  
Чтобы узнать интервалы и значения скорости, проведи повторный тест-анализ. То есть проанализируй те пункты требований, в которых описана логика расчёта времени и стоимости поездки только на выбранном транспорте. Например, вот одна из возможных таблиц — для такси:

![Интерфейс](https://code.s3.yandex.net/qa/schemes/Sprint_4_2.png)



Из элементов в шаблоне собери блок-схему. Чтобы открыть шаблон, используй сервис draw.io. Блок-схему сохрани в формате изображения и прикрепи в шаблон в Google Docs.
</details>

Решение 3


![Интерфейс](https://sun9-52.userapi.com/impg/jxyWgFAk_r0XrsVNh9JROFgIjeUsWsXnfJSD-A/kfaq91rRlCE.jpg?size=648x710&quality=96&sign=8efadd8d78df041c8faf08fcb0826f06&type=album)

Задание 4

Тест-дизайн: классы эквивалентности

Повторный тест-анализ проведен! Теперь тебе предстоит выделить классы эквивалентности для расстояния и времени начала движения. Продолжай работать с тем же видом транспорта, который выбран в предыдущем задании.

Решение 4

2 лист в таблице

https://docs.google.com/spreadsheets/d/18092eiIfdvr_nGDBCNHG1hYMR94TtexubJqN4vzytbE/edit#gid=1058266973

Задание 5 

Тест-дизайн: тест-кейсы

Если у тебя уже есть тестовые значения из предыдущего задания, то можно приступать к тест-кейсам. Продолжай работать с тем же видом транспорта.

Решение 5

3 лист в таблице

https://docs.google.com/spreadsheets/d/18092eiIfdvr_nGDBCNHG1hYMR94TtexubJqN4vzytbE/edit#gid=1058266973

</details>

## <a name="test-web" />ТЕСТИРОВНИЕ ВЕБ-ПРИЛОЖЕНИЙ

<details>
<summary>Проект №2</summary>

Проект 2-го спринта: задание



### Часть 1

<details>
<summary>Описание 1 части</summary>


Текущая версия Яндекс.Маршрутов сильно отличается от версии из первого спринта. Например, теперь в приложении можно заказать каршеринг. В первой части проекта тебе предстоит протестировать эту функциональность в двух окружениях:

Яндекс.Браузер, разрешение экрана 800x600;

Firefox, разрешение экрана 1920x1080.

Проанализируй макеты и требования к каршерингу. Если требования и макеты не сходятся — ориентируйся на требования.

<details>
<summary>макеты</summary>
 https://www.figma.com/file/42mNwme0cBfZwNZUIcN1mh/%D0%AF%D0%BD%D0%B4%D0%B5%D0%BA%D1%81.%D0%9C%D0%B0%D1%80%D1%88%D1%80%D1%83%D1%82%D1%8B?type=design&node-id=2-18586&mode=design
</details>

<details>
<summary>требования</summary>
https://praktikum.notion.site/07f02ccc272e494db6501def032e9258
</details>

Изучи приложение на тестовом стенде

1 Подготовь тестовую документацию, чтобы проверить вёрстку формы бронирования и навигационной карты.

![Интерфейс](https://sun9-49.userapi.com/impg/rvTHs9ryL_XxS2VahajGMNh_BThCJqk2s5Bd_Q/e7wImL70Hl0.jpg?size=2560x1348&quality=96&sign=dc4097141dbd118c36ff06df8f28650d&type=album)

Чтобы это сделать:

Внимательно изучи макеты каршеринга в Figma — вкладка «Marshruti car sharing».

Обрати внимание на блок «Требования к заказу». В макетах изображен не каршеринг, а такси: это вкладка «Marshruti taxi» → UI kit. Но принцип работы везде одинаковый. Отличаются только тарифы и текст.

Подробнее о работе панели «Требования к заказу» в каршеринге можно прочитать в текстовых требованиях.

Составь чек-лист, по которому будешь тестировать вёрстку формы бронирования и элементов на навигационной карте: это иконки автомобилей и действия с ними..

Выбери только один тариф. Например, «Роскошный».

Обращай внимание на орфографию, расположение элементов, их внешний вид — в том числе на навигационной карте, которая находится в центральной части интерфейса.

Не забудь про всплывающие окна: «Машина забронирована», «Вы уверены, что хотите отменить поездку?», «Поездка отменена».

Валидацию полей, а также вёрстку окон «Добавление прав», «Способ оплаты», «Добавление карты» тестировать не нужно.

Помести чек-лист на первую вкладку таблицы — «Часть 1. Чек-лист на вёрстку».

2. Подготовь тестовую документацию, чтобы проверить логику работы.
   
Проанализируй требования к функциональности каршеринга.

Составь чек-лист, по которому будешь проверять функциональность окон «Способ оплаты» и «Добавление карты». Здесь пригодятся соответствующие пункты требований: «Поле “Способ оплаты”» и «Окно “Добавление карты”».

Когда будешь составлять чек-лист, используй технику разбиения на классы эквивалентности и выделения граничных значений.

Не забудь про позитивные и негативные проверки.

Подготовь тест-кейсы:

На логику работы кнопки «Забронировать» — см. пункт требований «Кнопка “Забронировать”».

На логику функциональности бронирования — см. пункт требований «Бронь машины».

Не забудь про позитивные и негативные проверки.

Заполни соответствующие вкладки таблицы:

«Часть 1. Чек-лист «Способ оплаты» и «Добавление карты».

«Часть 1. Тест-кейсы на кнопку «Забронировать».

«Часть 1. Тест-кейсы на логику функциональности бронирования».

Обрати внимание: 

На кнопке «Забронировать» указаны расстояние и время в пути. Например: «Маршрут составит 3 км и займёт 4 мин». Тебе не нужно проверять, правильно ли рассчитаны эти данные.

Таймер, который отсчитывает время бесплатного ожидания, тестировать также не нужно.

4. Протестируй приложение и заведи баг-репорты

Протестируй функциональность каршеринга по чек-листам и тест-кейсам, которые тебе удалось спроектировать ранее. Времени на проверку осталось мало, поэтому используй только две конфигурации окружения:

Яндекс.Браузер при разрешении экрана 800x600;

Firefox при разрешении экрана 1920x1080.

Тестирование вёрстки нужно провести в обоих окружениях. Логику приложения достаточно проверить в одном окружении.

Когда будешь тестировать, отмечай результаты выполнения проверок: PASSED, FAILED или SKIPPED (англ. «пропущен»). Если тест со статусом FAILED —заведи баг-репорты в YouTrack. Не забудь вписать ID в соответствующую таблицу результатов. 

Обрати внимание: 

В требованиях сказано, что после заполнения поля «Добавить права» включается таймер на 30 секунд. В текущей реализации его нет. Разработчики специально передали тестовый стенд: так тебе не придётся ждать каждый раз, когда выполняешь проверку.

</details>

### Часть 2

<details>
<summary>Описание 2 части</summary>

Частные авиаперевозки развиваются быстро, и нужно успеть занять нишу. Поэтому в Яндекс.Маршруты добавили новый вид транспорта — аэротакси.

Тебе предстоит протестировать эту функциональность в Яндекс.Браузере.

Постановка задачи

Чтобы ускорить разработку, фронтенд и бэкенд для аэротакси делали одновременно: фронтенд уже готов, а бэкенд задерживается. 

Твоя задача — протестировать реализацию на фронтенде, не дожидаясь бэкенда. Для этого придётся поработать в Charles.

Изучи требования к новой фиче.

Изучи чек-лист на последней вкладке шаблона: «Часть 2. Чек-лист на Аэротакси».

Запусти Яндекс Маршруты и подмени ответы от бэкенда, чтобы отобразить новый тип транспорта. В интерфейсе должны появиться стоимость и время поездки.

На базе изменённых ответов создай автоматический ответ — так удобнее тестировать приложение.

Когда настроишь все автоматические ответы, протестируй новую функциональность по готовому чек-листу из шаблона выше.

Если нужно — заведи баг-репорты в Трекере.

Не забудь про распространённые ошибки в Charles.

Оформи задание: создай папку в Google Drive или Яндекс Диске. Помести туда следующие скриншоты:

Оригинальный ответ с видами транспорта из DevTools или Charles.

Изменённый ответ с видами транспорта из Charles.

Окно с настройками автоматического ответа по видам транспорта из Charles.

Оригинальный ответ с расчётом стоимости и длительности поездки из DevTools или Charles.

Изменённый ответ с расчётом стоимости и длительности поездки из Charles.

Окно с настройками автоматического ответа по расчёту стоимости и длительности поездки из Charles.

</details>

### Решение 2 проекта

https://docs.google.com/spreadsheets/d/1npPsju-U-WiTTV18z8oS_nJW7WkSjoBVRJklZ0nQnQw/edit#gid=899462569

</details>

## <a name="test-api" />ТЕСТИРОВАНИЕ МОБИЛЬНЫХ ПРИЛОЖЕНИЙ И API

<details>
<summary>Проект №3</summary>

<details>
<summary>Требования</summary>
  
  Яндекс.Метро — сервис, который позволяет ориентироваться в метро с помощью мобильного устройства. 
  
  В приложении есть схема метро, которая помогает построить маршрут и оценить время в пути; в приложении появляются актуальные уведомления о работе станций метро и изменениях графика работы. 
1. Список маршрутов
   
1.1. В карточке маршрута отображается:

информация маршрута — логотипы метро и номера линий метро, также сохраняется последовательность пересадок (если есть); 

количество пересадок (если есть); 

временной интервал маршрута — время в пути, время отправления и прибытия; 

кнопка «Закрыть»;  

кнопка «Детали маршрута»; 

поля «Откуда» (начальный пункт) и «Куда» (пункт назначения) (поля должны валидироваться). 

 ![2](https://sun9-46.userapi.com/impg/go8110FW4iUSTc4fF9KlTvJJJRj4AHy--zKVPg/x_aSFoixEyc.jpg?size=1400x571&quality=96&sign=3a8c2a7aabc2892d47e1e2e95ef956a8&type=album)

 1.2. Сброс маршрута 
 
Закрыть маршрут можно только тапом на крестик в карточке маршрута. При закрытии маршрута в поле ввода «Откуда» сохраняется начальная станция из последнего маршрута. Поле ввода «Куда» и маршрут на схеме сбрасывается, выделение станций пропадает (кроме начальной станции).

Если текущее время превышает время окончания маршрута, то временной интервал маршрута обновляется.

2. Выбор станции
   
2.1. Станцию можно выбрать несколькими способами:

тапом на схеме;

по иконке i из разных карточек маршрута. Если из поиска выбрать станцию тапом на i и закрыть карточку станции, должен происходить возврат на экран поиска;

![3](https://sun9-77.userapi.com/impg/_gfJqpWUZrlSG-HN3I6yUNvbcwzUXzCzZs9kZQ/TW_BzpEMZLo.jpg?size=1400x573&quality=96&sign=0b348e075b8c196a2bf4261e133e2c7f&type=album)

найти в поиске и нажать на станцию.

2.2. Если станция выбрана, всегда выполняются следующие действия:

Точка станции на схеме уменьшается.

На точке станции появляется пин цвета линии или специальный пин для закрытой станции.

![](https://sun9-58.userapi.com/impg/9i9MnIAWIQ68T65Jj48ZWZO_SENQG5rD9U_MXg/UDidE7iNW4Y.jpg?size=1400x268&quality=96&sign=e10a50737fd6da7a2ad44fbb2953ef43&type=album)

Выбранная станция сохраняется в истории: при нажатии на поле «Откуда» или «Куда» раскрывается список, содержащий станции, которые пользователь выбирал ранее. Список должен сохраниться и в новой версии приложения.

Шрифт названия станции становится bold.

3. Детали маршрута

3.1. Переход к карточке маршрута

Детали маршрута открываются двумя способами:

по тапу на кнопку Деталей маршрута в карточке маршрута;

по свайпу списка маршрутов вверх (только для смартфонов в портретной ориентации).

3.2. Отображение

В карточке маршрута отображается:

Временной интервал маршрута:

время в пути;

время отправления;

время прибытия;

отрезки пересадок между участками маршрута.

Кнопка «Закрыть»

Участки маршрута, разделённые сообщениями о пересадке

Сообщение об удобных вагонах для посадки

Картинка с указанием удобных вагонов

Станции прибытия и отправления

Пересадочные станции

Промежуточные станции (если на участке больше одной промежуточной станции, отображаются свёрнутым списком)

Рядом с каждой станцией, кроме промежуточных, отображается кнопка i для перехода в карточку станции


Станция, расположенная в начале каждого участка, содержит название, номер линии и иконку сервиса

Для каждой станции может отображаться событие

При смене ориентации с портретной на ландшафтную детали маршрута отображаются в левой части экрана

3.3. Закрытие карточки маршрута

Закрыть карточку маршрута можно также двумя способами:

по тапу на кнопку «Закрыть»;

свайпом вниз.

При закрытии деталей остаётся открытым список маршрутов, положение списка сохраняется, построенный маршрут не сбрасывается.

4. Уведомление об ошибке:

При отсутствии интернет-соединения появляется уведомление об ошибке.

5. Логика для альбомной ориентации

Карточки маршрута и станции и поля поиска отображаются в левой части экрана.

Карточки маршрута и станции открываются на всю высоту экрана.

Карточки станции закрываются при взаимодействии со схемой.

Маршруты отображаются в списке в левой части экрана.

Баннер на маршруте отображается сверху списка маршрута, если доступно достаточно места.

При смене ориентации экрана масштаб построенного маршрута не должен увеличиться или уменьшиться.

Список маршрутов не сворачивается при тапе на ячейку маршрута. Выбранный маршрут выделяется.

При построении маршрута маршрут вписывается в свободную область справа.

При тапе на станцию на схеме (с и без маршрута) происходит минимальный подскролл схемы, чтобы вместить пин.

При выборе станции по иконке i происходит минимальный подскролл схемы, чтобы вместить пин.

Карточки маршрута, станции и настроек сохраняют своё положение при переходе из портретной ориентации в ландшафтную (и обратно): свёрнутые остаются свёрнутыми, открытые — открытыми, среднее положение переходит в среднее.

Карточка Настроек открывается по центру экрана на некоторых девайсах (iPad и некоторые iPhone).

6. Лонг-тап по станции

При нажатии на станцию при помощи лонг-тапа открывается карточка станции с кнопками «Отсюда»/«Сюда».

![](https://sun9-79.userapi.com/impg/RA_VYs1fFvSkwQdWjvz7jDIRSLuSeFELp1MUSg/BdUdM8dKLus.jpg?size=693x807&quality=96&sign=3696d755e0affd1dfca9af9cc344532d&c_uniq_tag=A6oBN7-w807VC1junmVkte0ai2u8Goh9N3CzwYqPlVg&type=album)

Схема не должна смещаться вверх/вниз/влево/вправо при лонгтапе по станции.

7. Скролл схемы при помощи лонг-тапа

Чтобы воспроизвести скролл схемы при помощи лонгтапа — сделай лонгтап по станции и, удерживая палец, переводи фокус на другие станции.

При скролле лонгтапом можно выбрать нужную станцию, при этом схема остаётся неподвижной.

При попадании на область клика точки станции или её названия, на точку ставится пин, точка станции уменьшается, название станции выделяется

жирным шрифтом, появляется карточка станции.

Пин на станции и выделение станции пропадает, когда она не попадает в зону клика.

При дальнейшем движении шапка карточки станции остаётся неподвижной, и в ней меняются названия станций и сервисов. При этом карточка станции сохраняет минимальное состояние.

Если движение заканчивается на пустой области, карточка станции закрывается.

</details>


<details>
<summary>Задание 3 проекта</summary>

Тебе предстоит протестировать мобильное приложение и API. Как и в прошлых спринтах, результаты заданий нужно поместить в гугл-док и прикрепить ссылку в тренажёр. Для обоих заданий пригодится шаблон.

Мобильное приложение

Команда сделала рефакторинг приложения под Android. Чтобы выпустить новую версию, нужно протестировать те части продукта, которых коснулись изменения. Тестовой документации ещё нет, поэтому её нужно написать. 

Постановка задачи

Проанализируй требования к мобильному приложению Яндекс.Метро из предыдущего урока.

Напиши чек-лист для тестирования мобильного приложения на часть требований, выделенных жирным шрифтом. При необходимости визуализируй требования через mindmap или блок-схемы. Визуализацию сдавать не нужно.

Протестируй мобильное приложение в эмуляторе с помощью Android Studio или на своём Android-устройстве и заведи баг-репорты в YouTrack. Не забудь, что у ревьюера должен быть доступ к твоему проекту. Инструкция есть в этом уроке. Скачай готовящуюся к релизу версию приложения тут.

Чтобы проверить, что обновление происходит корректно, скачай предыдущую версию тут. Вспомни, как правильно это сделать: нужно установить предыдущую версию приложения, а затем обновить её на новую.

В процессе тестирования отмечай результаты выполнения теста: PASSED или FAILED. Если тест со статусом FAILED, заведи баг-репорт в YouTrack и впиши ID в соответствующую таблицу результатов.


### API

Разработчики сделали новую функциональность в API Яндекс.Прилавка. Новую версию API передали тебе на тестирование. 

Изучи новую функциональность.

Работа с наборами: возможность добавлять продукты в набор — ручка POST /api/v1/kits/:id/products.

Работа с курьерами: возможность проверить, есть ли доставка курьерской службой «Привезём быстро» и сколько она стоит. Ручка POST /fast-delivery/v3.1.1/calculate-delivery.xml. 

Работа с корзиной:

возможность получить список продуктов, которые добавили в корзину. Ручка GET /api/v1/orders/:id;

возможность добавлять продукты в корзину. Ручка PUT /api/v1/orders/:id;

возможность удалять корзину. Ручка DELETE /api/v1/orders/:id.

Постановка задачи

Проанализируй требования к новой функциональности бэкенда Яндекс.Прилавка. Изучи документацию к API в Apidoc. 

<details>
<summary>Требования к бэкенду находятся здесь.</summary>
  https://praktikum.notion.site/8c91f759cb834ef2aa23db9d803a6373
</details>

Спроектируй тесты в виде чек-листа, чтобы покрыть функциональность, которую тебе передали на тестирование: она описана выше. Авторизацию проверять не нужно.

Чек-лист помести в гугл-таблицу. Создай копию шаблона и открой доступ на комментирование по ссылке.

Протестируй API через Postman и заведи баг-репорты в YouTrack, если это понадобится.

</details>

## Решение 3 проекта
<details>
<summary>Решение</summary>
https://docs.google.com/spreadsheets/d/132cixwfebR8Qr1eTbhfD4S2OFr9jp6SNqNu4vKOA7Jk/edit#gid=857523888
</details>
</details>

## <a name="test-bd" /> Основы баз данных

<details>
<summary>Проект №4</summary>


<details>
<summary>Задание 4 проекта</summary>
### Консоль
  
Задание 1
  
От разработчиков поступила задача: нужно выяснить, какие запросы шли с IP-адреса. IP-адрес состоит из четырёх чисел, они разделены точками. Тебе нужны адреса, которые начинаются с «233.201.».
  
Логи лежат на удалённом сервере по адресу logs/2019/12. День, когда случилась ошибка, неизвестен. 
  
Твоя задача — узнать, какие запросы были отправлены. 
  
В ответе приложи:
  
команду, которой тебе удалось получить нужные логи;
  
подходящие строки, например: 184.79.247.161 - - [30/12/2019:21:38:13 +0000] "PUT /alerts HTTP/1.1" 400 3557
  
Задание 2
  
В системе обнаружен баг. Он проявлялся 30.12.2019 и 31.12.2019 с 21:30:00 до 21:39:59. При этом появлялись ошибки с номерами 400 и 500. Твоя задача — сохранить в отдельный файл логи, которые были записаны в этот период.  
  
Затем эти логи надо разложить по отдельным файлам: логи с одинаковой ошибкой положи в один файл. Как это сделать:
  
В домашней директории на удалённом сервере создай директорию bug1.
  
Все запросы, которые произошли в указанный период, положи в файл main.txt в директорию bug1.
  
Внутри директории bug1 создай директорию events.
  
Внутри директории events создай файлы для ошибок с номерами 400 и 500. Назови эти файлы 400.txt и 500.txt соответственно. В них выдели логи с соответствующей ошибкой из файла main.txt.
  
В ответе приложи:
  
команды, которые создают директории bug1 и events;
  
команду, которой ты выбираешь запросы за указанный период. Это те запросы, которыми ты отбираешь логи в файл main.txt;
  
команды, которыми ты кладёшь логи в файлы 400.txt и 500.txt из main.txt;
  
тексты файлов 400.txt и 500.txt.

### База данных

Описание данных

База данных о поездках такси в Чикаго:

Таблица neighborhoods — информация о районах города:

neighborhood_id — код района;

name — название района.

Таблица cabs — информация о такси:

cab_id — идентификатор такси;

vehicle_id — уникальный идентификатор автомобиля;

company_name — компания, которой принадлежит автомобиль.

Таблица trips — информация о поездках:

trip_id — код поездки;

cab_id — идентификатор такси, на котором была совершена поездка;

start_ts — дата и время начала поездки (время округлено до часа);

end_ts — дата и время окончания поездки (время округлено до часа);

duration_seconds — длительность поездки в секундах;

distance_miles — дальность поездки в милях;

pickup_location_id — код района города, в котором была начата поездка;

dropoff_location_id — код района города, в котором завершилась поездка.

Таблица weather_records — информация о погоде:

record_id — код записи погодных наблюдений;

ts — дата и время наблюдения (время округлено до часа);

temperature — температура на момент наблюдения;

description — краткое описание погодных условий. Например, light rain или scattered clouds.

Схема таблиц

![](https://sun9-69.userapi.com/impg/i4zyzHNcNNkTNUCkxIjwrI7dNrGBCK4WJTNDYA/jT6QVdVhOvo.jpg?size=807x433&quality=96&sign=37bc5e8b2720d87530f246557c772740&c_uniq_tag=DKiqH8mZKredtVFYHF2Qmc7fLD3euCRdI3766Ji8RkE&type=album)

В базе данных нет прямой связи между таблицами trips и weather_records. Связать эти таблицы можно по времени начала поездки (trips.start_ts) и моменту погодных наблюдений (weather_records.ts). 

### Задание 1

У тебя есть база данных с поездками на такси. По плану на линию обслуживания должно было выйти 10550 автомобилей — эта цифра покрывает спрос пользователей. Команде поступило много жалоб: свободных автомобилей оказалось недостаточно. Сколько такси вышло на линии на самом деле? Информация о всех машинах на линии есть в таблице cabs.

Зайди на удалённый сервер.

Подключись к базе данных chicago_taxi, используй логин morty и пароль smith.

Посчитай, сколько всего автомобилей в таблице cabs. Учти, что один автомобиль может принадлежать разным компаниями.

В ответе приложи:

число автомобилей;

запрос, которым тебе удалось решить задачу.

### Задание 2

Посчитай количество автомобилей в каждой компании из таблицы cabs. Отсортируй значения по убыванию. Команда предполагает, что некоторые компании не вывели достаточно автомобилей на линию. 

Выведи те компании, в которых меньше 100 автомобилей. Поле с числом автомобилей назови cnt, поле с названием компании — company_name.

Чтобы решить задачу, примени оператор HAVING — аналог WHERE для агрегирующих функций. Изучи в документации, как работает оператор: 

(https://postgrespro.ru/docs/postgrespro/11/queries-table-expressions#QUERIES-GROUP)

В ответе приложи: 

список компаний с числом автомобилей меньше 100;

запрос, которым тебе удалось решить задачу.

Обрати внимание: в консоль выводится неполный список. Чтобы просмотреть его полностью, нажми Enter или используй стрелки на клавиатуре. 

### Задание 3

В приложении такси рассчитывается коэффициент стоимости поездки. Если погода хорошая, значение коэффициента равно 1. Если на улице дождь или шторм, коэффициент повышается до 2. У команды есть гипотеза, что в расчётах коэффициента ошибка. Чтобы проверить расчёт коэффициента, команде нужна выборка данных: разработчик может сверить коэффициент с данными в логах и исправить баг. Твоя задача — получить выборку.

Чтобы это сделать:

Получи описание погодных условий из таблицы weather_records для каждого часа.

Раздели все часы на две группы оператором CASE: Bad, если поле description содержит слова rain или storm; Good для всех остальных.

Полученное поле назови weather_conditions.

В результирующей таблице должно быть два поля — дата и час (ts) и weather_conditions.

Сделай выборку за период с 2017-11-05 00:00 по 2017-11-06 00:00.

В ответе приложи:

полученную таблицу с данными за указанный период;

запрос, которым удалось решить задачу.

### Задание 4

После обновления ПО таксопарки стали сообщать, что прибыль, которую они получают, не сходится с данными, которые отдаёт приложение. Разработка предполагает, что проблема может быть в данных о количестве поездок. 

Чтобы определить, есть ли баг, нужно получить выборку с количеством поездок каждого таксопарка за 15 и 16 ноября 2017 года. 

Выведи поле company_name. Поле с числом поездок назови trips_amount и выведи его.

Результаты, полученные в поле trips_amount, отсортируй по убыванию.

Подсказка: чтобы решить задачу, соедини таблицы cabs и trips. Примени агрегирующие функции с группировкой. Не забудь написать конструкцию с условием.

В ответе приложи:

полученную таблицу с данными за указанный период;

запрос, которым удалось решить задачу.

</details>

## Решение 4 проекта
<details>
<summary>Решение</summary>
https://docs.google.com/document/d/1XpbE9BDz_Pzr-DvjXGEvS9GZBf6Ug46h76BURjtTZew/edit
</details>
</details>

## <a name="test-avto" />Основы автоматизации тестирования

<details>
<summary>Проект №5</summary>

        
### Задание 1

Автоматизируй тест-кейс для Яндекс.Маршрутов. Найди нужные селекторы на стенде: <https://qa-routes.praktikum-services.ru/>

```
[CASE-1] Проверка названия вида транспорта в результате для такси

Шаги:
1. Ввести «Время начала поездки» — 08:00.
2. В поле «Откуда»: Усачева, 3.
3. В поле «Куда»: Комсомольский проспект, 18.
4. Выбрать режим «Свой».
5. Выбрать вид транспорта: такси.

ОР: Текст появившегося результата начинается со слова «Такси».
```

### Решение

Селекторы:

| Элемент  | Селектор  |
|:----------|:----------|
| Поле «Часы»    | #form-input-hour    |
| Поле «Минуты»    | #form-input-minute    |
| Поле «Откуда»    | #form-input-from    |
| Поле «Куда»    | #form-input-to    |
| Режим «Свой»    | #form-mode-custom    |
| Транспорт «Такси»    | #from-type-taxi    |
| Строка результата    | #result-time-price    |

Автотест:

```javascript
const puppeteer = require('puppeteer');

const URL_TEST = 'https://qa-routes.praktikum-services.ru/';

async function testTaxiResult() {
    console.log('Запуск браузера');
    const browser = await puppeteer.launch({headless: false, slowMo: 100});

    console.log('Создание новой вкладки в браузере');
    const page = await browser.newPage();

    console.log('Переход по ссылке');
    await page.goto(URL_TEST);

    console.log('Шаг 1: ввод часов и минут');
    const hoursInput = await page.$('#form-input-hour');
    await hoursInput.type('08');

    const minutesInput = await page.$('#form-input-minute');
    await minutesInput.type('00');

    console.log('Шаг 2: заполнение поля Откуда');
    const fromInput = await page.$('#form-input-from');
    await fromInput.type('Усачева, 3');

    console.log('Шаг 3: заполнение поля Куда');
    const toInput = await page.$('#form-input-to');
    await toInput.type('Комсомольский проспект, 18');

    console.log('Шаг 4: выбор режима Свой');
    const routeMode = await page.$('#form-mode-custom');
    await routeMode.click();

    console.log('Шаг 5: выбор вида транспорта');
    const typeOfTransport = await page.$('#from-type-taxi');
    await typeOfTransport.click();

    console.log('Ожидание элемента с результатом');
    await page.waitForSelector('#result-time-price')

    console.log('Получение строки с результатом');
    const text = await page.$eval('#result-time-price', element => element.textContent);

    console.log('Проверка условия тест-кейса');
        if (text.startsWith('Такси')) {
        console.log('Успех. Текст содержит: ' + text);
    } else {
          console.log(`Ошибка. Текст не начинается со слова 'Такси'`)
    }

    console.log('Закрытие браузера');
    await browser.close();
}

testTaxiResult();
```

[Наверх](#up)

### Задание 2

Автоматизируй тест-кейс для [ya.ru](https://ya.ru), применив нужные селекторы.

```
[CASE-2] Проверка появления результатов поиска

Предусловие:
Перейти на страницу ya.ru.

Шаги:
1. Ввести «Автоматизация тестирования» в поисковую строку.
2. Нажать кнопку «Найти».

ОР: Выполнен переход на страницу выдачи поиска и результат поиска непустой.
```

### Решение

Селекторы:

| Элемент  | Селектор  | 
|:----------|:----------|
| Поисковая строка    | #text    |
| Кнопка «Найти»    | .button[type=submit]    |
| Результат поиска	    | .serp-item    |

Автотест:

```javascript
const puppeteer = require('puppeteer');

async function testYaRu() {
    console.log('Запуск браузера');
    const browser = await puppeteer.launch();

    console.log('Создание новой вкладки в браузере');
    const page = await browser.newPage();

    console.log('Переход на страницу ya.ru');
    await page.goto('https://ya.ru/');

    console.log('Ввод текста "Автоматизация тестирования" в поисковую строку');
    const searchField = await page.$('#text');
    await searchField.type('Автоматизация тестирования');

    console.log('Клик в кнопку "Найти"');
    const searchButton = await page.$('.button[type=submit]');
    await searchButton.click();
    
    console.log('Ожидание перехода в страницу поисковых результатов');
    await page.waitForNavigation();
    
    console.log('Получение элементов результата поиска');
    const result = await page.$('.serp-item');
    
    console.log('Сравнение ОР и ФР');
    if (result == null) {
        console.log('Результаты поиска не найдены');
    } else {
        console.log('Результаты поиска отобразились');
    }
    
    console.log('Закрытие браузера');
    await browser.close();
}

testYaRu();
```
</details>


## [Вернуться к темам проектов Андрея](#head)<br>
