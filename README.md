# exchange-parser

## 💾 Information
Данная программа получает информацию о цене последней совершенной сделки по тикеру.

Запрос адреса осуществляется через взаимодействие с API Московской Биржи

Программа имитирует работу клиента, а также ответ от сервера.

Имитация клиента расположена в `inforest/parserexchanger/client`

Код сервера расположен в `inforest/parserexchanger/server`

### ❓ Что делает клиент?
Клиент вводит название тикера в консоль и посылает гет-запрос с именем тикера:
```
http://localhost:8080/api/get?ticker=tickerName
```
При успешном выполнении получает ответ в виде JSON. 
Пример:
```json
{
  "response": {
    "time": "2021-09-09 18:48:17",
    "ticker_name": "AFLT",
    "last_price": "66.62"
  }
}
```

### ❓ Что делает сервер?
Сервер получает гет-запрос от нашего клиента.
Затем сервер делает гет-запрос на API Московской Биржи и возвращает ответ.

## 📝 How to run
Просто склонируйте репозиторий к себе
- Запустите `ParserExchangerApplication.java`
- Запустите `client/Main.java`