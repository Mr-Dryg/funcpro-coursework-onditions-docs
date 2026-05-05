# Ошибки и формат сообщений

Интерпретатор разделяет ошибки по этапам обработки.

## Общий формат

Ошибки выводятся в `stderr`, процесс завершается с ненулевым кодом.

Примеры префиксов:
- `Parse error: ...`
- `AST error: ...`
- `Runtime error: ...`

Лексические ошибки выводятся как есть (сообщение `LexError`).

## Типовые runtime-ошибки

- обращение к неопределенной переменной:
  - `Runtime error: unbound variable: <name>`
- неверный тип условия в `if`:
  - `Runtime error: if: condition must be bool, got <value>`
- вызов не-функции:
  - `Runtime error: cannot call non-function: <value>`
- неверная арность:
  - `Runtime error: arity mismatch: expected N args, got M`
- деление на ноль:
  - `Runtime error: division by zero`
- ошибки операций списка:
  - `Runtime error: head: empty list`
  - `Runtime error: tail: empty list`

## Ошибки запуска

- отсутствует аргумент пути:
  - печатается usage, код завершения `2`;
- файл не найден:
  - `Error: file not found: <path>`, код завершения `1`.
