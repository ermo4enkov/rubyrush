# Магазин, заготовка 

Напишите заготовку для небольшого магазинчика, который торгует фильмами и книгами. 

Создайте класс продукта, у экземпляров которого есть два поля: **цена** и **количество на складе**. При создании нового продукта можно передать значения цены и остатка. Для этих переменных сделайте геттеры.

Унаследуйте от этого класса два других: **книгу** и **фильм** соответственно. Своих переменных у этих классов пока нет.

Создайте в основной программе какой-нибудь продукт, например «фильм Леон». Выведите его стоимость в консоль.

```
Фильм Леон стоит 290 руб.
```

Создайте для этой программы локальный репозиторий. Мы к ней ещё вернёмся.

<div class="rubyrush-task-hint">

Создайте классы `Product`, `Movie` и `Book`, каждый в своём файле соответственно (не забудьте положить файлы классов в папку `lib`). 

2-й, 3-й классы отнаследуйте от класса продукта. Напишите у класса продукта конструктор `initialize(params)`, который принимает на вход ассоциативный массив `params` и записывает в поля значения своих аргументов, доставая их по соответствующим ключам.

Потом подключите эти файлы в основную программу с помощью `require_relative` и создайте фильм.

Например, так:

```ruby
movie = Movie.new(price: 290, amount: 4)
```

</div>


<div class="rubyrush-task-answer">

<p>
<a href="https://github.com/aristofun/rubyrush-path/tree/master/steps/classes-inheritance-02/solution/store/" class="rubyrush-task-solution-link">Вариант решения задачи</a>
</p>

</div>
