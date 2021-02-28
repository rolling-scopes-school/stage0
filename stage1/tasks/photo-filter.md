# photo-filter

### Предварительная версия задания в которую могут вноситься правки. Окончательная версия будет доступна после выдачи задания

| Дата выдачи | Deadline         | Folder name   | Branch name   |
| ------------| ---------------- | ------------- | ------------- |
|             |                  | photo-filter  | photo-filter  |

Даты выдачи и дедлайны тасков находятся в [расписании](https://docs.google.com/spreadsheets/d/1oM2O8DtjC0HodB3j7hcIResaWBw8P18tXkOl1ymelvE/edit#gid=1646898206)

## Task 2. photo-filter

![screenshot](images/photo-filter.png)

- [Демо](https://rolling-scopes-school.github.io/stage1-tasks/photo-filter/)
- [Файлы проекта](https://github.com/rolling-scopes-school/stage1-tasks/tree/photo-filter/photo-filter)
- [Советы по написанию кода](stage1/tasks/photo-filter-hints.md)
- [Описание stage1 js-projects](stage1/tasks/js-projects.md)

В ходе выполнения задания вам необходимо создать приложение позволяющее добавить изображению css-фильтры и сохранить изображение с наложенными на него фильтрами. Фото в приложение можно загрузить с компьютера или по url.

## Структура и работа приложения
- на странице отображается фото и настройки css-фильтров в виде ползунков, каждому из которых соответствует определённый css-фильтр
- кнопка Reset позволяет сбросить настройки css-фильтров
- кнопка Next picture предназначена для смены изображений, которые загружаются с внешнего ресурса по ссылке
- кнопка Load picture для загрузки фото с компьютера 
- кнопка Save picture позволяет скачать фото с добавленными фильтрами на компьютер

## Функциональность приложения
- напротив каждого ползунка есть окно, в котором отображается значение соответствующего css-фильтра. при перемещении ползунка значение изменяется
- при перемещении ползунка меняется внешний вид фото в соответствии с изменением значения соответствующего css-фильтра
- при клике по кнопке Reset, сбрасываются значения всех css-фильтров, соответственно возвращаются к исходному состоянию положение ползунков, значения в соответствующих окошках и внешний вид фото
- при нажатии на кнопку Next picture, загружается следующая картинка из списка картинок, подключенных по ссылке. Ссылку на картинки берем [здесь](https://github.com/rolling-scopes-school/stage1-tasks/tree/assets/images). Изображения разделены тематически по времени суток. Каждый период находится в своей папке по указанной ссылке day, nigth и т.д. В каждой папке 20 изображений. После последнего изображения загружается первое. Картинки должны соответствовать текущему времнени суток:
  + с 6 утра до 12 дня - утро
  + с 12 дня до 6 вечера - день
  + с 6 вечера до 12 ночи - вечер
  + с 12 ночи до 6 утра - ночь
- при клике по кнопке Load picture открывается окно выбора файлов на компьютере, выбранное фото отображается в приложении. Пропорции фото не искажены
- при клике по Save picture фото загружается на компьютер вместе с добавленными фильтрами
- есть кнопка Fullscreen при клике по которой можно развернуть приложение во весь экран

## Критерии оценки

**Максимальный балл за задание +60**
- реализовано не меньше 5 ползунков для настройки css-фильтров. Возле каждого ползунка отображается его актуальное значение +5
- при перемещении ползунка меняется внешний вид фото в соответствии с изменением значения соответствующего css-фильтра +10
- реализован сброс css-фильтров +5
- реализована возможность смены картинок, подключенных по ссылке +10
- подключенная картинка соответствует текущему времени суток +5
- изображение можно загрузить с локального компьютера +10
- изображение можно скачать на компьютер +10
- изображение скачивается на компьютер с применёнными фильтрами +5

## Ключевые навыки
- использование js для загрузки локальных файлов на веб-страницу
- использовать js для сохранения изображений на компьютер
- работа с датами в js
- Canvas API

## Материалы:
### Теория
- [input](https://developer.mozilla.org/ru/docs/Web/HTML/Element/Input)
- [input type="range"](https://developer.mozilla.org/ru/docs/Web/HTML/Element/Input/range)
- [output](https://developer.mozilla.org/ru/docs/Web/HTML/Element/output)
- [События: change, input](https://learn.javascript.ru/events-change-input)
- [Element.matches()](https://developer.mozilla.org/ru/docs/Web/API/Element/matches)
- [CSS Filters](https://css-tricks.com/almanac/properties/f/filter/)
- [CSS Filters for Online Photo Editing](https://orangeable.com/css/filters)
- [Использование переменных в CSS](https://developer.mozilla.org/ru/docs/Web/CSS/Using_CSS_custom_properties)
- [Изучите CSS-переменные за 5 минут](https://medium.com/devschacht/изучите-css-переменные-за-5-минут-3a5dc6193857)
- [Дата и Время в js](https://learn.javascript.ru/datetime)

### Видео
- [JS30. CSS Variables](https://youtu.be/AHLNzv13c2I)

### Демо для вдохновения
- [Магия фильтров: 9 интересных приложений для обработки фото](https://asn24.ru/sova/community/magiya-filtrov-9-interesnykh-prilozheniy-dlya-obrabotki-foto-v-instagram/)
- [CSSFilterGenerator](https://www.cssfiltergenerator.com/)

[Документ для вопросов](https://docs.google.com/spreadsheets/d/1dMDLBC4-1XPaVMehZB6DqetToXZhq4x0PiZtj-jvLRc/edit#gid=487334651)

## Cross-check
- инструкция по проведению cross-check: https://docs.rs.school/#/cross-check-flow
- ссылки на лучшие работы с дополнительным функционалом либо авторским качественным оформлением добавьте, пожалуйста, в эту форму [https://forms.gle/QELfqGDNCaPLHMzo9](https://docs.google.com/forms/d/e/1FAIpQLSc7DQoF0U4lB2qdMceofIl1F59UFS-pQAfQfJwcAc4nIXn31g/viewform?usp=sf_link)