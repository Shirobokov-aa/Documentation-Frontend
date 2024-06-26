# Документация для frontend разработчиков

## 1. [BEM](https://ru.bem.info/methodology/)

    При верстке используем смешаный формат стилей именования Two Dashes и CamelCase, например,

```html
<b>bigBlock__bigElement--bigModificator</b>
```

    Ниже приведены рекомандации для блоков, которые чаще всего есть на любом сайте, которые необоходимо придерживаться.

**Базовый каркас для верстки**

```html
<div class="wrapper">
  <header class="header"></header>
  <main class="main">
    <b
      >Дополнительные обертки добавляются строго в этой области (Пример ниже)</b
    >
  </main>
  <footer class="footer"></footer>
</div>
```

**Базовый каркас для внутренних страниц**

```html
<div class="wrapper">
  <header class="header"></header>
  <main class="main">
    <div class="insidePage">
      <div class="insidePage__sidebar insidePage__sidebar--left"></div>
      <div class="insidePage__mainContent">Основная рабочая область</div>
      <div class="insidePage__sidebar insidePage__sidebar--right"></div>
    </div>
  </main>
  <footer class="footer"></footer>
</div>
```

**Хлебные крошки**

```html
<nav class="breadcrumb" aria-label="Breadcrumb">
  <ul class="breadcrumb__list">
    <li class="breadcrumb__item">
      <a class="breadcrumb__link" href="#">Home</a>
    </li>
    <li class="breadcrumb__item">
      <a class="breadcrumb__link" href="#">About</a>
    </li>
    <li class="breadcrumb__item">
      <a
        class="breadcrumb__link breadcrumb__link--last"
        href="#"
        aria-current="location"
        >Vision</a
      >
    </li>
  </ul>
</nav>
Или
<div class="breadcrumb" aria-label="Breadcrumb">
  <div class="breadcrumb__container container">
    <nav class="breadcrumb__nav">
      <ul class="breadcrumb__list">
        <li class="breadcrumb__item">
          <a class="breadcrumb__link" href="#">Home</a>
        </li>
        <li class="breadcrumb__item">
          <a class="breadcrumb__link" href="#">About</a>
        </li>
        <li class="breadcrumb__item">
          <a
            class="breadcrumb__link breadcrumb__link--last"
            href="#"
            aria-current="location"
            >Vision</a
          >
        </li>
      </ul>
    </nav>
  </div>
</div>
```

**Кнопки**
В зависимости от сложности макетов испольузются такие модификаторы как
--size
--color

```html
<a href="#" class="button button--red button--sizeBig">
  <span class="button__prependIcon"> 🚀 </span>
  <span class="button__text">Текст ссылки или кнопки</span>
  <span class="button__appendIcon"> 👨‍🚀 </span>
</a>
```

**Превью карточки товара**

```html
<div class="previewItem">
  <div class="previewItem__imageContainer">
    <picture class="previewItem__picture">
      <img src="src" alt="" class="previewItem__image" />
    </picture>
  </div>
  <div class="previewItem__body">
    <div class="previewItem__name"></div>
    <div class="previewItem__desc"></div>
    <a href="#" class="previewItem__button button"></a>
  </div>
</div>
```

**Пример тизеров**

```html
<div class="tizers">
  <div class="tizers__container container">
    <div class="tizers__row row">
      <div class="tizers__itemContainer tizers__itemContainer--w33">
        <div class="tizersItem">
          <div class="tizersItem__iconContainer">
            <img src="icon" alt="" class="tizersItem__icon" />
          </div>
          <div class="tizersItem__desc"></div>
        </div>
      </div>
      <div class="tizers__itemContainer tizers__itemContainer--w33">
        <div class="tizersItem">
          <div class="tizersItem__iconContainer">
            <img src="icon" alt="" class="tizersItem__icon" />
          </div>
          <div class="tizersItem__desc"></div>
        </div>
      </div>
      <div class="tizers__itemContainer tizers__itemContainer--w33">
        <div class="tizersItem">
          <div class="tizersItem__iconContainer">
            <img src="icon" alt="" class="tizersItem__icon" />
          </div>
          <div class="tizersItem__desc"></div>
        </div>
      </div>
    </div>
  </div>
</div>
```

**Детальная карточка товара**

```html
<div class="cardProduct">
  <div class="cardProduct__row">
    <div class="cardProduct__sideBar">
      <div class="cardProduct__gallery gallery">
        <div class="gallery__sliderContainer">
          <div class="gallery__slide">
            <a href="#" data-fancybox class="gallery__link">
              <picture class="gallery__picture">
                <img class="gallery__image" src="src" alt="" />
              </picture>
            </a>
          </div>
          <div class="gallery__slide">
            <a href="#" data-fancybox class="gallery__link">
              <picture class="gallery__picture">
                <img class="gallery__image" src="src" alt="" />
              </picture>
            </a>
          </div>
          <div class="gallery__slide">
            <a href="#" data-fancybox class="gallery__link">
              <picture class="gallery__picture">
                <img class="gallery__image" src="src" alt="" />
              </picture>
            </a>
          </div>
        </div>
      </div>
    </div>
    <div class="cardProduct__content">
      <div class="cardProduct__rating rating"></div>
      <div class="cardProduct__title"></div>
      <div class="cardProduct__desc"></div>
      <button class="cardProduct__button button--addToCart"></button>
    </div>
  </div>
</div>
```

**Чекбокс или радиокнопка**

```html
<label class="checkbox">
  <input class="checkbox__input" type="checkbox" id="MyCustomCheckbox" />
  <svg
    class="checkbox__icon"
    xmlns="http://www.w3.org/2000/svg"
    viewBox="0 0 22 22"
  >
    <rect
      width="21"
      height="21"
      x=".5"
      y=".5"
      fill="#FFF"
      stroke="#006F94"
      rx="3"
    />
    <path
      class="tick"
      stroke="#6EA340"
      fill="none"
      stroke-linecap="round"
      stroke-width="4"
      d="M4 10l5 5 9-9"
    ></path>
  </svg>
  <span class="checkbox__label">Описание</span>
</label>
```

**Шапка**

```
  <header class="header">
        <div class="header__top">
            <div class="header__container">
                <div class="header__row">
                    <div class="header__mainMenu mainMenu">
                        <nav class="mainMenu__nav">
                            <ul class="mainMenu__list">
                                <li class="mainMenu__item">
                                    <a href="#" class="mainMenu__link"></a>
                                </li>
                                <li class="mainMenu__item">
                                    <a href="#" class="mainMenu__link"></a>
                                </li>
                                <li class="mainMenu__item">
                                    <a href="#" class="mainMenu__link"></a>
                                </li>
                                <li class="mainMenu__item">
                                    <a href="#" class="mainMenu__link"></a>
                                </li>
                                <li class="mainMenu__item">
                                    <a href="#" class="mainMenu__link"></a>
                                </li>
                                <li class="mainMenu__item">
                                    <a href="#" class="mainMenu__link"></a>
                                </li>
                            </ul>
                        </nav>
                    </div>
                    <div class="header__buttons">
                        <button class="header__button">
                            <img src="" alt="" class="header__icon">
                        </button>
                    </div>
                    <div class="header__links">
                        <a href="#" class="header__link"></a>
                        <a href="#" class="header__link"></a>
                        <a href="#" class="header__link"></a>
                    </div>
                </div>
            </div>
        </div>
        <div class="header__bottom">
           <div class="container">
                <div class="header__row">
                    <a href="/" class="header__logo logo">
                        <img class="logo__images" src="" alt="">
                    </a>
                    <div class="header__search search">
                            <div class="search__wrap">
                                <div class="search__inputContainer">
                                    <input type="text" class="search__input">
                                    <button class="search__button">
                                        <img class="search__buttonIcon" src="" alt="">
                                    </button>
                                </div>
                                <div class="search__dropdown">
                                    <div class="search__item">
                                        <a href="#" class="search__itemLink"></a>
                                    </div>
                                    <div class="search__item">
                                        <a href="#" class="search__itemLink"></a>
                                    </div>
                                    <div class="search__showmoreContainer">
                                        <a href="#" class="search__showMore"></a>
                                    </div>
                                </div>
                            </div>
                    </div>
                </div>
           </div>
        </div>
    </header>
```

**Часто используемые классы**

**_Блоки_**

page — корневой элемент страницы

header — шапка (страницы или элемента)

footer — подвал (страницы или элемента)

section — раздел контента (один из нескольких)

body — основная часть (страницы или элемента)

content — содержимое элемента

sidebar — боковая колонка (страницы или элемента)

aside — блок с дополнительной информацией

widget — виджет, например, в боковой колонке

**_Раскладка_**

wrapper, wrap — обёртка, обычно внешняя

inner — внутренняя обёртка

container, holder, box — контейнер

grid — раскладка (страницы или элемента) в виде сетки (обычно содержит в себе row и col)

row — контейнер в виде строки

col, column — контейнер в виде столбца

**_Текст_**

title, subject, heading, headline, caption — заголовок

subtitle — подзаголовок

slogan — слоган

lead, tagline — лид-абзац в тексте

text — текстовый контент

desc — описание, вариант текстового контента

excerpt — отрывок текста, обычно используется перед ссылкой «Читать далее…»

copyright, copy — копирайт

**_Ссылки, кнопки_**

link — ссылка

button, btn — кнопка, например, для отправки формы

**_Списки_**

list, items — список

item — элемент списка

**_Изображения_**

image, img, picture, pic — картинка

icon — иконка

logo — логотип

userpic, avatar — юзерпик, маленькая картинка пользователя

thumbnail, thumb — миниатюра, уменьшенное изображение

**_Элементы управления_**

control — элемент управления, например, стрелки «Вперёд/назад» в фотогалерее, кнопки управления слайдером

dropdown — выпадающий список

search — поиск

slider, carousel — слайдер, интерактивный элемент с прокруткой содержимого

pagination — постраничная навигация

bullet — переключатели в пагинации

modal — модальное (диалоговое) окно

popup — всплывающее окно

tooltip, tip — всплывающие подсказки

preview — анонс, отрывок, например новости или поста, может состоять из заголовка, описания и картинки. Предполагается ссылка на полную версию

breadcrumbs — навигационная цепочка, «хлебные крошки»

**_Медиавыражения_**

phone, mobile — мобильные устройства

phablet — телефоны с большим экраном (6-7″)

tablet — планшеты

notebook, laptop — ноутбуки

desktop — настольные компьютеры

**_Размеры_**

tiny, xs — маленький, крохотный

small, sm — небольшой

medium, md — средний

big, large, lg — большой

huge, xl — огромный

narrow — узкий

wide — широкий

**_Состояния_**

active, current — активный элемент, например, текущий пункт меню

hidden — скрытый элемент

error — статус ошибки

warning — статус предупреждения

success — статус успешного выполнения задачи

pending — состояние ожидания, например, перед сменой статуса на error или success

**_Дополнительно_**

socials — блок иконок соцсетей

advertisement, adv, commercial, promo — рекламный блок (режутся Адблоком, не рекомендуется использовать такие классы для блоков с внутренней рекламой)

features, benefits — список основных особенностей товара, услуги

user, author — пользователь, автор записи или комментария

meta — блок с дополнительной информацией, например, блок тегов и даты в посте

cart, basket — корзина

more, all — ссылка на полную информацию

## 2. Стек плагинов

- [Слайдер - swiper.js](https://swiperjs.com/)
- [Маска в инпуты](https://imask.js.org/)
- [Анимация GSAP](https://greensock.com/gsap/)
- [Тригер на скролл для анимации GSAP (Если требуется анимация плавающих элементов на мобильных устройствах)](https://scrollmagic.io/)
- [Умный скролл для мобильных устройств, необходимый для более плавной анимации](https://github.com/cubiq/iscroll)

## 3. Сборка для проектов

Gulp - сборка MaxGraph

> Используется Gulp 4
> Для работы с данной сборкой в новом проекте, склонируйте все содержимое репозитория <br>
> `git clone <this repo>`
> Затем, находясь в корне проекта, запустите команду `npm i`, которая установит все находящиеся в package.json зависимости.
> После этого вы можете использовать любую из предложенных команд сборки (итоговые файлы попадают в папку **app** корневой директории): <br>
> `gulp` - базовая команда, которая запускает сборку для разработки, используя browser-sync

`gulp build` - команда для продакшн-сборки проекта. Все ассеты сжаты и оптимизированы для выкладки на хостинг.

`gulp cache` - команда, которую стоит запускать после `gulp build`, если вам нужно загрузить новые файлы на хостинг без кэширования.

`gulp backend` - команда для бэкенд-сборки проекта. Она лишена ненужных вещей из dev-сборки, но не сжата, для удобства бэкендера.

`gulp zip` - команда собирает ваш готовый код в zip-архив.

## Структура папок и файлов

```
├── src/                          # Исходники
│   ├── js                        # Скрипты
│   │   └── main.js               # Главный скрипт
│   │   ├── _vars.js              # файл с переменными проекта
│   │   ├── _vendor.js            # файл с подключениями библиотек
│   │   ├── _functions.js         # файл с готовыми функциями на js
│   │   ├── _components.js        # файл с подключениями компонентов
│   │   ├── components            # js-компоненты
│   │   ├── vendor                # папка для загрузки локальных версий библиотек
│   ├── scss                      # Стили сайта (препроцессор sass в scss-синтаксисе)
│   │   └── main.scss             # Главный файл стилей
│   │   └── vendor.scss           # Файл для подключения стилей библиотек из папки vendor
│   │   └── _fonts.scss           # Файл для подключения шрифтов (можно использовать миксин)
│   │   └── _mixins.scss          # Файл для подключения миксинов из папки mixins
│   │   └── _vars.scss            # Файл для написания css- или scss-переменных
│   │   └── _settings.scss        # Файл для написания глобальных стилей
│   │   ├── components            # scss-компоненты
│   │   ├── mixins                # папка для сохранения готовых scss-компонентов
│   │   ├── vendor                # папка для хранения локальных css-стилей библиотек
│   ├── partials                  # папка для хранения html-частей страницы
│   ├── img                       # папка для хранения картинок
│   │   ├── svg                   # специальная папка для преобразования svg в спрайт
│   ├── resources                 # папка для хранения иных ассетов - php, видео-файлы, favicon и т.д.
│   │   ├── fonts                 # папка для хранения шрифтов в формате woff2
│   └── index.html                # Главный html-файл
└── gulpfile.js                   # файл с настройками Gulp
└── package.json                  # файл с настройками сборки и установленными пакетами
└── .editorconfig                 # файл с настройками форматирования кода
└── .ecrc                         # файл с настройками пакета editorconfig-checker (исключает ненужные папки)
└── .stylelintrc                  # файл с настройками stylelint
└── README.md                     # документация сборки
```

1. [npm-скрипты](#npm-скрипты)
2. [Работа с html](#работа-с-html)
3. [Работа с CSS](#работа-с-css)
4. [Работа с JavaScript](#работа-с-javascript)
5. [Работа со шрифтами](#работа-со-шрифтами)
6. [Работа с изображениями](#работа-с-изображениями)
7. [Работа с иными ресурсами](#работа-с-иными-ресурсами)
8. [Типограф](#типограф)
9. [Рекомендуемые плагины VS Code](#рекомендуемые-плагины-для-vs-code)
10. [Локальные сниппеты](#локальные-сниппеты)
11. [Готовые модули](#готовые-модули)

## npm-скрипты

Вы можете вызывать gulp-скрипты через npm.
Также в сборке есть возможность проверять код на соответствие конфигу (editorconfig) и валидировать html.

`npm run html` - запускает валидатор html, запускать нужно при наличии html-файлов в папке **app**.

`npm run code` - запускает editorconfig-checker для проверки соответствия конфиг-файлу.

## Работа с html

Благодаря плагину **gulp-file-include** вы можете разделять html-файл на различные шаблоны, которые должны храниться в папке **partials**. Удобно делить html-страницу на секции.

> Для вставки html-частей в главный файл используйте `@include('partials/filename.html')`

Если вы хотите создать многостраничный сайт - копируйте **index.html**, переименовывайте как вам нужно, и используйте.

При использовании команды `gulp build`, вы получите минифицированный html-код в одну строку для всех html-файлов.

## Работа с CSS

В сборке используется препроцессор **sass** в синтаксисе **scss**.

Стили, написанные в **components**, следует подключать в **main.scss**.
**ВАЖНО:** Обязательно удалить стили, которые написаны в **main.scss** для `.page__body`.

Чтобы подключить сторонние css-файлы (библиотеки) - положите их в папку **vendor** и подключите в файле **\_vendor.scss**

Если вы хотите создать свой миксин - делайте это в папке **mixins**, а затем подключайте в файл **\_mixins.scss**.

Если вы хотите использовать scss-переменные - подключите **\_vars.scss** также в main.scss или в любое другое место, где он нужен, но обязательно удалите **:root**.

> Для подключения css-файлов используйте директиву `@import`

В итоговой папке **app/css** создаются два файла: <br> **main.css** - для стилей страницы, <br> **vendor.css** - для стилей всех библиотек, использующихся в проекте.

При использовании команды `gulp build`, вы получите минифицированный css-код в одну строку для всех css-файлов.

## Работа с JavaScript

Для сборки JS-кода используется webpack.

JS-код лучше делить на компоненты - небольшие js-файлы, которые содержат свою, изолированную друг от друга реализацию. Такие файлы помещайте в папку **components**, а потом импортируйте в файл **\_components.js**

В файле **vars.js** должны храниться базовые переменные проекта, вроде нахождения элементов и т.д.

В файле **main.js** ничего менять не нужно, он сделан просто как результирующий.

Подключать сторонние библиотеки можно через npm, для этого существует файл **\_vendor.js**. Импортируйте туда подключения.

Если какой-то библиотеки нет в npm или просто нужно подключить что-либо локальным файлом - кладите его в папку **vendor** и точно так же импортируйте, но уже с путем до файла.

При использовании команды `gulp build`, вы получите минифицированный js-код в одну строку для всех js-файлов.

## Работа со шрифтами

Т.к. автор не поддерживает IE11, в сборке реализована поддержка только формата **woff2** (это значит, что в миксине подключения шрифтов используется только данный формат).

Загружайте файлы **woff2** в папку **resources/fonts**, а затем вызывайте миксин `@font-face` в файле **\_fonts.scss**.

Также не забудьте прописать эти же шрифты в `<link preload>` в html.

## Работа с изображениями

Любые изображения, кроме **favicon** кладите в папку **img**.

Если вам нужно сделать svg-спрайт, кладите нужные для спрайта svg-файлы в папку **img/svg**. При этом, такие атрибуты как fill, stroke, style будут автоматически удаляться. Иные svg-файлы просто оставляйте в папке **img**.

При использовании команды `gulp build`, вы получите минифицированные изображения в итоговой папке **img**.

В сборке доступна поддержка **webp** и **avif** форматов. Подключить их вы можете через тег `picture`. Для background можно использовать обычные **jpg** или **png**, либо использовать `image-set` там, где это возможно.

## Работа с иными ресурсами

Любые ресурсы (ассеты) проекта, под которые не отведена соответствующая папка, должны храниться в папке **resources**. Это могут быть видео-файлы, php-файлы (как, например, файл отправки формы), favicon и прочие.

## Типограф

Для корректного отображения текста на странице был подключен плагин типограф, которые автоматически добавит неразрывные пробелы и иные символы, чтобы текст везде отображался по всем правилам русского языка.

## Рекомендуемые плагины для VS Code

Я рекомендую использовать именно VS Code, и в сборке реализовано взаимодействие именно с этим редактором. Так, при открытии папки со сборкой в VS Code, редактор предложит вам ранее не установленные плагины, которые подойдут для корректной работы сборки.

Самый важный из них – **projects snippets**, этот плагин "включает" локально написанные сниппеты для сборки.

## Локальные сниппеты

Для удобства и быстроты разработки были добавление локальные сниппеты (находятся в папке .vscode/snippets), которые работают благодаря плагину, описанному выше. Все сниппеты начинаются с префикса **g-**. В сниппетах пока только html (быстрое создание навигации, соцсетей, корректного тега picture с webp и avif и так далее).

Некоторые сниппеты тесно связаны с scss-миксинами, например кнопка-бургер. Сниппет **g-burger** создаст вам html-разметку бургера, а подключение миксина **@include burger** добавит для него стили, что крайне удобно.

Полный список сниппетов с поддержкой миксинов будет опубликован позже.

## Готовые модули

В сборку постепенно добавляются готовые, часто-используемые модули под различные задачи. Ниже будет перечислен уже добавленный функционал.

**Внимание!** В файле _functions.js_ описаны лишь подключения всех нужных модулей. Рекомендуется использовать все это в отдельных файлах. Например, если вам нужно создать модальное окно, создаете файл _modal.js_ в папке components, подключаете его в файл components.js и уже в файле _modal.js_ используете код подключения.

### Бургер меню

Вы можете очень быстро добавить рабочий бургер к себе на страницу, для этого нужно:

1. В html вызвать сниппет `g-burger`
2. На ваше потенциальное меню в html добавить атрибут `data-menu`
3. В scss вызвать миксин `burger`

```
.burger { @include burger }
```

4. Зайти в файл js/\_functions.js и раскомментировать строку с подключением js-файла бургера
5. Настроить стили показа меню под себя с помощью класса `menu--active`

### Модальное окно

Вы можете очень быстро добавить рабочее модальное окно к себе на страницу, для этого нужно:

1. В html вызвать сниппет `g-graph-btn`. Он создаст кнопку для модального окна, ваша задача лишь заполнить атрибут `data-graph-path`
2. Далее вызвать сниппет `g-graph-modal`. Он создаст базовую разметку окна. Ваша задача - сделать окно по макету, заполнить контент и обязательно обозначить атрибут `data-graph-target` с тем же значением, что и у `data-graph-path`
3. Зайти в файл vendor.scss и раскомментировать строку с подключением файла graph-modal.min.css
4. Зайти в файл js/\_functions.js и раскомментировать строку с импортом и подключением библиотеки `GraphModal`

### Управление скроллом

Вы можете отключать\включать скролл на странице (работает даже на iPhone). Для этого нужно:

1. Зайти в файл js/\_functions.js и раскомментировать строку с импортом функций `disableScroll`, `enableScroll`.
   **Важно!**. Если на странице присутствуют блоки с фиксированным позиционированием (например, шапка), добавьте ей класс `fixed-block`, чтобы этот блок не прыгал при отключении скролла.

Необязательно использовать функции именно в файле **functions**, делайте как удобно вам.

### Табы

Вы можете очень быстро добавить рабочие табы к себе на страницу, для этого нужно:

1. В html вызвать сниппет `g-tabs`. Он создаст разметку для табов, ваша задача лишь заполнить атрибут `data-tabs`
2. Для класса `.tabs` вызвать миксин `tabs` в scss (или же использовать подключение скрипта библиотеки из npm в файле vendor.scss)
3. Зайти в файл js/\_functions.js и раскомментировать строку с импортом и подключением библиотеки `GraphTabs`

### Валидация и отправка данных на почту

Вы можете быстро настроить валидацию и отправку данных на почту (пока работает в тестовом режиме). Как это использовать:

1. Создать форму, указав у нее уникальный класс. Также указать уникальные классы для полей ввода.
2. Создать массив, в котором будут переданы правила плагина <a href="https://github.com/horprogs/Just-validate" target="_blank">just-validate</a>, например:

```
const rules1 = [
  {
    ruleSelector: '.input-name',
    rules: [
      {
        rule: 'minLength',
        value: 3
      },
      {
        rule: 'required',
        value: true,
        errorMessage: 'Заполните имя!'
      }
    ]
  },
  {
    ruleSelector: '.input-tel',
    tel: true,
    telError: 'Введите корректный телефон',
    rules: [
      {
        rule: 'required',
        value: true,
        errorMessage: 'Заполните телефон!'
      }
    ]
  },
];
```

**ВАЖНО**. Если в вашей форме есть поле с телефоном, обязательно пропишите в массиве с правилами новые поля: `tel: true, telError: 'Ошибка при вводе телефона'`. 3. Подключить функцию `validateForms`, она находится в _functions.js_, передав туда три параметра:
3.1. Строку с классом формы
3.2. Массив правил
3.3. Если нужно, можно создать свою функцию, которая выполнится после отправки, тогда ее тоже нужно будет передать как аргумент функции `validateForms`.

Пример кода:

```
import { validateForms } from './functions/validate-forms';
const rules1 = [
  {
    ruleSelector: '.input-name',
    rules: [
      {
        rule: 'minLength',
        value: 3
      },
      {
        rule: 'required',
        value: true,
        errorMessage: 'Заполните имя!'
      }
    ]
  },
  {
    ruleSelector: '.input-tel',
    tel: true,
    telError: 'Введите корректный телефон',
    rules: [
      {
        rule: 'required',
        value: true,
        errorMessage: 'Заполните телефон!'
      }
    ]
  },
];

const afterForm = () => {
  console.log('Произошла отправка, тут можно писать любые действия');
};

validateForms('.form-1', rules1, afterForm);
```

### Throttle-функция

Чтобы сгладить управление частоиспользуемыми событиями, вы можете использовать готовую функцию **throttle**. Для этого нужно:

1. В нужном месте импортировать функцию **throttle()**
2. Написать нужную вам функцию, например, **func()**
3. Создать переменную, в которую поместить вызов вашей фукнции внутри throttle, например: `let f = throttle(func)`
4. Использовать эту переменную как функцию в вызове, например: `window.addEventListener('resize', f)`

### Фикс фулскрин блоков

Нередко блоки с высотой 100vh вызывают проблемы в мобильных браузерах. Решить это поможет готовый модуль fix-fullheight:

1. Раскомментируйте строку с импортом файла **fix-fullheight.js**
2. Назначьте на нужный вам блок высоту не 100vh, а `var(--vh)`

Для этой функции используется ранее упомянутый throttle. Вы можете убрать его, либо изменить время внутри файла **fix-fullheight.js**.

### Получение высоты шапки

Иногда требуется получить точную высоту шапки, если она сделана абсолютным или фиксированным позиционированием, и для этого есть функция `getHeaderHeght`. Как ее использовать:

1. Раскомментируйте строку с импортом файла **header-height.js**
2. Используйте css-переменную `--header-height` в нужном вам месте

Необязательно использовать функции именно в файле **functions**, делайте как удобно вам.

### Кастомный скролл

Для реализации кастомного скролла в сборку установлен плагин **simplebar.js**. Как его использовать:

1. Раскомментируйте строку с импортом плагина **simplebar**
2. Добавьте нужному блоку максимальную высоту и атрибут `data-simplebar`

### Функции определения вьюпорта

Вы можете запускать скрипты на определенной ширине (пока что поддержка ресайза не реализована) с помощью готовых функций `isMobile()`, `isTablet()`, `isDesktop()`. Для этого нужно лишь подключить нужную из них из файла, а затем использовать внутри условия `if`.

### Тултипы

Вы можете быстро создать рабочий, доступный тултип, который к тому же будет сам рассчитывать отступы с помощью js. Как это использовать:

1. В html вызвать сниппет `g-tooltip`. Он создаст кнопку для модального окна, ваша задача лишь заполнить атрибуты `aria-describedby` и `id`.
2. Далее нужно подключить тултипы (код в файле _functions.js_), и вместо el передать id или class кнопки тултипа, а вместо tooltip передать id или class самого тултипа.
3. После этого можете стилизовать тултип как вам угодно.

### Слайдер

Вы можете быстро создать рабочий swiper-слайдер. Как это использовать:

1. В html вызвать сниппет `g-swiper`. Он создаст базовую структуру свайпер-слайдера, вам нужно добавить свой класс для свайпер-контейнера.
2. Раскомментировать строку с подключением стилей в файле _vendor.scss_
3. Подключить сам свайпер (код в файле _functions.js_) и использовать его, следуя документации.

### Анимации по скроллу

Вы можете быстро набросать анимаций по скроллу с помощью плагина. Как это использовать:

1. Подключить код библиотеки AOS.js (код в файле _functions.js_) и инициализировать его.
2. С помощью атрибутов из документации плагина вызывать те или иные анимации, или написать свою.

### Параллакс по скроллу

Вы можете быстро набросать параллакс элементов по скроллу с помощью плагина. Как это использовать:

1. Подключить код библиотеки rellax.js (код в файле _functions.js_) и инициализировать его, передав класс элемента (элементов).
2. Задать этот класс нужным элементам, а также использовать атрибуты из документации для кастомизации анимаций.

### Плавный скролл к якорям

Вы можете сделать плавный скролл к якорям, который работает даже в Safari, с помощью плагина. Как это использовать:

1. Подключить код библиотеки smooth-scroll.js (код в файле _functions.js_) и инициализировать его, передав селектор всех якорных ссылок.
2. Раздать всем якорным ссылкам атрибут `data-scroll`.

### Свайпы на мобильных устройствах

Вы можете реализовывать различные взаимодействия со страницей через свайпы на мобильных устройствах с помощью плагина. Как это использовать:

1. Подключить код библиотеки swiped-events.js (код в файле _functions.js_).
2. Использовать различные события из библиотеки плагина.
