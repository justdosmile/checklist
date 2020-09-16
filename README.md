# Чеклист верстки
Для разработчиков Webfact

## Структура
1. Верстка должна **соответствовать макету**. Допускается лишь незначительное расхождение размеров, сделанное с целью исправить расположение криво нарисованных блоков или отступов.

2. Верстка должна быть кроссбраузерной. Корректное отображение в стабильных версиях браузеров: Mozilla Firefox, Yandex.Браузер, Safari, Opera, Miscrosoft Edge, IE 11.

3. Должна быть установлена кодировка `UTF-8`
4. HTML страницы должны проходить проверку на валидность [W3C](https://validator.w3.org/nu/)
5. Первая строка любой страницы должна начинаться с `<!DOCTYPE HTML>`
6. В разметке HTML5 должны использоваться теги `header` `footer` `aside` `nav` `section` `article`
7. Должна быть соблюдена правильная структура заголовков `h1, h2, h3...`
8. Логотип сайта должен вести на главную страницу
9. **Необходимо что бы верстка была надежной!** При изменении текста в блоках, вбивании реального текста (короткий, длинный, длинный без переноса) - сайт не должен ломаться. Все изображения, используемые на сайте в новостях, товарах, в слайдерах и т.д., которые будут выводиться из CMS должны быть заменяемые. Должна быть предусмотрена загрузка изображений любых пропорций и разрешений. С этой целью вместо `img` допустимо использовать `background-image`
10. Ссылки на внешние сайты должны быть с атрибутами: `target="_blank"` и `rel="nofollow noopener"`
11. Все `<input>` должны быть правильного типа `email/url/tel/text/password`
12. При верстке не использовать id, только классы. Именование классов допустимо только маленькими буквами. Если нужно добавить обработчик JS к какому-то элементу ему дается дополнительный класс в стиле js_action.

## Стили
1. Проверить что все интерактивные элементы, которые должны работать - работают. Все ссылки и кнопки имеют стили для `:hover`, поля и textarea имеют стили для `:focus`. Элементы должны реагировать изменением цвета, подчеркиванием, размером, чем угодно. При наведении на такое элементы курсор должен становиться `pointer`
2. В верстке **не должен использоваться Bootstrap**
3. Не должны быть использованы инлайновые `стили style=""` в HTML. Все стили должны быть в CSS файле.
4. Сайт должен корректно отображаться на всех популярных разрешениях экранов: от 320px - до 1920px. Адаптивность сайта должна достигаться только путем использования `@media` запросов. Файл стилей должен быть отдельным и называться `media.css`.
5. Поля ввода `<input>` на мобильных устройствах должны иметь размер текста `font-size: 16px`.
6. Все параметры подключенных шрифтов должны соответстовать макету (размер, межстрочный интервал, стиль). При подключении шрифтов обязательно должен быть указан альтернативый заменяющий шрифт, схожий с кастомным.
7. При расположении блоков на странице использование flex в приоритете (использование float и inline-block только с обоснованием в комментариях)
8. Стили должны соответстовать стандарту CSS3
9. Все тени, градиенты, скругления должны быть реализованы с помощью CSS свойств. Также в CSS следует избегать `!important`, допускается использования этого параметра с обоснованием в комментарии.
10. При использовании LESS, SASS препроцессоров CSS код должен быть обязательно скомпилирован в файл `.css`.

## Скрипты
1. В консоли браузера не должно быть JS ошибок и console.log()
2. Должен быть подключен внутренний jQuery последней стабильной версии
3. Скрипты должны быть подключены перед закрывающим тегом `</body>`. Файл скриптов проекта должен быть самым последним.

## Общее
1. Все изображения должны находиться в отдельной папке, css стили - в отдельной и js скрипты- в отдельной. Графика которая не является частью дизайна (иллюстрации, фотографии в новостях и т.д.) должна находит]мся в отдельной папке (напр. uploads)
2. Все изображения должны быть поджаты без потери качества. Все js-скрипты должны быть минифицированы (без потери читабельности, не js код в одну строку!). Все css файлы должны быть минифицированы без потери читабельности. (Название каждого класса и каждого свойства к нему - разные строки)
3. Сайт должен иметь favicon.ico и apple-touch-icon. При необходимости запросить favicon в дизайнера.
4. Все иконки сайта (в т.ч. логотип) должны быть реализованы при помощи иконочных шрифтов или SVG изображений. При необходимости запросить недостающие изображения у дизайнера.
