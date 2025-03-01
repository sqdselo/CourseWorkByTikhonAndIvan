## Краткий тур по базе данных
<hr/>

## Сущности
1) ### Пользователь:
<span style="color:orange">__id__</span> - *уникальный идентификатор* <br/>
__fio__ - *фамилия имя отчество* <br/>
__email__ - *электронный адрес* <br/>
__phone__ - *номер телефона* <br/>
__birth_date__ - *дата рождения* <br/>
__password__ - *хешированный пароль*<br/>

2) ### Счет:
<span style="color:orange">__id__</span> - *уникальный идентификатор* <br/>
<span style="color:green">__user_id__</span> - *идентификатор владельца счета* <br/>
__balance__ - *состояние счета* <br/>
__is_active__ - *активен ли счет* <br/>
__create_date__ - *дата создания счета* <br/>

3) ### Карта:
<span style="color:orange">__id__</span> - *уникальный идентификатор* <br/>
<span style="color:green">__account_id__</span> - *идентификатор счета, которому принадлежит карта* <br/>
__nubmer__ - *номер карты* <br/>
__expiration_date__ - *срок действия* <br/>
__cvv__ - *защитный код* <br/>
__status__ - *текущее состояние карты (активна, заблокирована или прошел срок действия)* <br/>

4) ### Заявка:
<span style="color:orange">__id__</span> - *уникальный идентификатор* <br/>
<span style="color:green">__card_id__</span> - *идентификатор карты из которой будет происходить снятие валюты* <br/>
__amount__ - *планируемая сумма снятия* <br/>
__status__ - *текущее состояние заявки (ожидает, принята, отклонена)*
__create_date__ - *дата создания заявки* <br/>

5) ### Выдача наличных:
<span style="color:orange">__id__</span> - *уникальный идентификатор* <br/>
<span style="color:green">__account_id__</span> - *идентификатор счета, из которого будет происходить снятие* <br/>
<span style="color:green">__withdrawal_request_id__</span> - *идентификатор заявки, которая хранит сумму снятия и карту* <br/>
__create_date__ - *дата выдачи наличных* <br/>

6) ### Операция на пополнение:
<span style="color:orange">__id__</span> - *уникальный идентификатор* <br/>
<span style="color:green">__account_id__</span> - *идентификатор счета, на который будет поступление денег* <br/>
__amount__ - *сумма пополнения* <br/>
__create_date__ - *дата пополнения* <br/>

7) ### Перевод денег:
<span style="color:orange">__id__</span> - *уникальный идентификатор* <br/>
<span style="color:green">__from_account_id__</span> - *счет отправителя* <br/>
<span style="color:green">__to_account_id__</span> - *счет получателя* <br/>
__amount__ - *сумма перевода* <br/>
__create_date__ - *дата перевода* <br/>









