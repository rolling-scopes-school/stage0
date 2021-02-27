## Прогноз погоды в 20 строк

Создадим небольшое приложение с прогнозом погоды для указанного пользователем города

### Регистрация

Регистрируемся в OpenWeatherMap API [https://home.openweathermap.org/users/sign_up](https://home.openweathermap.org/users/sign_up)

На указанную при регистрации почту приходит письмо с предложением подтвердить e-mail. Подтверждаем.

На странице [https://home.openweathermap.org/api_keys](https://home.openweathermap.org/api_keys) видим свой API key

### Получение информации о погоде

Для получения информации о погоде создаём ссылку
`https://api.openweathermap.org/data/2.5/weather?q=Минск&lang=ru&appid=08f2a575dda978b9c539199e54df03b0&units=metric`

Здесь:
- `Минск` - название города, можно указывать на русском или на английском
- `08f2a575dda978b9c539199e54df03b0` - API key полученный при регистрации 
- `lang=ru` - язык отображения описания погоды (можно указать `lang=en`)
- `units=metric` - температура в градусах Цельсия (можно указать `units=imperial` для отображения температуры в градусах Фаренгейта)

Дальше используем только ссылку с своим собственным API key. Если использовать ссылку, пример которой приводится в задании, очень быстро исчерпается лимит API, и она перестанет работать.

### Просмотр информации о погоде

Переходим по созданной ссылке.  На странице отображается информация о погоде. Для удобного её отображения можно установить расширение [**JSONView**](https://chrome.google.com/webstore/detail/jsonview/chklaanhfefbnpoihckbnefhakgolnmc?hl=ru)

По ссылке отображается объект с погодой. Некоторые свойства данного объекта:
- `.weather[0].id` - id иконки погоды
- `.weather[0].description` - описание погоды
- `.main.temp` - температура

### Вывод информации о погоде в консоль

Получим информацию о погоде. Пока выведем её в консоль.

Для этого создаём асинхронную функцию

```js
async function getWeather() {  
  const url = `https://api.openweathermap.org/data/2.5/weather?q=Минск&lang=ru&appid=08f2a575dda978b9c539199e54df03b0&units=metric`;
  const res = await fetch(url);
  const data = await res.json(); 
  console.log(data.weather[0].id, data.weather[0].description, data.main.temp);
}
getWeather()
```
В функции `getWeather()` мы получили объект с погодой `data` и вывели в консоль интересующие нас свойства.

Ссылка в косых кавычках - шаблонная строка, прочитать о шаблонных строках можно [на сайте mdn](https://developer.mozilla.org/ru/docs/Web/JavaScript/Reference/template_strings)  
Возможность добавить в шаблонную строку значение переменной мы используем позже.

Функция `getWeather()` не большая, не сложная. Единственное её неудобство - все полученные данные доступны исключительно внутри самой функции, получить их в основном коде невозможно. 

### Вывод информации о погоде на страницу

Выведем полученные данные на страницу
В `index.html` создадим элементы

```html
<i class="weather-icon owf"></i>
<div class="temperature"></div>
<div class="weather-description"></div>
```

В `script.js` найдём эти элементы

```js
const weatherIcon = document.querySelector('.weather-icon');
const temperature = document.querySelector('.temperature');
const weatherDescription = document.querySelector('.weather-description');
```

И внутри функции `getWeather()` укажем их содержание

```js
async function getWeather() {
  const url = `https://api.openweathermap.org/data/2.5/weather?q=Минск&lang=ru&appid=08f2a575dda978b9c539199e54df03b0&units=metric`;
  const res = await fetch(url);
  const data = await res.json();

  weatherIcon.classList.add(`owf-${data.weather[0].id}`);
  temperature.textContent = `${data.main.temp}°C`;
  weatherDescription.textContent = data.weather[0].description;
}
```

Блокам с температурой и описанием погоды мы указали `textContent`, иконке погоды добавили класс.

### Отображение иконки погоды

Иконки погоды для Open Weather Map API находятся здесь https://websygen.github.io/owfont/
Скачиваем, распаковываем, папку `fonts` помещаем в папку с проектом, файл `owfont-regular.css` из скачанной папки `css` помещаем в папку `css` нашего проекта, подключаем в `index.html`  перед подключением `style.css` 

```html
<link rel="stylesheet" href="css/owfont-regular.css">
```

### Получаем погоду для определённого города

В `index.html` создадим `div` с классом `city` со свойством `contenteditable="true"`, которое позволяет пользователям редактировать его содержимое и укажем в нём название города, например, `Минск`  

```html
<div class="city" contenteditable="true">Минск</div>
```

В `script.js` найдём этот элемент

```js
const city = document.querySelector('.city');
```

В функции `getWeather()` изменим ссылку

```js
const url = `https://api.openweathermap.org/data/2.5/weather?q=${city.textContent}&lang=ru&appid=08f2a575dda978b9c539199e54df03b0&units=metric`;
```

Теперь у нас отображается погода того города, который указан в блоке `city`.
Напишем функцию `setCity(event)`, для обновлении прогноза погоды при изменении содержания блока city

```js
function setCity(event) {
  if (event.code === 'Enter') {
    getWeather();
    city.blur();
  }
}
```

Если в блоке `city` нажали клавишу `Enter`, запускаем функцию `getWeather()` и убираем фокус с блока `city`.

В функции `getWeather()` перед добавлением иконке погоды дополнительного класса укажем строку

```js
weatherIcon.className = 'weather-icon owf';
```

Этой строкой мы удаляем все лишние классы перед добавлением нового, чтобы иконка погоды обновлялась корректно.

Строки

```js
document.addEventListener('DOMContentLoaded', getWeather);
city.addEventListener('keypress', setCity);
```

запускают отображение прогноза погоды при загрузки страницы и при нажатии на `Enter` в блоке `city` при вводе нового города

Добавим немного стилей и приложение погоды готово.

[Код приложения](https://github.com/rolling-scopes-school/stage1-tasks/tree/gh-pages/weather)  
[Demo](https://rolling-scopes-school.github.io/stage1-tasks/weather/)