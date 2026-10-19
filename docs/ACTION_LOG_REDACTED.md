# Журнал действий — WIP-DEFENSE-06

## Правила статусов

- `prepared` — документ подготовлен, не отправлен.
- `sent` — отправлен, подтверждение отправки отсутствует или приложено.
- `registered` — присвоен входящий номер.
- `attached` — приобщён к материалам дела.
- `response_received` — получен ответ.

## Записи

| date/time | action | recipient | reference | sent? | registered? | outcome | proof_file | next_step | deadline | owner | verified_by | updated_at |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| 2026-10-15 | Фотофиксация материалов дела | — | — | no | no | USER_REPORTED | — | Локальный разбор | 2026-10-19 | USER | — | 2026-10-19 |
| 2026-10-16 | Ходатайство № 31808/2026 | Суд | 31808/2026 | yes | yes | Доступ к делу предоставлен | NEEDS_IMPORT | Проверить содержание | 2026-10-26 | USER | — | 2026-10-19 |
| 2026-10-16 12:44:44 | Документ суда № 32403/2026 | Суд | 32403/2026 | yes | yes | USER_REPORTED: приобщён к делу 02-5004/2026 | NEEDS_IMPORT | Проверить, что именно приобщено | 2026-10-26 | USER | — | 2026-10-19 |
| 2026-10-16 13:02 | Запрос в «INSURER» | АО «ГСК «INSURER» | 01-03/114788-26 | yes | yes | Зарегистрирован | NEEDS_IMPORT | Ждать ответ; готовить дополнение | 2026-10-26 | USER | — | 2026-10-19 |
| 2026-10-19 | Дополнение к запросу в «INSURER» | АО «ГСК «INSURER» | 01-03/114788-26 addendum | yes | no | SENT; дата отправки TO_BE_CONFIRMED; ответ PENDING | NEEDS_IMPORT | WAIT_FOR_RESPONSE; подтвердить дату и номер регистрации | 2026-10-26 | USER | — | 2026-10-19 |
| 2026-10-26 09:10 | Судебное заседание | Тимирязевский районный суд | 02-5004/2026 | — | — | scheduled | Повестка: IMG_20261016_120834.jpg | Подготовить возражения и ходатайства | 2026-10-26 | USER | — | 2026-10-19 |

## INSURER_ADDENDUM

```yaml
INSURER_ADDENDUM:
  status: SENT
  sent_date: TO_BE_CONFIRMED
  response_status: PENDING
  registration_number: UNKNOWN
  next_action: WAIT_FOR_RESPONSE
```
