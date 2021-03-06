﻿## API для записи/чтения данных в БД

### 1. Регистрация нового пользователя
```
string Registration (string login, string password) {
    return message;
}
```

Функция принимает логин и пароль в качестве аргументов и возвращает сообщение об успешной регистрации нового пользователя, либо сообщение об ошибке, если регистрация не удалась.

### 2. Авторизация пользователя
```
string Authorization (string login, string password) {
    return message;
}
```

Функция принимает логин и пароль в качестве аргументов и возвращает сообщение об успешной авторизации пользователя, либо сообщение об ошибке, если авторизация не удалась.

### 3. Отправка нового сообщения
```
 bool PostMessage (string loginSender, string loginRecipient, string textMessage, string typeMessage = "text") {
    return message;
}
```

Функция принимает логины отправителя / получателя, текст сообщения и и тип сообщения (`text` или `file`, по умолчанию - `text`) в качестве аргументов и возвращает `true` если запись успешно осуществлена и `false` если запись не была осуществлена.

### 4. Получение нового сообщения или запрос нескольких сообщений
```
Dictionary<DateTime, List<string>> GetMessage (string loginSender, string loginRecipient, int quantityMessages) {

}
```

Функция принимает логины отправителя / получателя и количество сообщений в качестве аргументов и возвращает `Dictionary<DateTime, List<string>>` с датой в качестве ключа, а в качестве значения `List<string>` с двумя элементами (первый элемент сообщение, а второй элемент тип сообшения).

### 5. Получение списка пользователей
```
List<string> GetUserList () {

}
```

Функция возвращает `List<string>` с датой в качестве ключа, а в качестве значения `List<string>` со списком пользователей.