# Лабораторная работа 
## Тема: автоматизация задач, с использованием cron
#### Немного теории
cron используется для автоматизации регулярных операций в системе, таких как бэкап файлов, удаление старых логов и мониторинг состояния системы, но его можно настроить 
и для чего-то менее серьезного;)

Для просмотра вашего файла 
```
crontab -l
```
Для создания нового задания
```
crontab -e
```
После этого откроется файл для редактирования, подробнее про синтаксис можно посмотреть в дополнительных источниках, приложенных ниже

Для удаления всех заданий 
```
crontab -r
```

### Задание 0 (для примера) 
Немобходимо настроить cron так, чтобы каждую минуту в файл записывалось текущее время(то есть у нас получится файл-часы) 

1. Открываем файл crontab для редактирования:
```
crontab -e
```
2. Добавляем задачу в файл crontab
```
* * * * * date '+\%Y-\%m-\%d \%H:\%M:\%S' >> /<путь к файлу, в который будем записывать время>/time
```
Выходим из редактора

3. Теперь мы можем проверить, добавилась ли наша задача
```
crontab -l
```
в терминале должна появиться строчка, которую мы добавляли в файл crontab
если она есть, значит все получилось

4. Теперь откроем файл time
```
cat /<путь к файлу, в который будем записывать время>/time
```
в терминале будет что-то подобное:

<img width="147" alt="image" src="https://github.com/user-attachments/assets/ec3dc557-d6ed-4a55-96e9-a31c4feedc82" />

Либо, если мы откроем файл, как файл:

<img width="158" alt="image" src="https://github.com/user-attachments/assets/e2a038ba-4ae6-43e7-9ab7-92def56a4f9c" />


### Задание 1 (основное)
Напишите Bash-скрипт CronManage.bash, который будет добавлять и удалять задачи из crontab. Должны быть реализованы команды:
- add - для добавления задачи

если дан доступ к исполнению:
```
/<путь к файлу>/CronManage.bash add 
```

если нет:
```
bash CronManage.bash add
```
- remove - для удаления задачи

если дан доступ к исполнению:
```
/<путь к файлу>/CronManage.bash remove
```

если нет:
```
bash CronManage.bash remove
```
Это пример того, как может запускаться скрипт, возможена другая реализация,
но должна быть возможность самостоятельно задавать задачи, 
то есть файл CronManage.bash должен быть универсальным, а не добавлять только те задачи, которые вы напишите внутри!
Удачи!


### Как успешно сдать работу?
В своем репозитории для лабораторных работ создайте папку для этой лабораторной работы ```All_labs/this_lab/отчет.md``` и оформите отчет, который должен включать в себя
шаги выполнения, которые вы делали для получения финального результата

Что нужно знать для защиты: 
что такое cron, для чего он используется, основные команды, синтаксис для зааписи задач, ориентироваться в своем bash скрипте

### Ресурсы, которые могут пригодиться:
1) [ответы на все вопросы](https://www.google.ru/)
2) [Настройка Cron](https://losst.pro/nastrojka-cron)
3) [Documentation](https://rockylinux-docs.vercel.app/de/guides/automation/cron_jobs_howto/)
4) [How to Automate Tasks in Ubuntu with Terminal and Cron Jobs](https://medium.com/@AlexanderObregon/how-to-automate-tasks-in-ubuntu-with-terminal-and-cron-jobs-51897a5c2918)

