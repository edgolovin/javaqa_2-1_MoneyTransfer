# Отчёт о тестировании приложения "MoneyTransfer"

## Краткое описание

При пополнении счёта VIP-клиента что-то пошло не так. \
Входные данные:
* текущий баланс счёта клиента - переменная типа int, значение - 2_000_000_000 (два миллиарда рублей)
* сумма перевода - переменная типа int, значение - 500_000_000 (пятьсот миллионов рублей)
* переменная для хранения итогового значения - тип int

Для воспроизведения ситуации было создано базовое приложение, в соответствии с входными данными. \
Значение итоговой переменной должно составлять 2_500_000_000 (два миллиарда пятьсот миллионов рублей).\
Вместо этого в переменной находится значение 
`-1794967296`.

## Описание тестов

Создано базовое приложение для воспроизведения ситуации с входными данными. Приложение действительно выдаёт неожиданный результат, вследствие чего можно говорить об успешном воспроизведении ситуации. Проведено позитивное тестирование, результат отрицательный.

## Результаты

1. 100% неуспешных тестов
1. Заведён баг-репорт [Issue #1](https://github.com/edgolovin/javaqa_2-1_MoneyTransfer/issues/1)

## Общие рекомендации

Произошло переполнение типа `int` переменной `final_user_deposit`. Необходимо изменить тип переменной на больший по рангу.
