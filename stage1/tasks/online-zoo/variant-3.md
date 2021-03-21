# Вариант #3

Выполнить задание согласно макету автора *Vladislav Chernov*: **[Online Zoo](https://www.figma.com/file/74wXlorl9mZQP0uhqDg83j/Online-Zoo)**


## Создание макета: неделя #1+2

Выполняется создание всех страниц для ширины экрана **1920px**.


### Технические требования

Максимальный балл: **80**


#### Общие

Все фоновые элементы макета должны растягиваться на всю доступную ширину экрана, если ширина больше 1920px. При этом направляющие должны сохраняться в исходном размере, 1400px. Особенностью этого проекта яляется дизайн, в котором изначально размеры учитывают необходимые отступы при скролле, или манипуляциях. При этом важно, что ни в коем случае, на странице не должна появляться горизонтальная полоса прокрутки. О таких случаях будет сказано в технических требованиях соотвествующих блоков.

Для создания вертикальных отступов лучше использовать вертикальные margin на блоках высшего порядка, насколько это возможно. При этом иметь ввиду, что вертикальные margin могут схлопнуться.

Для создание многоколоночных структур, или элементов имеющих относительное горизонтальное расположение, должно быть использовано одно из свойств:
- display: flex
- display: grid
- display: inline-block


#### Landing (20 баллов)

1. **Header** (`<header>` содержит только логотип, панель навигации и иконку юзера)
- Логотип находится слева. Нажатие на логотип работает по принципу нажатия на `About`, перебрасывает нас на текущую страницу, на First Page. Landing.
- Интерактивная панель навигации. (About / Map / Zoos / Contact Us / Design)
- Нажатие на `Map` перебрасывает нас на Zoos Map.
- Нажатие на `Zoos` перебрасывает нас на Zoos Translation с пандой.
- Нажатие на `Contact Us` перебрасывает нас на страницу с ошибкой 404.
- Нажатие на `Design` перебрасывает нас на оригинальную страницу [Figma](https://www.figma.com/file/74wXlorl9mZQP0uhqDg83j/Online-Zoo).
- Должен быть подсвечен первый элемент `About`. И он должен перестать быть интерактивным.
- На странице обязательно должен присутствовать один элемент `<h1>`. В нем должен быть текст `Online Zoo`.
- Хедер, за исключением логотипа, "липким" делать не нужно. Т.е. при скролле он остается на своей позиции.

2. **Side bar** (`<aside>` содержит иконку логотипа, кнопку "вверх", кнопки соц. сетей)
- Панель слева: При скролле она должна "прилипнуть" к своей позиции, и всегда оставаться там вплоть до футера [position: fixed](https://developer.mozilla.org/ru/docs/Web/CSS/position#fixed_positioning).
- При нажатии кнопки "вверх" может ничего не происходить.
- Интерактивная панель соцсетей. Нажатия на соцсети могут вести просто на заглавные страницы соотвествующих ресурсов.

3. Блок **Watch your favorite animal online**
- Кнопка `Choose zoo` должна быть интерактивной. Нажатие перебрасывает нас на Zoos Map.
- Кнопка `Watch online` должна быть интерактивной. Нажатие перебрасывает нас на Zoos Translation с пандой.

4. Блок **How zoo online works**
- Кнопка `Try now` должна быть интерактивной. Нажатие перебрасывает нас на Zoos Translation с пандой.
  
5. Блок **Famous pets**
- Кнопки влево и вправо должны быть интерактивными. При нажатии может ничего не происходить.
- Карточки животных должны быть интерактивными. [Пример анимации](https://drive.google.com/drive/folders/1yrzuAEEHFqkZn-4zkrlrYAHbNXdHOpRo), который также можно посмотреть во вкладке Components.

6. Блок **Pay and feed**
- (3) Заголовки, текст, картинки, стрелки - это все разные элементы.

7. Блок **Testimonials**
- Кнопка `Leave Feedback` должна быть интерактивной. При нажатии может ничего не происходить.
- Кнопка `See more reviews` должна быть интерактивной. При нажатии может ничего не происходить.
- Кнопки влево и вправо должны быть интерактивными. При нажатии может ничего не происходить.

8. Блок **Zoogeography**
- На карте должно быть 4 интерактивных иконки. При наведении должна быть анимация, когда элемент увеличивается и граница меняет цвет. При нажатии может ничего не происходить.
- По умолчанию выбран Eagle, панель слева показывает описание. Описание может не меняться.
- Кнопка `Watch now` перебрасывает нас на Zoos Translation с соотвествующим животным. В случае с орлом - на страницу орла.

9. **Footer** (`<footer>` содержит меню, доготипы, кнопки доната и соц. сетей):
- Интерактивная панель навигации. По умолчанию, элементы не имеют подсветки. Каждая ссылка - это [якорь](https://webref.ru/course/html-tutorial/anchor), по нажатию на который нас перебрасывает на нужное место на странице:  
-- Watch online  
-- How it works  
-- Famous pets  
-- Pay & feed  
-- Testimonials  
-- Zoogeography  
- Кнопка `Donate for volunteers` должна быть интерактивной. При нажатии может ничего не происходить.
- Нажатие на основной логотип работает по принципу нажатия на About, перебрасывает нас на текущую страницу, на Landing.
- Остальные Логотипы не интерактивные. Они не должны реагировать на нажатие. Но должен появлятся тултип (атрибут title) с соотвествующей надписью (Yem Digital, Rolling Scopes School).
- Интерактивная панель соцсетей. Нажатия на соцсети могут вести просто на заглавные страницы соотвествующих ресурсов.


#### Zoos Map (20 баллов)

1. **Header** (`<header>` содержит только логотип, панель навигации и иконку юзера)
- Логотип находится слева. Нажатие на логотип работает по принципу нажатия на `About`, перебрасывает нас на текущую страницу, на First Page. Landing.
- Интерактивная панель навигации. (About / Map / Zoos / Contact Us / Design)
- Нажатие на `About` перебрасывает нас на Landing.
- Нажатие на `Zoos` перебрасывает нас на Zoos Translation с пандой.
- Нажатие на `Contact Us` перебрасывает нас на страницу с ошибкой 404.
- Нажатие на `Design` перебрасывает нас на оригинальную страницу [Figma](https://www.figma.com/file/74wXlorl9mZQP0uhqDg83j/Online-Zoo).
- Должен быть подсвечен элемент `Map`. И он должен перестать быть интерактивным.
- На странице обязательно должен присутствовать один элемент `<h1>`. В нем должен быть текст `Online Zoo`.
- Хедер, за исключением логотипа, "липким" делать не нужно. Т.е. при скролле он остается на своей позиции.

2. **Side bar** (`<aside>` содержит иконку логотипа, кнопки животных и стрелки)
- Панель слева: Всегда будет в одной позиции, можно не делать "липкой".
- Интерактивная панель с животными. Нажатия на животных могут вести просто на заглавные страницы соотвествующих ресурсов.
- Стрелки вверх и вниз должны быть интерактивными. При нажатии может ничего не происходить.

3. Блок **Map**
- Иконки животных должны занимать свою позицию относительно карты.
- При наведении должна быть анимация, когда элемент увеличивается и граница меняет цвет. При нажатии может ничего не происходить.
- Карту можно зафиксировать в положении, как на дизайне. Главное, масштаб картинки должен соотвествовать такому же, как на дизайне.
- Не должно быть быть ни вертикального, ни горизонтального скролла.


#### Zoos Translation (10 x 4 = 40 баллов)
Требования для типовой страницы. Переход осуществляется по ссылкам типа `.../zoos/panda` или `.../zoos/gorilla`

1. **Header** (`<header>` содержит только логотип, панель навигации и иконки соц. сетей)
- Логотип находится слева. Нажатие на логотип работает по принципу нажатия на `About`, перебрасывает нас на текущую страницу, на First Page. Landing.
- Интерактивная панель навигации. (About / Map / Zoos / Contact Us / Design)
- Нажатие на `About` перебрасывает нас на Landing.
- Нажатие на `Map` перебрасывает нас на Zoos Map.
- Нажатие на `Contact Us` перебрасывает нас на страницу с ошибкой 404.
- Нажатие на `Design` перебрасывает нас на оригинальную страницу [Figma](https://www.figma.com/file/74wXlorl9mZQP0uhqDg83j/Online-Zoo).
- Должен быть подсвечен элемент `Zoos`. И он должен перестать быть интерактивным.
- На странице обязательно должен присутствовать один элемент `<h1>`. В нем должен быть текст `Online Zoo`.
- Хедер, за исключением логотипа, "липким" делать не нужно. Т.е. при скролле он остается на своей позиции.

2. **Side bar** (`<aside>` содержит иконку логотипа, кнопки животных, вопросительный знак и стрелки)
- Панель слева: При скролле она должна "прилипнуть" к своей позиции, и всегда оставаться там вплоть до футера [position: fixed](https://developer.mozilla.org/ru/docs/Web/CSS/position#fixed_positioning).
- Интерактивная панель с кнопками животных. Нажатие перебрасывает нас на Zoos Translation с соотвествующим животным.
- При нажатии на "?" может ничего не происходить.
- Стрелки вверх и вниз должны быть интерактивными. При нажатии может ничего не происходить.

3. Блок **Main cam**
- В кнопке `Feed the animal` вместо animal должно быть название животного.
- Кнопка `Feed the animal` должна быть интерактивной. При нажатии может ничего не происходить.
- Блок видео - это элемент `iframe` с видео трансляции, его можно добавить на страницу по [инструкции](https://support.google.com/youtube/answer/171780?hl=ru).
- Кнопки влево и вправо должны быть интерактивными.
- Картинки в карусели - это должны быть либо превью с youtube, либо такие же `iframe` с видео.

4. Блок **Other cams**
- Картинки в карусели - это должны быть либо превью с youtube, либо такие же `iframe` с видео.
- При наведении на элемент видео, поверх должен появляться текст и затемняться картинка снизу. Такого эффекта можно достичь наложив полностью прозрачный элемент сверху, который не даст нажать видео, и ничего не произойдет. Эта заглушка нужна будет при работе с js.
- Кнопки со стрелками должны быть интерактивными. При нажатии может ничего не происходить.

5. Блок **Interesting facts**
- (3) Если панели будут закрыты, и не смогут открыться - это будет считаться ошибкой. При этом выпадающие панели с информацией могут быть полностью раскрыты на момент выполнения недели#1-3, это не ошибка.
- Когда панель раскрыта, то на заголовке появляется "-" (будет везде в случае, если панели просто будут раскрыты). В случае закрытой панели, будет "+".
- Ссылки в тексте будут перебрасывать нас на соотвествующий ресурс.

6. Блок **Pay and feed**
- (3) Заголовки, текст, картинки, стрелки - это все разные элементы.

7. **Footer** (`<footer>` содержит меню, доготипы, кнопки доната и соц. сетей):
- (3) Интерактивная панель навигации. По умолчанию, элементы не имеют подсветки. Каждая ссылка - это [якорь](https://webref.ru/course/html-tutorial/anchor), по нажатию на который нас перебрасывает на нужное место на странице **Landing**:  
-- Watch online  
-- How it works  
-- Famous pets  
-- Pay & feed  
-- Testimonials  
-- Zoogeography  
- Кнопка `Donate for volunteers` должна быть интерактивной. При нажатии может ничего не происходить.
- Нажатие на основной логотип работает по принципу нажатия на About, перебрасывает нас на текущую страницу, на Landing.
- Остальные Логотипы не интерактивные. Они не должны реагировать на нажатие. Но должен появлятся тултип (атрибут title) с соотвествующей надписью (Yem Digital, Rolling Scopes School).
- Интерактивная панель соцсетей. Нажатия на соцсети могут вести просто на заглавные страницы соотвествующих ресурсов.

#### (3) [404 Error](https://www.figma.com/file/74wXlorl9mZQP0uhqDg83j/Online-Zoo?node-id=433%3A75) (10 баллов)

1. **Header** (`<header>` содержит только логотип, панель навигации и иконки соц. сетей)
- Логотип находится слева. Нажатие на логотип работает по принципу нажатия на `About`, перебрасывает нас на текущую страницу, на First Page. Landing.
- Интерактивная панель навигации. (About / Map / Zoos / Contact Us / Design)
- Нажатие на `About` перебрасывает нас на Landing.
- Нажатие на `Map` перебрасывает нас на Zoos Map.
- Нажатие на `Zoos` перебрасывает нас на Zoos Translation с пандой.
- Нажатие на `Design` перебрасывает нас на оригинальную страницу [Figma](https://www.figma.com/file/74wXlorl9mZQP0uhqDg83j/Online-Zoo).
- Должен быть подсвечен элемент `Contact Us`. И он должен перестать быть интерактивным.
- На странице обязательно должен присутствовать один элемент `<h1>`. В нем должен быть текст `Online Zoo`.
- Хедер, за исключением логотипа, "липким" делать не нужно. Т.е. при скролле он остается на своей позиции.

2. Блок **Oops**
- (3) Кнопка `Back to main page` должна быть интерактивной. Нажатие перебрасывает нас на Landing.
- Поля (input, textarea), помеченные звездочкой, должны быть обязательными для заполнения, т.е. required. Если при нажатии на кнопку `send message` хоть одно поле не проходит валидацию, запрос не должен быть отправлен.
- Подсвеченная ссылка `click here to go to support` должна иметь интерактивность ссылки, но не должна никуда вести, т.к. мы уже на нужной странице.

3. **Footer** (`<footer>` содержит меню, доготипы, кнопки доната и соц. сетей):
- (3) Интерактивная панель навигации. По умолчанию, элементы не имеют подсветки. Каждая ссылка - это [якорь](https://webref.ru/course/html-tutorial/anchor), по нажатию на который нас перебрасывает на нужное место на странице **Landing**:  
-- Watch online  
-- How it works  
-- Famous pets  
-- Pay & feed  
-- Testimonials  
-- Zoogeography  
- Кнопка `Donate for volunteers` должна быть интерактивной. При нажатии может ничего не происходить.
- Нажатие на основной логотип работает по принципу нажатия на About, перебрасывает нас на текущую страницу, на Landing.
- Остальные Логотипы не интерактивные. Они не должны реагировать на нажатие. Но должен появлятся тултип (атрибут title) с соотвествующей надписью (Yem Digital, Rolling Scopes School).
- Интерактивная панель соцсетей. Нажатия на соцсети могут вести просто на заглавные страницы соотвествующих ресурсов.


## Адаптивность: неделя #3

Сверстанные страницы адаптируюятся под следующую ширину экрана устройства:
- 1920px (уже будет готово)
- 1200px
- 640px
- 320px

### Технические требования

Максимальный балл: **40**

🚧 Задание в процессе разработки 🚧


## Функционалная часть и пользовательские события: неделя #4-5

Добавление JavaScript.

### Технические требования

Максимальный балл: **80**

🚧 Задание в процессе разработки 🚧