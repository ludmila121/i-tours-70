## Lesson 1 REACT,JSX,Collections

#### SPA - Single-page application - застосунок ТІЛЬКИ з однією html сторінкою.

#### React - бібліотека,випущена Facebook у 2013 році,для вирішення проблеми з довгим оновленням візуалізації у браузері.

#### VIRTUAL DOM - точна копія browser DOM, при оновленнях вони порівнюються і браузер перемальовує ТІЛЬКИ змінену частину

#### JSX - надстройка над JS, яка дозволяє писати розмітку схожу на html.

#### Components - основні блоки з яких будується весь сайт. Їх організація та структура є дуже ВАЖЛИВОЮ!

#### Ієрархія компонентів - деревоподібна, зверху від батьківського до дочірнього.

#### Props - обєкт, який передається від компонента до компонента.

#### Prop-types - необхідні для перевірки переданих властивостей.

#### KEY - обовязковий prop при рендерингу масивів, списків, колекцій для оптимізації ре-рендерингу.

## Lesson 2 Стилізаці

#### Є 3 основні підходи до стилізації - inline style , CSS (Less,Scss), CSS modules, CSS in JS

#### 'Глобальний css' - незалежно в якому місці був підключений фай css, компілюється все в ОДИН файл.

#### \*застосовується останні стилі при одинакових класах

#### CSS modules - одне з вирішень проблеми глобального css

#### Бібліотека clsx - функція яка повертає строку з назвами класів які = true

#### Нормалізація стилів - приведення елементів до однієї поведінки для очікуваних дій при різних браузерах

## Lesson 3 Події та стан компонента

#### Функціональні компоненти ТІЛЬКИ для відображення, класові компоненти мають ВНУТРІШНІЙ СТАН

#### Для подій використовується надстройка Event - SyntheticEvent, обробники вішаємо прямо на елемент camelCase

#### state - внутрішній стан компонента, змінюється ТІЛЬКИ внутрішніми методами, зберігає обєкт.

#### setState - функція яка зміною state, та викликає render(re-render) компонента та всіх його нащадків.

#### setState - працює в асинхроному режимі після основного коду.

#### Тільки зміна props || state викликає метод render

## Lesson 4 Форми

## Форми потрібні для отримання даних від користувача.

## Елементи є: контрольовані (коли значення записується в стейт), неконтрольовані - коли в елемента немає обробника події.

## Для звязування label з input використовується атрибут htmlFor + id з input

## В залежності від типу елемента він має свою поведінку та по різному витягуються значення:

## input => event.target.value | value

## checkbox=> event.target.checked | cheked

## radio => event.target.checked | cheked \* атрибут name повинен бути одинаковий

## select => event.target.value | value \* повинен в собі мати option з атрибутом value

## Lesson 5 Методи життєвого циклу

#### В кожного класового компонента є свій життєвий цикл та вже визначені методи

#### Є 3 основні методи які має знати кожен:

#### \* componentDidMount() - викликається ТІЛЬКИ один раз після монтування компоненти

#### \* componentDidUpdate() - викликається КОЖЕН раз після рендеру, після першого рендере НЕ ВИКЛИКАЄТЬСЯ

#### \* componentWillUnmount() - викликається перед самим видалення компонента з DOM

#### Методи життєвого циклу викликаються автоматично і завжди, програмісти тільки перевизначають їхню логіку.

## Lesson 6 REST API

#### REST API не бібліотека, а тільки де факто домовленості як потрібно писати сервери

#### Для роботи з сервером ми використовуємо HTTP запити

#### GET - отримання даних

#### POST - створення даних

#### PATCH - ЧАСТКОВОГО оновлення даних

#### PUT - повного оновлення даних

#### DELETE - видалення даних

#### axios найпоширеніша бібліотека для робити з сервером

## Lesson 7 React hooks part 1

##### Хуки - функції, які підвязуються до життєвого циклу компонента.

##### useState - хук, який зберігає значення та повертає функцію для його оновлення.

##### useEffect - хук, який використовується для побічних ефектів (запити,підписки,обробники)

##### \* - без масиву залежностей - викликається при кожному render

##### \* - [] пустий масив- аналог componentDidMount

##### \* - [value_1,value_2] - спрацьовує при зміні переданих властивостей

##### Функція що повертається з useEffect аналог componentWillUnmount

##### Кастомні хуки - зберігають значення state, повертають state та методи роботи з ним.

## Lesson 8 React Hooks part 2

#### Context API - сховище в якому зберігаються дані. Доступний у всіх дочірніч компонентах незалежно від їхньої ієрархії.

#### Context API - вирішує проблему передачі пропсів між компонентами які знаходяться далеко один від одного.

#### useRef - хук який не підвязаний до методів життєвого циклу, дозволяє отримати посилання на дом елемент напряму.

#### useMemo - хук який вирішує проблему з "дорогими" js, обчисленнями, кешуючи результат виклику.

#### useCAllback - хук який кешує ініціалізацію методу, вирішує проблему виділення новох памяті для константного методу.

## Lesson 9 React router Dom part 1

#### React Router Dom - обгортка над нативними обєктами маршрутизації,яка спрощує написання та структуру коду.

#### <BrowserRouter> - компонент яким потрібно обгорнути все дерево компонентів для роботи з бібліотекою.

#### <NavLink> & <Link> - обгортки над тегом <a> які мають свою внутрішню реалізацію, <NavLink> має додатковий клас active для стилізації.

#### <Route> - компонент який вирішує чи рендерити контент чи ні. Приймає path та element. Обовязково має бути вкладений в <Routes></Routes>

#### useParams() - хук який повертає url параметри із адресної строки.

#### <Outlet> - компонент який буде рендерити те що між тегами та співпадає.

#### Пропс index - вказує, що марштрут відповідає батьківському <Route> та рендерить його без path.

## Lesson 10 React router DOM part 2

#### useNavigate() & <Navigate  to='' /> - способи програмної навігації для додатку в залежності від умов.

#### URLSearchParams - обгортка над Locationб яка повертає обєкт з параметрами та функцію для оновлення.

#### Хук useLocation - повертає обєкт розташування для поточної url адреси

#### location.state - обєкт за дпомогою якого можна прокидувати дані між різними адресами.

#### <Suspense> & React.lazy - связка яка використовується для динамічної загруки компонентів(модулів) в реакт

## Lesson 11. Redux Basic

#### Redux - біліотека для зберігання стану на фронтенді.

#### store - джерело єдиної,актуальної правди.

#### selectors - функції,які отримують актуальний стан та повертають необхідне значення.

#### actions - обєкт з полями type\*, payload який передається в store.

#### reducers - функції обробники actions, які оновлюють обєкт state.

#### useSelector - хук для використання селекторів.

#### useDispatch - хук для посилання actions в стор.

## Lesson 12: Selectors

#### Абстрація селекторів потрібна для того,щоб послабити звязки між компонентом і store.

#### Назви селекторів повинні починатися з select.

#### Атомарні селектори - просто витягують дані з state.

#### Складові селектори - містять в собі якісь операції різного типу (обчилення,філтрація і тд)

#### createSelector - метод для створення селекторів, в яких результат буде кешуватися і не обчислюватися при повторних викликах.

## Lesson 15-16

#### - Облікові записи існують для розділення інформації між різними користувачами.

#### - Права доступу відрізняють між собою користувачів (роль, статус, тип підписки).

#### - Json Web Token - метод безпечного представлення даних між двома сторонами (client, server).

#### - access_token живе до 15хв використовується для перевірки чи довіряти запиту.

#### - refresh_token використовується для оновлення пари токенів живе до 30 днів.
