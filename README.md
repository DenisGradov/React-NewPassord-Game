<a name="начало"></a>

# Сайт-игра NewPassword Game

### Привет, я Денис, и я разработал сайт на Реакте. Идея не моя, но я попробовал сделать свою версию. Цель игры - создать защищенный пароль. При этом у сайта есть много правил для формирования пароля, например 6+ символов, 4+ числа, сумма чисел должна равняться 25 и другие правила, которые обязательны к выполнению. В данном проекте я немного попрактиковался с анимациями (ранее не использовал).

### Ты можешь посмотреть [краткий видео-обзор](https://youtu.be/xzyFQob5M0w), а можешь почитать этот пост

### Главы

- [Начало](#начало)
- [Правила](#Правила)
- [Используемые компоненты](#компоненты)

<a name="Правила"></a>

## Правила ([в начало](#Правила))

### Система правил довольно проста. В utils/rules.js находится список правил. В каждом правиле содержатся: номер правила (ключ, значением которого является свойство правила), заголовок (который выводится при нарушении правила), а так же функция, которая проверяет выполнение правила. Функция в параметрах получает введенный юзером пароль, после чего уже проверяет его, возвращая true при выполнении правила, а false при не выполнении. При попытке регистрации - сайт перебирает все правила (свойства). Если все правила выполняются - рендерится компонент о выигрыше. Если 1 из правил не выполняется - оно выводится ошибкой, остальные же правила (которые выполнились) - показываются как выполненные

![screen]()

<br/>

<a name="компоненты"></a>

## Используемые компоненты ([в начало](#начало))

| Название компонента | Значение                                    |
| ------------------- | ------------------------------------------- |
| App.js              | Рендеринг компонента с меню игры, состояния |
| Menu.jsx            | Рендеринг меню, мозг проекта                |
| Error.jsx           | Рендеринг ошибки                            |
| NoError.jsx         | Рендеринг выполненных правил                |
| Win.jsx             | Рендеринг сообщения о победе                |
| Rules.js            | Содержит список правил                      |
