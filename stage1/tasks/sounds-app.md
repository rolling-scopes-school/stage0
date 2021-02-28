# sounds-app

### Предварительная версия задания в которую могут вноситься правки. Окончательная версия будет доступна после выдачи задания

| Дата выдачи | Deadline         | Folder name   | Branch name   |
| ------------| ---------------- | ------------- | ------------- |
|             |                  | sounds-app    | sounds-app    |

Даты выдачи и дедлайны тасков находятся в [расписании](https://docs.google.com/spreadsheets/d/1oM2O8DtjC0HodB3j7hcIResaWBw8P18tXkOl1ymelvE/edit#gid=1646898206)

## Task 3. sounds-app

![screenshot](images/sounds-app.png)

- [Демо](https://7oom.ru/penie-ptic.html)
- [Файлы проекта](https://github.com/rolling-scopes-school/stage1-tasks/tree/sounds-app)
- [Советы по написанию кода](stage1/tasks/sounds-app-hints.md)
- [Описание stage1 js-projects](stage1/tasks/js-projects.md)

В ходе выполнения задания вам необходимо создать музыкальное приложение, в котором есть несколько звуковых тем. Каждая тема содержит зацикленное видео, а также несколько аудиоплееров с звуками природы и музыкой. Также в приложении есть виджет с прогнозом погоды. 

## Структура и работа приложения
- в приложении есть несколько звуковых тем. Минимальное количество тем - шесть. Каждая тема содержит зацикленное видео, а также несколько аудио плееров (минимум два для каждой темы) с соответствующими этому месту звуками природы и музыкой
- темы можно перелистывать кликами по стрелкам. При этом видео пролистывается как слайдер с эффектом сдвига слайда, в аудиоплеерах, которые размещаются в боковой панели, меняются названия аудиотреков и ссылки на аудио 
-  в боковой панели есть виджет погоды, отображающий погоду для указанного пользователем населённого пункта

## Критерии оценки

**Максимальный балл за задание +50**
- в приложении есть не меньше шести звуковых тем, каждая из которых содержит зацикленное видео, а также несколько аудио плееров - минимум два для каждой темы +5
- темы можно перелистывать кликами по стрелкам. При этом видео пролистывается как слайдер с эффектом сдвига слайда, в аудиоплеерах, которые размещаются в боковой панели, меняется содержимое +10
- темы можно перелистывать свайпами мышкой по слайдеру с видео +5
- темы пролистываются зацикленно, после последней снова идёт первая +5
- кастомный аудиоплеер, выглядящий так же, как в демо +10
- при открытии новой темы автоматически запускаются все относящиеся к ней аудиоплееры, есть возможность независимо настраивать громкость каждого из них +5
- в боковой панели есть виджет погоды, отображающий погоду для указанного пользователем населённого пункта +5
- последняя выбранная пользователем тема и указанный пользователем город, для которого отображается прогноз погоды, сохраняются при перезагрузке страницы +5

## Ключевые навыки
- работа с HTML5-видео
- создание зацикленного слайдера/свайпера
- кастомизация аудио
- получение данных от API
- работа с асинхронными запросами
- сохранение данных в local storage

## Материалы:
#### HTML5-видео
- [video](https://developer.mozilla.org/ru/docs/Web/HTML/Element/video)
- [HTML5-видео](https://html5book.ru/html5-video/)
#### Slider
- [Делаем слайдер на чистом JavaScript с нуля](https://youtu.be/K3E1OfQuJ0Q) - [код и демо](https://github.com/Eremeow138/wayup-slider-js)
- [Infinite pure Javascript slider](https://medium.com/@claudiaconceic/infinite-plain-javascript-slider-click-and-touch-events-540c8bd174f2) - [код и демо](https://codepen.io/cconceicao/pen/PBQawy)
- [Swiper & Slider Examples (carousel live coding)](https://youtu.be/rkz6LURkbBw) - [код](https://www.dropbox.com/s/0g5c0qz69keig6s/carusel-swiper.zip?dl=0)
#### HTML5-audio
- [HTML5-аудио](https://html5book.ru/html5-audio/)
- [Как создать плеер для сайта на HTML5 и JavaScript](https://skillbox.ru/media/code/kak_sozdat_pleer_dlya_sayta/)
- [Create custom audio player using HTML5 and JavaScript](http://talkerscode.com/webtricks/create-custom-audio-player-using-html5-and-javascript.php)
#### LocalStorage
- [Window.localStorage](https://developer.mozilla.org/ru/docs/Web/API/Window/localStorage)
- [LocalStorage на пальцах](https://tproger.ru/articles/localstorage/)
#### Асинхронность, async/await
- [Поймут даже дети: простое объяснение async/await и промисов в JavaScript](https://habr.com/ru/post/474726/)
- [JavaScript. Как работает Async, Await](https://youtu.be/SHiUyM_fFME)
- [Вебинар: Асинхронность в JavaScript](https://youtu.be/Ih6Q7ka2eSQ)
#### Видео
- [Pixabay](https://pixabay.com/videos/search/nature/)
#### API погоды
- https://openweathermap.org/
#### Демо для вдохновения
- http://ecosounds.net/
- http://7oom.ru/penie-ptic.html
- http://www.allolo.ru/?id=12

[Документ для вопросов](https://docs.google.com/spreadsheets/d/1dMDLBC4-1XPaVMehZB6DqetToXZhq4x0PiZtj-jvLRc/edit#gid=610380603)

## Cross-check
- инструкция по проведению cross-check: https://docs.rs.school/#/cross-check-flow
- ссылки на лучшие работы, добавьте, пожалуйста, в эту форму [https://forms.gle/qzqvrDmWbhLerYzb7](https://docs.google.com/forms/d/e/1FAIpQLSdqWPAPY5lFefhHOzoC0ms2xXPOYr2qGMvAiN87pEmCkj55hw/viewform?usp=sf_link)