# Тестовое задание для стажёра на frontend стажировку (JavaScript)

Требуется реализовать сайт из трех страниц с навигацией между ними, выложить его на GitHub Pages.

Figma (нужно авторизоваться, чтобы видеть информацию об отступах и тд): [Ссылка](https://www.figma.com/file/gZwWzeyH4mUkt72XETyg0p/Web-develop-tasks)

Страницы:

1) Страница пользователя
2) Карта с местом жительства
3) Таймер, показывающий время нахождения пользователя на сайте

Примерный вид сайта (актуальные макеты в Figma):
![Сайт](https://github.com/web-bee-ru/ru-test-assignments/blob/main/files/base-frontend-stages/main.png)

Верстать весь сайт **не нужно**, требуется только верстка блока навигации - верхние две строки

## Первый уровень

- Реализовать блок навигации между страницами сайта. Все три страницы должны содержать этот блок. Ссылка на текущую страницу должна быть выделена.
- Переименовать "Activity" в "Resume" и реализовать страницу "Резюме". Можно использовать свое или чужое, в свободной форме, но оно должно содержать фотографию, контакты и навыки.
- Страницы "Карта" и "Таймер" можно оставить пустыми (кроме блока навигации).
- Выложить сайт на Github Pages (а не просто на Github !!!).

Проверяемые навыки: знание html и css, работа с git

## Второй уровень

- Реализовать все из первого уровня.
- Использовать для оформления всех страниц Bootstrap. Достаточно использовать в паре мест классы `container, row, col`, и может быть `d-flex, mb-2, pb-2, justify-content-between, align-items-center, text-center`.
- Реализовать страницу "Карта". Там должна быть интерактивная карта, с маркером в месте проживания. Пока карта загружается, отображать анимированный прелоадер. Можно использовать карты яндекса, гугла и любые другие. **Запрещается** использовать `<iframe>` карты напрямую в html разметке, предполагается инициализация карты через js.
- Страницу "Таймер" можно оставить пустой (кроме блока навигации).

Примерный вид карты:

- До загрузки:
![До](https://github.com/web-bee-ru/ru-test-assignments/blob/main/files/base-frontend-stages/map_loading.png)

- После загрузки:
![После](https://github.com/web-bee-ru/ru-test-assignments/blob/main/files/base-frontend-stages/map_loaded.png)

Проверяемые навыки: знание javascript, работа со сторонними библиотеками

## Третий уровень

- Реализовать все из первого и второго уровней.
- Переходы между страницами сайта должны происходить без перезагрузки (single page application) \*
- Сайт должен работать в разных браузерах.
- Сайт должен адекватно отображаться на типичных разрешениях экрана (телефон, планшет, десктоп).
- Реализовать страницу "Таймер". Таймер показывает сколько времени посетитель находится на сайте. Таймер не сбрасывается при переходе между страницами, но сбрасывается когда вкладка закрывается и открывается заново.

Примерный вид таймера:
![Таймер](https://github.com/web-bee-ru/ru-test-assignments/blob/main/files/base-frontend-stages/timer.png)

\* Для этого можно использовать history api и обьект с маппингами урла и контента страницы по этому урлу. И повесить обработчики на ссылки с кодом типа такого.
```js
e.preventDefault();
const contentEl = document.querySelector('#content');
contentEl.innerHtml = routes[url];
history.pushState(..., url)
```

Проверяемые навыки: знание javascript

## Четвертый уровень

- При реализации использовать один из MVVM фреймворков: **react**, **vue**, **svelte**, **angular** (*angular* самый **нежелательный**)
- Выложить результат на https://codesandbox.io/
- Можно воспользоваться стартером из папки `01-base-frontend-stages`. Запуск в дев режиме - `npm run start`, билд - `npm run build`, запуск собранного приложения - `npm run start-prod`.

Проверяемые навыки: умение работать с реактивными фреймворками, сборщиками и npm
