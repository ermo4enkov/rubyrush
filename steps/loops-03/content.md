# Проверка ввода пользователя 

Возьмите вашу игру, которую вы сделали в домашнем задании к уроку про «южное бутово» (если не делали — самое время сделать). В этой игре теперь защитите программу от неправильного ввода вариантов.

То есть если программа просит выбрать `1. ... 2. ... 3. ...`, а пользователь вводит `7` или вообще посторонние символы, то программа повторяет свой вопрос и не продолжается пока не будет введен один из доступных вариантов.

<div class="rubyrush-task-hint">

Нужно везде, где программа делает выбор по какому варианту пойти, перед конструкцией типа `if choice == ...` вставить циклическую проверку введенных данных.

Для проверки выполнения одного из нескольких условий цикла используйте оператор `||` – «ИЛИ».

Подробнее об «ИЛИ» читайте текстовую версию четвертого урока.

</div>


<div class="rubyrush-task-answer">


<ul>
<li><a href="https://github.com/aristofun/rubyrush-path/blob/master/steps/loops-03/solution/user_choice.rb" class="rubyrush-task-solution-link">Наш вариант решения</a></li></ul>

</div>
