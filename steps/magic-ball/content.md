# Пишем Волшебный шар 

 Сегодня мы напишем нашу первую содержательную программу: программу-игрушку «Волшебный шар». Он подскажет ответ на любой жизненный вопрос. 

А потом разберем самые популярные ошибки в написании программ и узнаем как находить и исправлять ошибки в программах на ruby.

![Магический шар](http://goodprogrammer.ru/system/rich_texts/000/000/109156eec8c804b28fe2d10bd52d5947f55af84937f/1.jpg?1429388853 "Волшебный шар")


<!-- youtube starts here -->
<script>
var videoPlan = {}
</script>

<div class="embed-responsive embed-responsive-16by9 rubyrush-video" id="video-0">
<iframe src="https://www.youtube.com/embed/Y22vv3fG59w" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
<script>
videoPlan["video-0"] = [{"begin":"0:10","comment":"Приветствие и план урока"},{"begin":"0:53","comment":"Предупреждение! Не пытайтесь всё понять сразу!"},{"begin":"1:48","comment":"Самое важное правило программиста"},{"begin":"2:50","comment":"Пишем программу «Волшебный шар»"},{"begin":"7:13","comment":"Культура программирования: комментарии"},{"begin":"8:52","comment":"Культура программирования: разметка кода"},{"begin":"10:06","comment":"Работа с ошибками в ваших программах"},{"begin":"15:34","comment":"Итоги урока"}]
</script>
</div>

 <!-- youtube ends here --> 

### Важнейшее правило программирования

> «Любая программа начинается с постановки задачи».

Вы не можете написать программу, пока вы не поняли, какой результат от неё ждёте. Продумайте вашу программу до того, как её писать. Это во-первых, облегчит вам работу, во-вторых, ваша программа будет содержать меньше ошибок.

Задача для программы «Волшебный шар»:

**Написать программу, которая реализует поведение игрушки волшебный шар.**

Чтобы понять как работает шар, посетим [страницу](https://ru.wikipedia.org/wiki/Magic_8_ball) Википедии, посвященную магическому шару. Она называется «Magic 8 Ball». Нас здесь интересуют все возможные варианты ответов, один из которых случайным образом должна выбрать программа.

### Наша первая программа

Мы создаём, как обычно, папку `lesson3` в нашей рабочей папке c:\rubytut. А в ней уже создадим файл `8ball.rb`, скопировав варианты ответов из Википедии и оформив это в виде массива ruby.

```ruby
answers = [
  # Положительные
  "Бесспорно",
  "Предрешено",
  "Никаких сомнений",
  "Определённо да",
  "Можешь быть уверен в этом",

  # Нерешительно положительные
  "Мне кажется — «да»",
  "Вероятнее всего",
  "Хорошие перспективы",
  "Знаки говорят — «да»",
  "Да",

  # Нейтральные
  "Пока не ясно, попробуй снова",
  "Спроси позже",
  "Лучше не рассказывать",
  "Сейчас нельзя предсказать",
  "Сконцентрируйся и спроси опять",

  # Отрицательные
  "Даже не думай",
  "Мой ответ — «нет»",
  "По моим данным — «нет»",
  "Перспективы не очень хорошие",
  "Весьма сомнительно"
]
```

После этого мы выведем на экран произвольный элемент этого массива с помощью специального метода `sample`.

Добавьте в вашу программу в конце следующую строчку. И сохраните программу в папке урока.

```ruby
puts answers.sample
```

Для того, чтобы запустить эту программу, переходим в консоли в нашу папку

```sh
cd c:\rubytut\lesson3
```

и запускаем программу

```sh
ruby 8ball.rb
```

### Как и зачем писать комментарии (в Ruby и не только)

В Ruby комментарии начинаются с `#` — всё, что идёт после этого символа и до конца строки будет проигнорировано руби. Как будто вы ничего и не писали.

```ruby
# Тут можно писать всякую ерунду ;)
```

Комментарии — очень нужная вещь.

Пишите их, чтобы пояснять действия ваших инструкций в программах для вас в будущем или для других людей, которые будут читать ваши программы.

Очень помогает при обучении прежде, чем писать программу, сначала написать всю программу в виде комментариев на русском языке прямо в файле программы. В этих комментариях просто описать все шаги — что и как делает программа.

### Отступы в программировании

Для удобства восприятия текста программы их авторы используют отступы. Например, если вы пишете блок между скобками или на нескольких строчках, всегда используйте отступы.

Согласитесь, что такой текст читать гораздо сложнее и непонятнее:

```ruby
answers = ['один',
'два',
  'три', 'четыре',
'пять'
]
```

чем такой:

```ruby
answers = [
  'один',
  'два',
  'три',
  'четыре',
  'пять'
]
```

В хорошо отформатированном тексте гораздо проще найти и избежать ошибки. Хотя для ruby оба варианта равнозначны.

Sublime обычно сам подсказывает вам правильные отступы. Но их всегда можно сделать вручную клавишей Tab.

### Ошибки в программировании

Пока вы новичок — ваши программы часто не будут работать с первого раза из-за досадных ошибок и опечаток. Это нормально, все через это проходят.

![Поиск ошибок в программировании](http://goodprogrammer.ru/system/rich_texts/000/000/110560fae80c4a4279c67cbaa633f697e509decdd0e/2.png?1429388853 "Поиск ошибок в программировании")

К счастью большинство таких ошибок довольно просто обнаружить и исправить.
Можно запустить Ruby в режиме проверки файла, добавив к запуску ключ `-c` (параметры с минусами, передаваемые в программу часто называют ключами).

Для этого в консоли (находясь конечно в папке с программой) выполните:

```sh
ruby -c 8ball.rb
```

Забытая скобка, забытая запятая, опечатка в названии переменной или метода — это те причины, по которым ваша программа может даже не запуститься. Ни в коем случае не расстраивайтесь, просто читайте текст ошибок и исправляйте ошибки по одной — сверху вниз.

В тексте ошибки вам не нужно понимать всё, что написано. Достаточно в начале найти название файла и после двоеточия цифру. Эта цифра — номер строки, где обнаружена ошибка.

Но обратите внимание, что ошибка может оказаться не ровно на этой строке, а плюс-минус одна строка (пустые строки и комментарии не учитываются!).

Если же плюс–минус одна строка в порядке, то возможно ошибку следует искать в симметричной конструкции. Например, если ошибка в районе строки, где есть символ `}` или `]`, или `)`, то возможно дело в том, что для этой закрывающей скобки нету открывающей. На какой-то совсем другой строке, где она должна быть по смыслу вашей программы.

Точно также ошибки могут проявиться и без всяких ключей, при обычном запуске программы. Искать и исправлять их нужно точно также – по одной, всегда сначала самую верхнюю из списка ошибок. Бывает, что исправление одной самой верхней ошибки автоматически исправляет и все остальные.

После того, как мы написали нашу первую более-менее сложную программу и научились делать разметку и комментарии в тексте программ, а также бороться с опечатками в Ruby — можно переходить к изучению основ программирования.

В следующем уроке мы расскажем вам о переменных в Ruby и операторе if-else.

