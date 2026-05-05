# Примеры программ

Примеры лежат в каталоге `examples/`.

## factorial.fun

```bash
dotnet run --project src -- examples/factorial.fun
# 120
```

Проверяет `letrec`, `if`, арифметику и рекурсию.

## fibonacci.fun

```bash
dotnet run --project src -- examples/fibonacci.fun
# 55
```

Проверяет двойную рекурсию.

## closures.fun

```bash
dotnet run --project src -- examples/closures.fun
# 8
```

Проверяет лексические замыкания.

## lists.fun

```bash
dotnet run --project src -- examples/lists.fun
# 15
```

Проверяет операции со списками и рекурсивную обработку.

## higherOrder.fun

```bash
dotnet run --project src -- examples/higherOrder.fun
# (1 4 9 16 25)
```

Проверяет функции высшего порядка.

## lazy-basic.fun

```bash
dotnet run --project src -- examples/lazy-basic.fun
# "addition"
# 42
# 42
# "addition"
# 3
# 3
```

Проверяет вызываемый thunk с memoization по аргументам.

## lazy-stream.fun

```bash
dotnet run --project src -- examples/lazy-stream.fun
# 3
```

Проверяет ленивый хвост списка и последовательное `force`.

## file-io.fun

```bash
dotnet run --project src -- examples/file-io.fun
# "funky-io-ok"
```

Проверяет `writeFile` и `readFile`.

## file-io-error.fun

```bash
dotnet run --project src -- examples/file-io-error.fun
# Runtime error: readFile failed for 'examples/does-not-exist.txt': ...
```

Проверяет диагностику I/O-ошибок.
