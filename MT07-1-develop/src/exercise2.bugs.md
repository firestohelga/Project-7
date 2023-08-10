# БАГ- РЕПОРТ

## Баг-репорт № 1. Некорректный код ответа Activities: Запрос на создание ресурсов POST ​/api​/v1​/Activities 


1. Предшествующие условия

- Открыта страница Swagger (https://fakerestapi.azurewebsites.net/index.html)
- Открыт раздел Activities


2. Серьезность: Minor

3. Шаги для воспроизведения:

- ID в теле запроса поставить 5
- Отправить POST запрос https://fakerestapi.azurewebsites.net/api/v1/Activities
- Проверить код состояния
- Проверить тело ответа от сервера
- Проверить структуру ответа

4. Ожидаемый результат:

- код ответа 201 (Created - Создано)

5. Фактический результат:

- код ответа 200 ОК

6. Окружение: Windows 10 (Google Chrome, Версия 113.0.5672.93)

## Баг-репорт № 2. Некорректный код и тело ответа Activities: Запрос на создание ресурсов POST ​/api​/v1​/Activities негативный (пустой)


1. Предшествующие условия

- Открыта страница Swagger (https://fakerestapi.azurewebsites.net/index.html)
- Открыт раздел Activities


2. Серьезность: Major

3. Шаги для воспроизведения:

- Удалить тело запроса
- Отправить POST запрос https://fakerestapi.azurewebsites.net/api/v1/Activities
- Проверить код состояния
- Проверить тело ответа от сервера
- Проверить структуру ответа

4. Ожидаемый результат:

- код ответа 415 (Unsupported Media Type - Неподдерживаемый медиа тип)

5. Фактический результат:

- код ответа 400 (Bad Request - Плохой запрос)

6. Окружение: Windows 10 (Google Chrome, Версия 113.0.5672.93)

## Баг-репорт № 3. Некорректный код ответа Activities: Запрос на обновление ресурсов PUT ​/api​/v1​/Activities​/{id}  (отрицательный ID)


1. Предшествующие условия

- Открыта страница Swagger (https://fakerestapi.azurewebsites.net/index.html)
- Открыт раздел Activities


2. Серьезность: Minor

3. Шаги для воспроизведения:

- ID в теле запроса поставить -1
- Отправить POST запрос https://fakerestapi.azurewebsites.net/api/v1/Activities
- Проверить код состояния
- Проверить тело ответа от сервера
- Проверить структуру ответа

4. Ожидаемый результат:

- код ответа 405 (Method Not Allowed - Метод не разрешен)

5. Фактический результат:

- код ответа 200 ОК

6. Окружение: Windows 10 (Google Chrome, Версия 113.0.5672.93)

## Баг-репорт № 4. Некорректный код ответа CoverPhotos: Запрос на создание ресурсов POST ​/api​/v1​/CoverPhotos 


1. Предшествующие условия

- Открыта страница Swagger (https://fakerestapi.azurewebsites.net/index.html)
- Открыт раздел CoverPhotos


2. Серьезность: Minor

3. Шаги для воспроизведения:

- ID в теле запроса поставить 4
- Отправить POST запрос https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos
- Проверить код состояния
- Проверить тело ответа от сервера
- Проверить структуру ответа

4. Ожидаемый результат:

- код ответа 201 (Created - Создано)

5. Фактический результат:

- код ответа 200 ОК

6. Окружение: Windows 10 (Google Chrome, Версия 113.0.5672.93)

## Баг-репорт № 5. Некорректный код ответа CoverPhotos: Запрос на создание ресурсов POST ​/api​/v1​/CoverPhotos негативный (пустой)


1. Предшествующие условия

- Открыта страница Swagger (https://fakerestapi.azurewebsites.net/index.html)
- Открыт раздел CoverPhotos


2. Серьезность: Major

3. Шаги для воспроизведения:

- Удалить тело запроса
- Отправить POST запрос https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos
- Проверить код состояния
- Проверить тело ответа от сервера
- Проверить структуру ответа

4. Ожидаемый результат:

- код ответа 415 (Unsupported Media Type - Неподдерживаемый медиа тип)

5. Фактический результат:

- код ответа 400 (Bad Request - Плохой запрос)

6. Окружение: Windows 10 (Google Chrome, Версия 113.0.5672.93)

## Баг-репорт № 6. Некорректный код ответа Users​: Запрос на обновление ресурсов PUT ​/api​/v1​/Users​/{id}  (отрицательный ID)


1. Предшествующие условия

- Открыта страница Swagger (https://fakerestapi.azurewebsites.net/index.html)
- Открыт раздел Users


2. Серьезность: Minor

3. Шаги для воспроизведения:

- ID в теле запроса поставить -1
- Отправить POST запрос https://fakerestapi.azurewebsites.net/api/v1/Users/-1
- Проверить код состояния
- Проверить тело ответа от сервера
- Проверить структуру ответа

4. Ожидаемый результат:

- код ответа 405 (Method Not Allowed - Метод не разрешен)

5. Фактический результат:

- код ответа 200 ОК

6. Окружение: Windows 10 (Google Chrome, Версия 113.0.5672.93)


## Баг-репорт №7. Users: (POST)добавление нового пользователя 

1. Предшествующие условия

- Открыта страница сайта (https://fakerestapi.azurewebsites.net/index.html)
- Открыта секция  объекта Authors со списком методов

2. Серьезность: Minor 

3. Шаги для воспроизведения:
- Заполнить тело запроса POST /api/v1/Users
Тело запроса:
{
"id": 1000,
"userName": "User 1000",
"password": "Password 1000"
}
- Отправить POST запрос https://fakerestapi.azurewebsites.net/api/v1/Users
- Проверить код состояния
- Проверить структуру ответа
- Проверить заголовок ответа
- Проверка базовой работоспособности

4. Ожидаемый результат:
- Отображается тело запроса в формате JSON
- Запрос успешно отправлен на сервер
- `Получение статус-кода 201.`
- Структура JSON отображена корректно
- Заголовок содержит метаданные о запросе и ответе (тип содержимого, дата и время ответа, сервер)
- Успешно
5. Фактический результат:
- Отображается тело запроса в формате JSON
- Запрос успешно отправлен на сервер
- `Получение статус-кода 200.`
- Структура JSON отображена корректно
- Заголовок содержит метаданные о запросе и ответе (тип содержимого, дата и время ответа, сервер)
- Успешно

6. Окружение: Windows 11 Pro (Google Chrome, Версия Версия 113.0.5672.129)

## Баг-репорт №8. Users: (POST)добавление нового пользователя (некорректный id=отрицательное значение) 

1. Предшествующие условия

- Открыта страница сайта (https://fakerestapi.azurewebsites.net/index.html)
- Открыта секция  объекта Authors со списком методов

2. Серьезность: Major 

3. Шаги для воспроизведения:
- Заполнить тело запроса POST /api/v1/Users
Тело запроса:
{ "id": -1,
 "userName": "User 1000",
 "password": "Password 1000"}
- Отправить POST запрос https://fakerestapi.azurewebsites.net/api/v1/Users
- Проверить код состояния
- Проверить структуру ответа
- Проверить заголовок ответа
- Проверка базовой работоспособности

4. Ожидаемый результат:
- Отображается тело запроса в формате JSON
- Запрос успешно отправлен на сервер
- `Получение статус-кода 400.`
- Структура JSON отображена корректно
- Заголовок содержит метаданные о запросе и ответе (тип содержимого, дата и время ответа, сервер)
- Успешно
5. Фактический результат:
- Отображается тело запроса в формате JSON
- Запрос успешно отправлен на сервер
- `Получение статус-кода 200.`
- Структура JSON отображена корректно
- Заголовок содержит метаданные о запросе и ответе (тип содержимого, дата и время ответа, сервер)
- Успешно

6. Окружение: Windows 11 Pro (Google Chrome, Версия Версия 113.0.5672.129)

## Баг-репорт №9. Users: (POST)добавление нового пользователя (некорректный id=0) 

1. Предшествующие условия

- Открыта страница сайта (https://fakerestapi.azurewebsites.net/index.html)
- Открыта секция  объекта Authors со списком методов

2. Серьезность: Major 

3. Шаги для воспроизведения:
- Заполнить тело запроса POST /api/v1/Users
Тело запроса:
{ "id":0,
 "userName": "User 1000",
 "password": "Password 1000"}
- Отправить POST запрос https://fakerestapi.azurewebsites.net/api/v1/Users
- Проверить код состояния
- Проверить структуру ответа
- Проверить заголовок ответа
- Проверка базовой работоспособности

4. Ожидаемый результат:
- Отображается тело запроса в формате JSON
- Запрос успешно отправлен на сервер
- `Получение статус-кода 400.`
- Структура JSON отображена корректно
- Заголовок содержит метаданные о запросе и ответе (тип содержимого, дата и время ответа, сервер)
- Успешно
5. Фактический результат:
- Отображается тело запроса в формате JSON
- Запрос успешно отправлен на сервер
- `Получение статус-кода 200.`
- Структура JSON отображена корректно
- Заголовок содержит метаданные о запросе и ответе (тип содержимого, дата и время ответа, сервер)
- Успешно

6. Окружение: Windows 11 Pro (Google Chrome, Версия Версия 113.0.5672.129)

## Баг-репорт №10. Users: (POST)добавление нового пользователя(не заполнены данные имя и пароль пользователя)

1. Предшествующие условия

- Открыта страница сайта (https://fakerestapi.azurewebsites.net/index.html)
- Открыта секция  объекта Authors со списком методов

2. Серьезность: Major 

3. Шаги для воспроизведения:
- Заполнить тело запроса POST /api/v1/Users
{ "id": 1000
  "userName": "",
  "password": ""}
- Отправить POST запрос https://fakerestapi.azurewebsites.net/api/v1/Users
- Проверить код состояния
- Проверить структуру ответа
- Проверить заголовок ответа
- Проверка базовой работоспособности

4. Ожидаемый результат:
- Отображается тело запроса в формате JSON
- Запрос успешно отправлен на сервер
- `Получение статус-кода 400.`
- Структура JSON отображена корректно
- Заголовок содержит метаданные о запросе и ответе (тип содержимого, дата и время ответа, сервер)
- Успешно
5. Фактический результат:
- Отображается тело запроса в формате JSON
- Запрос успешно отправлен на сервер
- `Получение статус-кода 200.`
- Структура JSON отображена корректно
- Заголовок содержит метаданные о запросе и ответе (тип содержимого, дата и время ответа, сервер)
- Успешно

6. Окружение: Windows 11 Pro (Google Chrome, Версия Версия 113.0.5672.129)

## Баг-репорт №11. Users: (POST)добавление нового пользователя ( указаны некорректные данные имя и фамилия пользователя: символы)

1. Предшествующие условия

- Открыта страница сайта (https://fakerestapi.azurewebsites.net/index.html)
- Открыта секция  объекта Authors со списком методов

2. Серьезность: Major 

3. Шаги для воспроизведения:
- Заполнить тело запроса POST /api/v1/Users
{ "id": 10000000000
  "userName": "№№№№№№№№",
  "password": "№№№№№№№№"}
- Отправить POST запрос https://fakerestapi.azurewebsites.net/api/v1/Users
- Проверить код состояния
- Проверить структуру ответа
- Проверить заголовок ответа
- Проверка базовой работоспособности

4. Ожидаемый результат:
- Отображается тело запроса в формате JSON
- Запрос успешно отправлен на сервер
- `Получение статус-кода 400.`
- Структура JSON отображена корректно
- Заголовок содержит метаданные о запросе и ответе (тип содержимого, дата и время ответа, сервер)
- Успешно
5. Фактический результат:
- Отображается тело запроса в формате JSON
- Запрос успешно отправлен на сервер
- `Получение статус-кода 200.`
- Структура JSON отображена корректно
- Заголовок содержит метаданные о запросе и ответе (тип содержимого, дата и время ответа, сервер)
- Успешно

6. Окружение: Windows 11 Pro (Google Chrome, Версия Версия 113.0.5672.129)

## Баг-репорт №12. Users: (POST)добавление нового пользователя ( указаны некорректные данные имя и фамилия пользователя: цифры)

1. Предшествующие условия

- Открыта страница сайта (https://fakerestapi.azurewebsites.net/index.html)
- Открыта секция  объекта Authors со списком методов

2. Серьезность: Major 

3. Шаги для воспроизведения:
- Заполнить тело запроса POST /api/v1/Users
{ "id": 1000
  "userName": "1000",
  "password": "1000"}
- Отправить POST запрос https://fakerestapi.azurewebsites.net/api/v1/Users
- Проверить код состояния
- Проверить структуру ответа
- Проверить заголовок ответа
- Проверка базовой работоспособности

4. Ожидаемый результат:
- Отображается тело запроса в формате JSON
- Запрос успешно отправлен на сервер
- `Получение статус-кода 400.`
- Структура JSON отображена корректно
- Заголовок содержит метаданные о запросе и ответе (тип содержимого, дата и время ответа, сервер)
- Успешно
5. Фактический результат:
- Отображается тело запроса в формате JSON
- Запрос успешно отправлен на сервер
- `Получение статус-кода 200.`
- Структура JSON отображена корректно
- Заголовок содержит метаданные о запросе и ответе (тип содержимого, дата и время ответа, сервер)
- Успешно

6. Окружение: Windows 11 Pro (Google Chrome, Версия Версия 113.0.5672.129)


## Баг-репорт №13. Authors: (POST)добавление нового автора  

1. Предшествующие условия

- Открыта страница сайта (https://fakerestapi.azurewebsites.net/index.html)
- Открыта секция  объекта Authors со списком методов

2. Серьезность: Minor

3. Шаги для воспроизведения:
- Заполнить тело запроса POST /api/v1/Authors
Тело запроса:
{"id": 1000,
 "idBook": 1000,
 "firstName": "First Name 1000",
 "lastName": "Last Name 1000"}
- Отправить POST запрос https://fakerestapi.azurewebsites.net/api/v1/Authors
- Проверить код состояния
- Проверить структуру ответа
- Проверить заголовок ответа
- Проверка базовой работоспособности

4. Ожидаемый результат:
- Отображается тело запроса в формате JSON
- Запрос успешно отправлен на сервер
- `Получение статус-кода 201.`
- Структура JSON отображена корректно
- Заголовок содержит метаданные о запросе и ответе (тип содержимого, дата и время ответа, сервер)
- Успешно
5. Фактический результат:
- Отображается тело запроса в формате JSON
- Запрос успешно отправлен на сервер
- `Получение статус-кода 200.`
- Структура JSON отображена корректно
- Заголовок содержит метаданные о запросе и ответе (тип содержимого, дата и время ответа, сервер)
- Успешно

6. Окружение: Windows 11 Pro (Google Chrome, Версия Версия 113.0.5672.129)

## Баг-репорт №14. Authors: (POST)добавление нового автора (некорректный id=0)

1. Предшествующие условия

- Открыта страница сайта (https://fakerestapi.azurewebsites.net/index.html)
- Открыта секция  объекта Authors со списком методов

2. Серьезность: Major 

3. Шаги для воспроизведения:
- Заполнить тело запроса POST /api/v1/Authors
Тело запроса:
{ "id": 0,
  "idBook": 0,
  "firstName": "First Name 1000",
   "lastName": "Last Name 1000"}
- Отправить POST запрос https://fakerestapi.azurewebsites.net/api/v1/Authors
- Проверить код состояния
- Проверить структуру ответа
- Проверить заголовок ответа
- Проверка базовой работоспособности

4. Ожидаемый результат:
- Отображается тело запроса в формате JSON
- Запрос успешно отправлен на сервер
- `Получение статус-кода 400. Неверный запрос.`
- Структура JSON отображена корректно
- Заголовок содержит метаданные о запросе и ответе (тип содержимого, дата и время ответа, сервер)
- Успешно
5. Фактический результат:
- Отображается тело запроса в формате JSON
- Запрос успешно отправлен на сервер
- `Получение статус-кода 200.`
- Структура JSON отображена корректно
- Заголовок содержит метаданные о запросе и ответе (тип содержимого, дата и время ответа, сервер)
- Успешно

6. Окружение: Windows 11 Pro (Google Chrome, Версия Версия 113.0.5672.129)

## Баг-репорт №15. Authors: (POST)добавление нового автора (некорректный id=отрицательное значение)

1. Предшествующие условия

- Открыта страница сайта (https://fakerestapi.azurewebsites.net/index.html)
- Открыта секция  объекта Authors со списком методов

2. Серьезность: Major 

3. Шаги для воспроизведения:
- Заполнить тело запроса POST /api/v1/Authors
Тело запроса:
{ "id": -5,
  "idBook": -5,
  "firstName": "First Name 1000",
   "lastName": "Last Name 1000"}
- Отправить POST запрос https://fakerestapi.azurewebsites.net/api/v1/Authors
- Проверить код состояния
- Проверить структуру ответа
- Проверить заголовок ответа
- Проверка базовой работоспособности

4. Ожидаемый результат:
- Отображается тело запроса в формате JSON
- Запрос успешно отправлен на сервер
- `Получение статус-кода 400. Неверный запрос.`
- Структура JSON отображена корректно
- Заголовок содержит метаданные о запросе и ответе (тип содержимого, дата и время ответа, сервер)
- Успешно
5. Фактический результат:
- Отображается тело запроса в формате JSON
- Запрос успешно отправлен на сервер
- `Получение статус-кода 200.`
- Структура JSON отображена корректно
- Заголовок содержит метаданные о запросе и ответе (тип содержимого, дата и время ответа, сервер)
- Успешно

6. Окружение: Windows 11 Pro (Google Chrome, Версия Версия 113.0.5672.129)

## Баг-репорт №16. Authors: (POST)добавление нового автора (не заполнены данные имя и фамилия автора)

1. Предшествующие условия

- Открыта страница сайта (https://fakerestapi.azurewebsites.net/index.html)
- Открыта секция  объекта Authors со списком методов

2. Серьезность: Major 

3. Шаги для воспроизведения:
- Заполнить тело запроса POST /api/v1/Authors
Тело запроса:
{ "id": 1000,
  "idBook": 1000,
  "firstName": "",
   "lastName": ""}
- Отправить POST запрос https://fakerestapi.azurewebsites.net/api/v1/Authors
- Проверить код состояния
- Проверить структуру ответа
- Проверить заголовок ответа
- Проверка базовой работоспособности

4. Ожидаемый результат:
- Отображается тело запроса в формате JSON
- Запрос успешно отправлен на сервер
- `Получение статус-кода 400. Неверный запрос.`
- Структура JSON отображена корректно
- Заголовок содержит метаданные о запросе и ответе (тип содержимого, дата и время ответа, сервер)
- Успешно
5. Фактический результат:
- Отображается тело запроса в формате JSON
- Запрос успешно отправлен на сервер
- `Получение статус-кода 200.`
- Структура JSON отображена корректно
- Заголовок содержит метаданные о запросе и ответе (тип содержимого, дата и время ответа, сервер)
- Успешно

6. Окружение: Windows 11 Pro (Google Chrome, Версия Версия 113.0.5672.129)

## Баг-репорт №17. Authors: (POST)добавление нового автора ( указаны некорректные данные имя и фамилия автора: символы)

1. Предшествующие условия

- Открыта страница сайта (https://fakerestapi.azurewebsites.net/index.html)
- Открыта секция  объекта Authors со списком методов

2. Серьезность: Major 

3. Шаги для воспроизведения:
- Заполнить тело запроса POST /api/v1/Authors
Тело запроса:
{ "id": 1000,
 "idBook": 1000,
 "firstName": "№№№№№№№№",
 "lastName": "№№№№№№№№"}
- Отправить POST запрос https://fakerestapi.azurewebsites.net/api/v1/Authors
- Проверить код состояния
- Проверить структуру ответа
- Проверить заголовок ответа
- Проверка базовой работоспособности

4. Ожидаемый результат:
- Отображается тело запроса в формате JSON
- Запрос успешно отправлен на сервер
- `Получение статус-кода 400. Неверный запрос.`
- Структура JSON отображена корректно
- Заголовок содержит метаданные о запросе и ответе (тип содержимого, дата и время ответа, сервер)
- Успешно
5. Фактический результат:
- Отображается тело запроса в формате JSON
- Запрос успешно отправлен на сервер
- `Получение статус-кода 200.`
- Структура JSON отображена корректно
- Заголовок содержит метаданные о запросе и ответе (тип содержимого, дата и время ответа, сервер)
- Успешно

6. Окружение: Windows 11 Pro (Google Chrome, Версия Версия 113.0.5672.129)

## Баг-репорт №18. Authors: (POST)добавление нового автора ( указаны некорректные данные имя и фамилия автора: Цифры)

1. Предшествующие условия

- Открыта страница сайта (https://fakerestapi.azurewebsites.net/index.html)
- Открыта секция  объекта Authors со списком методов

2. Серьезность: Major 

3. Шаги для воспроизведения:
- Заполнить тело запроса POST /api/v1/Authors
Тело запроса:
{ "id": 1000,
  "idBook": 1000,
 "firstName": "9999",
 "lastName": "9999"}
- Отправить POST запрос https://fakerestapi.azurewebsites.net/api/v1/Authors
- Проверить код состояния
- Проверить структуру ответа
- Проверить заголовок ответа
- Проверка базовой работоспособности

4. Ожидаемый результат:
- Отображается тело запроса в формате JSON
- Запрос успешно отправлен на сервер
- `Получение статус-кода 400. Неверный запрос.`
- Структура JSON отображена корректно
- Заголовок содержит метаданные о запросе и ответе (тип содержимого, дата и время ответа, сервер)
- Успешно
5. Фактический результат:
- Отображается тело запроса в формате JSON
- Запрос успешно отправлен на сервер
- `Получение статус-кода 200.`
- Структура JSON отображена корректно
- Заголовок содержит метаданные о запросе и ответе (тип содержимого, дата и время ответа, сервер)
- Успешно

6. Окружение: Windows 11 Pro (Google Chrome, Версия Версия 113.0.5672.129)

## Баг-репорт №19. Authors: (GET c ID )получение данных об авторах конкретной книги (некорректный id=0)

1. Предшествующие условия

- Открыта страница сайта (https://fakerestapi.azurewebsites.net/index.html)
- Открыта секция  объекта Authors со списком методов

2. Серьезность: Minor

3. Шаги для воспроизведения:
- Отправить GET запрос https://fakerestapi.azurewebsites.net/api/v1/Authors/authors/books/0
- Проверить код состояния
- Проверить структуру ответа
- Проверить заголовок ответа
- Проверка базовой работоспособности

4. Ожидаемый результат:

- Запрос успешно отправлен на сервер
- `Получение статус-кода 400. Неверный запрос.`
- Структура JSON отображена корректно
- Заголовок содержит метаданные о запросе и ответе (тип содержимого, дата и время ответа, сервер)
- Успешно
5. Фактический результат:
- Запрос успешно отправлен на сервер
- `Получение статус-кода 200.`
- Структура JSON отображена корректно
- Заголовок содержит метаданные о запросе и ответе (тип содержимого, дата и время ответа, сервер)
- Успешно

6. Окружение: Windows 11 Pro (Google Chrome, Версия Версия 113.0.5672.129)

## Баг-репорт №20. Authors: (GET c ID )получение данных об авторах конкретной книги (некорректный id=отрицательное значение)

1. Предшествующие условия

- Открыта страница сайта (https://fakerestapi.azurewebsites.net/index.html)
- Открыта секция  объекта Authors со списком методов

2. Серьезность: Minor

3. Шаги для воспроизведения:
- Отправить GET запрос https://fakerestapi.azurewebsites.net/api/v1/Authors/authors/books/-1
- Проверить код состояния
- Проверить структуру ответа
- Проверить заголовок ответа
- Проверка базовой работоспособности

4. Ожидаемый результат:

- Запрос успешно отправлен на сервер
- `Получение статус-кода 400. Неверный запрос.`
- Структура JSON отображена корректно
- Заголовок содержит метаданные о запросе и ответе (тип содержимого, дата и время ответа, сервер)
- Успешно
5. Фактический результат:
- Запрос успешно отправлен на сервер
- `Получение статус-кода 200.`
- Структура JSON отображена корректно
- Заголовок содержит метаданные о запросе и ответе (тип содержимого, дата и время ответа, сервер)
- Успешно

6. Окружение: Windows 11 Pro (Google Chrome, Версия Версия 113.0.5672.129)


## Баг-репорт №21. Authors: (PUT)замена данных по  конкретному автору (не заполнены данные имя и фамилия автора)

1. Предшествующие условия

- Открыта страница сайта (https://fakerestapi.azurewebsites.net/index.html)
- Открыта секция  объекта Authors со списком методов

2. Серьезность: Minor

3. Шаги для воспроизведения:
- Заполнить тело запроса PUT /api/v1/Authors/1
Тело запроса:
{"id": 1,
"idBook": 1,
"firstName": "",
"lastName": ""}
- Отправить PUT запрос https://fakerestapi.azurewebsites.net/api/v1/Authors/1
- Проверить код состояния
- Проверить структуру ответа
- Проверить заголовок ответа
- Проверка базовой работоспособности

4. Ожидаемый результат:
- Отображается тело запроса в формате JSON
- Запрос успешно отправлен на сервер
- `Получение статус-кода 400. Неверный запрос.`
- Структура JSON отображена корректно
- Заголовок содержит метаданные о запросе и ответе (тип содержимого, дата и время ответа, сервер)
- Успешно
5. Фактический результат:
- Отображается тело запроса в формате JSON
- Запрос успешно отправлен на сервер
- `Получение статус-кода 200.`
- Структура JSON отображена корректно
- Заголовок содержит метаданные о запросе и ответе (тип содержимого, дата и время ответа, сервер)
- Успешно

6. Окружение: Windows 11 Pro (Google Chrome, Версия Версия 113.0.5672.129)

## Баг-репорт №22. Authors: (PUT)замена данных по  конкретному автору ( указаны некорректные данные имя и фамилия автора: символы)

1. Предшествующие условия

- Открыта страница сайта (https://fakerestapi.azurewebsites.net/index.html)
- Открыта секция  объекта Authors со списком методов

2. Серьезность: Minor

3. Шаги для воспроизведения:
- Заполнить тело запроса PUT /api/v1/Authors/1
Тело запроса:
{"id": 1,
 "idBook": 1,
 "firstName": "№№№№№№№№",
 "lastName": "№№№№№№№№"}
- Отправить PUT запрос https://fakerestapi.azurewebsites.net/api/v1/Authors/1
- Проверить код состояния
- Проверить структуру ответа
- Проверить заголовок ответа
- Проверка базовой работоспособности

4. Ожидаемый результат:
- Отображается тело запроса в формате JSON
- Запрос успешно отправлен на сервер
- `Получение статус-кода 400. Неверный запрос.`
- Структура JSON отображена корректно
- Заголовок содержит метаданные о запросе и ответе (тип содержимого, дата и время ответа, сервер)
- Успешно
5. Фактический результат:
- Отображается тело запроса в формате JSON
- Запрос успешно отправлен на сервер
- `Получение статус-кода 200.`
- Структура JSON отображена корректно
- Заголовок содержит метаданные о запросе и ответе (тип содержимого, дата и время ответа, сервер)
- Успешно

6. Окружение: Windows 11 Pro (Google Chrome, Версия Версия 113.0.5672.129)

## Баг-репорт №23. Authors: (PUT)замена данных по  конкретному автору ( указаны некорректные данные имя и фамилия автора: цифры)

1. Предшествующие условия

- Открыта страница сайта (https://fakerestapi.azurewebsites.net/index.html)
- Открыта секция  объекта Authors со списком методов

2. Серьезность: Minor

3. Шаги для воспроизведения:
- Заполнить тело запроса PUT /api/v1/Authors/1
Тело запроса:
{"id": 1,
 "idBook": 1,
 "firstName": "99999",
 "lastName": "99999"}
- Отправить PUT запрос https://fakerestapi.azurewebsites.net/api/v1/Authors/1
- Проверить код состояния
- Проверить структуру ответа
- Проверить заголовок ответа
- Проверка базовой работоспособности

4. Ожидаемый результат:
- Отображается тело запроса в формате JSON
- Запрос успешно отправлен на сервер
- `Получение статус-кода 400. Неверный запрос.`
- Структура JSON отображена корректно
- Заголовок содержит метаданные о запросе и ответе (тип содержимого, дата и время ответа, сервер)
- Успешно
5. Фактический результат:
- Отображается тело запроса в формате JSON
- Запрос успешно отправлен на сервер
- `Получение статус-кода 200.`
- Структура JSON отображена корректно
- Заголовок содержит метаданные о запросе и ответе (тип содержимого, дата и время ответа, сервер)
- Успешно

6. Окружение: Windows 11 Pro (Google Chrome, Версия Версия 113.0.5672.129)

## Баг-репорт №24. Authors: (DELETE )удаление данных о конкретном авторе   (некорректный id=0) 

1. Предшествующие условия

- Открыта страница сайта (https://fakerestapi.azurewebsites.net/index.html)
- Открыта секция  объекта Authors со списком методов

2. Серьезность: Minor

3. Шаги для воспроизведения:

- Отправить DELETE запрос https://fakerestapi.azurewebsites.net/api/v1/Authors/0
- Проверить код состояния
- Проверить структуру ответа
- Проверить заголовок ответа
- Проверка базовой работоспособности

4. Ожидаемый результат:

- Запрос успешно отправлен на сервер
- `Получение статус-кода 400. Неверный запрос.`
- `Структура JSON отображена корректно`
- Заголовок содержит метаданные о запросе и ответе (тип содержимого, дата и время ответа, сервер)
- Успешно
5. Фактический результат:

- Запрос успешно отправлен на сервер
- `Получение статус-кода 200.`
- `Отсутствует`
- Заголовок содержит метаданные о запросе и ответе (тип содержимого, дата и время ответа, сервер)
- Успешно

6. Окружение: Windows 11 Pro (Google Chrome, Версия Версия 113.0.5672.129)

## Баг-репорт №25. Authors: (DELETE )удаление данных о конкретном авторе   (некорректный id=отрицательное число) 

1. Предшествующие условия

- Открыта страница сайта (https://fakerestapi.azurewebsites.net/index.html)
- Открыта секция  объекта Authors со списком методов

2. Серьезность: Minor

3. Шаги для воспроизведения:

- Отправить DELETE запрос https://fakerestapi.azurewebsites.net/api/v1/Authors/-1
- Проверить код состояния
- Проверить структуру ответа
- Проверить заголовок ответа
- Проверка базовой работоспособности

4. Ожидаемый результат:

- Запрос успешно отправлен на сервер
- `Получение статус-кода 400. Неверный запрос.`
- `Структура JSON отображена корректно`
- Заголовок содержит метаданные о запросе и ответе (тип содержимого, дата и время ответа, сервер)
- Успешно
5. Фактический результат:

- Запрос успешно отправлен на сервер
- `Получение статус-кода 200.`
- `Отсутствует`
- Заголовок содержит метаданные о запросе и ответе (тип содержимого, дата и время ответа, сервер)
- Успешно

6. Окружение: Windows 11 Pro (Google Chrome, Версия Версия 113.0.5672.129)

## Баг-репорт № 26. Некорректный код ответа Books: Запрос на добавление отчета POST ​/api​/v1​/Books 

1. Предшествующие условия

- Открыта страница Swagger (https://fakerestapi.azurewebsites.net/index.html)
- Открыт раздел Books

2. Серьезность: Minor

3. Шаги для воспроизведения:

- ID в теле запроса поставить 12
- Отправить POST запрос https://fakerestapi.azurewebsites.net/api/v1/Books
- Проверить код состояния
- Проверить тело ответа от сервера
- Проверить структуру ответа

4. Ожидаемый результат:

- Получен код ответа 201 (Created - Создано)

5. Фактический результат:

- Получен код ответа 200 ОК

6. Окружение: Windows 11 (Atom, Версия 26.0.0.21)

## Баг-репорт № 27. Некорректный код ответа Books: Запрос на обновление отчета c отрицательным ID. PUT ​/api​/v1​/Books​/{id}

1. Предшествующие условия

- Открыта страница Swagger (https://fakerestapi.azurewebsites.net/index.html)
- Открыт раздел Books

2. Серьезность: Minor

3. Шаги для воспроизведения:

- ID в теле запроса поставить -1
- Отправить DELETE запрос https://fakerestapi.azurewebsites.net/api/v1/Books/
- Проверить код состояния

4. Ожидаемый результат:

- Получен код ответа 405 (Method Not Allowed - Метод не разрешен)

5. Фактический результат:

- Получен код ответа 200 ОК

6. Окружение: Windows 11 (Atom, Версия 26.0.0.21)

## Баг-репорт № 28. Некорректный код ответа CoverPhotos: Запрос на обновление обложки c отрицательным ID. PUT ​//api/v1/CoverPhotos/{id}

1. Предшествующие условия

- Открыта страница Swagger (https://fakerestapi.azurewebsites.net/index.html)
- Открыт раздел CoverPhotos

2. Серьезность: Minor

3. Шаги для воспроизведения:

- ID в теле запроса поставить -1
- Отправить POST запрос https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/
- Проверить код состояния
- Проверить тело ответа от сервера
- Проверить структуру ответа

4. Ожидаемый результат:

- Получен код ответа 405 (Method Not Allowed - Метод не разрешен)

5. Фактический результат:

- Получен код ответа 200 ОК

6. Окружение: Windows 11 (Atom, Версия 26.0.0.21)

