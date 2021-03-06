=================
История изменений
=================

2.1 (6.05.2018)
---------------
* `Wallet.balance` теперь имеет базовое значение `currency` 643 (Российский рубль)
* Новый метод для идентификации кошельков: `Wallet.identification`
* Весь блок методов к истории платежей был обновлен до API v2
* Для получения квитанции по платежу был добавлен метод `Wallet.cheque`
* Если у вас по какой-то причине нет "балансов" на аккаунте, вы можете их создать при помощи `Wallet.create_account`
    Запрос доступных счетов, доступных для создания реализован в `Wallet.offered_accounts`
* Создание ссылки для автозаполненных платежных форм достуно в `pyqiwi.generate_form_link`
* Вы хотите определить ID провайдера для пополнения мобильного телефона? Используйте `pyqiwi.detect_mobile`

2.0.8 (29.04.2018)
------------------

* У нас появились тесты! 
* Небольшие исправления

2.0.7 (14.04.2018)
------------------

* Небольшие исправления

2.0.6 (9.03.2018)
-----------------

* Небольшие исправления

2.0.5 (6.11.2017)
-----------------

* Логгер был перенесен из `pyqiwi.logger` в `pyqiwi.apihelper.logger`
* Появился метод в `Wallet` `transaction` для получения определенной транзакции по ID и её типу.
* Вместе с этим и появился для него собственный тип: `pyqiwi.types.Transaction`
* Небольшие исправления в документации
* Небольшие исправления

2.0.4 (6.11.2017)
-----------------

* Небольшие исправления

2.0.3 (6.11.2017)
-----------------

* Небольшие исправления

2.0.2 (29.10.2017)
------------------

* Небольшие исправления

2.0.1 (29.10.2017)
------------------

* У нас появилась документация на ReadTheDocs!
* Документация в коде была широко дополнена
* Были внесены изменения в вид документации в коде

2.0 (28.10.2017)
----------------
Первое большое изменение библиотеки!

* Интересны логи? У нас появился логгер `pyqiwi` в `pyqiwi.logger`
* Хотите посмотреть счета в Qiwi? `Wallet.accounts`
* Теперь выдается не `dict`-обьекты, а что-либо из `pyqiwi/types.py`
* Все вызовы к API были перенесены в `pyqiwi/apihelper.py`
* Если у вас возникла ошибка в запросе к API, вы получите исключение из `pyqiwi/exceptions.py`

1.2.1 (24.10.2017)
------------------

* Релиз на PyPI.

1.2 (24.10.2017)
----------------

* Переименование класса `Person` в `Wallet`
* Методы класса `Payment` теперь в `Wallet`
* Класс `Payment` удален
* Нет необходимости в config'е, теперь нужно передать токен в `Wallet()` [Возможность мульти-аккаунта]
* Вместе с этим, нужно передавать токен в `get_commission` (но эта же функция находится в `Wallet` c подготовленным токеном)
* Методы `Wallet.history()` и `Wallet.stat()` требуют `datetime.datetime`, вместо `str`
* Любые обращения к f-строкам, были заменены на метод `str.format`

1.1 (5.09.2017)
---------------
* Небольшие улучшения

1.0 (5.09.2017)
---------------
* Первый релиз!