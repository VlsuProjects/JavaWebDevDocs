# [**Назад**: *Синтаксис Thymeleaf*](../features/thymeleaf-syntax.md)

# Условия в Thymeleaf

Условия в Thymeleaf позволяют вам встраивать динамический контент в ваши HTML-шаблоны в зависимости от определенных условий.

Существует несколько типов операторов условий в Thymeleaf, которые позволяют вам проверять различные условия и встраивать контент в зависимости от их результатов:
- `th:if` - встраивает контент, если условие истинно
- `th:unless` - встраивает контент, если условие ложно
- `th:switch` - аналог оператора `switch` в Java

Условия используют стандартные операторы сравнения с некоторыми усложнениями:
- `==` - равно, нельзя использовать для сравнения контента строк, только для примитивных типов
- `!=` - не равно
- `<` - меньше
- `>` - больше
- `<=` - меньше или равно
- `>=` - больше или равно
- `and` или `&&` - логическое "и", используется между условиями для проверки их обоих
- `or` или `||` - логическое "или", используется между условиями для проверки хотя бы одного из них
- `not` - логическое "не", используется перед условием для проверки его отрицания
- `empty` - проверяет, пуста ли переменная или коллекция
- `!empty` - проверяет, не пуста ли переменная или коллекция
- `isEven` - проверяет, является ли число четным
- `isOdd` - проверяет, является ли число нечетным
- `isDivisibleBy` - проверяет, делится ли число на другое без остатка
- `isNotDivisibleBy` - проверяет, не делится ли число на другое без остатка
- `matches` - проверяет, соответствует ли строка регулярному выражению
- `startsWith` - проверяет, начинается ли строка с указанной подстроки
- `endsWith` - проверяет, заканчивается ли строка указанной подстрокой
- `contains` - проверяет, содержит ли строка указанную подстроку
- `equals` - проверяет, равны ли две строки
- `equalsIgnoreCase` - проверяет, равны ли две строки без учета регистра
- на самом деле их больше, - это основные

Простой пример использования условий `if` и `unless` в Thymeleaf, в котором мы проверим, что переменная не равна 5, и если это условие истинно, то выведем сообщение "Переменная не равна 5", в противном случае - выведем сообщение "Переменная равна 5":

```html
<div th:if="${variable != 5}">
    <p>Переменная не равна 5</p>
</div>
<div th:unless="${variable != 5}">
    <p>Переменная равна 5</p>
</div>
```

В этом примере мы использовали `th:if` и `th:unless` для проверки условий и встраивания контента в зависимости от их результатов. Также, вместо `th:unless` можно использовать `th:else`, чтобы встраивать контент, если условие ложно:

```html
<div th:if="${variable != 5}">
    <p>Переменная не равна 5</p>
</div>
<div th:else>
    <p>Переменная равна 5</p>
</div>
```


# [**Назад**: *Синтаксис Thymeleaf*](../features/thymeleaf-syntax.md)
