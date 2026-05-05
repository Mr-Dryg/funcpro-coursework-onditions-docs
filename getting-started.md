# Быстрый старт

## Требования

- .NET SDK 10

## Сборка

```bash
dotnet build src/Funky.fsproj
```

## Запуск интерпретатора

```bash
dotnet run --project src -- <path-to-.fun-file>
```

Пример:

```bash
dotnet run --project src -- examples/factorial.fun
# 120
```

## Что делает CLI

Pipeline выполнения:

`source -> tokenize -> parse -> toAst -> eval initialEnv -> formatValue`

CLI печатает результат вычисления каждого top-level выражения.

## Коды завершения

- `0` — успешное выполнение;
- `1` — ошибка обработки файла/лексера/парсера/AST/runtime;
- `2` — неправильные аргументы запуска.
