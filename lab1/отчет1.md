## Лабораторная работа 1 Отчет

1. Я создаю новый файл с именем `script.bash`, использую touch <имя файла>

![image](https://github.com/user-attachments/assets/ebd85eae-c015-4f49-a3ec-a62b3230d693)

2. Далее открываю созданный файл `script.bash` для редактирования, использую для этого nano <имя файла>
<img width="571" alt="image" src="https://github.com/user-attachments/assets/189653c8-fff7-43bd-b3d6-3a7a6d1c1c9e">
<img width="565" alt="image" src="https://github.com/user-attachments/assets/a4bff7bb-0a14-43ca-af74-e26657c6c549">

3. Вписываю следующий скрипт:
<img width="560" alt="image" src="https://github.com/user-attachments/assets/44a96d33-8e90-45c5-93ca-e964467e4549">

Скрипты bash начинаеются с shebang(bash # и bang !), за которыми следует путь оболочки bash: /bin/bash
поэтому первая строка: #!/bin/bash

Далее пишу команду echo, которая выводит на терминал строку текста или значение переменой(или все вместе)

5. Сохраняю (^O), выхожу из nano (^X)

6. Запускаю bash-скрипт

<img width="564" alt="image" src="https://github.com/user-attachments/assets/aead5496-6da9-4ba2-8e34-e3fc4b3b4fcb">

Получаю результат



Теперь непосредственно задача.
### Задача
Текст задачи:
Модифицируйте файл `script.bash` так, чтобы при его запуске в терминале в виде

```bash
bash script.bash Vasya Pupkin
```

Вывод был

`Welcome, Vasya Pupkin`

*Hint:* Скрипт должен работать для любых имен, даже если это Benedict Timothy Carlton Cumberbatch.


Решение:
1. Снова открываю редактирование файла через nano <имя файла>
<img width="561" alt="image" src="https://github.com/user-attachments/assets/b9b694ab-d8bd-4f56-8705-39d66ce96c9b">

Редактирую надпись(первую строку не трогаю), использую $@, мне необходим '$', чтобы получить доступ к значению переданных аргументов(рассматриваю случай, где их несколько, но с одним тоже будет работать), @ - значения всех аргументов, переданных скрипту

<img width="565" alt="image" src="https://github.com/user-attachments/assets/0c5af86b-10e1-4e8d-a714-a36167cf7f30">

далее сохраняю и выхожу из nano

3. Запускаю скрипт:
<img width="561" alt="image" src="https://github.com/user-attachments/assets/4cd36f67-15e6-43a5-bcc5-34abc2a24b42">

Проверка для другого имени:

<img width="560" alt="image" src="https://github.com/user-attachments/assets/2e33d463-ae27-44c5-b0bb-61264af5669a">

Проверка, если аргумент один:

<img width="568" alt="image" src="https://github.com/user-attachments/assets/2ef359b9-ccc5-46aa-abb5-ec9001ddd2da">

Все работает

