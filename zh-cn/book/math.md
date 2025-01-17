# 算数

有时当你在做一个任务时，需要将一些数加起来。 Nu 提供了一些基本的算数操作：

要进入 「算数模式」，你需要用 `=` 作为命令的开头。这让 Nu 知道你将要使用一些操作符。一些命令，例如 `where` 将会自动为你执行此操作，因此不必主动去做。

## 加减乘除

```
> = 1 + 3
4
```

在 Nu，你可以使用通常的加减乘除运算符 `+-*/`。运算符的优先级遵循惯例，所以 `1 + 2 * 3` 和 `1 + (2 * 3)` 等效。也可以用括号手动调整优先级。

## 括号

在算数模式中可以使用括号来将表达式分组，这允许你手动将某个表达式的运算优先级提高，例如 `(1 + 2) * 3` 中的加法表达式的优先级将高于乘法。

## `in` 和 `not-in`

你可以使用 `in` 和 `not-in` 运算符来检查某个值是否在一个集合中。

```
> = 1 in [1 2 3]
true
```

```
> = 1 not-in [1 2 3]
false
```

## =~ 和 !~

你可以使用 `=~` 和 `!~` 来检查某个字符串是否是另一个字符串的子串。

```
> = "foobar" =~ "foo"
true
```

```
> = "foobar" !~ "baz"
true
```

## 比较

以下是可用的比较运算：

- `<` - 小于
- `<=` - 小于等于（不大于）
- `>` - 大于
- `>=` - 大于等于（不小于）
- `==` - 等于
- `!=` - 不等于

## 复合运算符

Nushell 也提供 `&&` 和 `||` 来将两个返回布尔值的运算连接在一起，分别表示 「且」和 「或」。例如 `ls | where name in ["one" "two" "three"] && size > 10kb`。
