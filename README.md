# LR6
Лабораторная работа №6

В самом начале создаем копию репозитория в личное хранилище репозиторий: https://github.com/Kurtyanik/LR6/.

![image](https://user-images.githubusercontent.com/116668932/199715394-bb9760d2-e36d-45b8-ba79-ba5b203cb48d.png)

Далее используем команды git config --global user.name и git config --global user.email для настройки клиента Git и вводим свои данные от GitHub.

![image](https://user-images.githubusercontent.com/116668932/199715998-55ac8d18-73e0-4ae5-8999-8c87c2dfcbee.png)

Клонируем удаленный репозиторий, используя команду git clone.

![image](https://user-images.githubusercontent.com/116668932/199716100-1a397d8a-03d3-47e0-bddc-b80db04eae7a.png)

Добавим файл через интерфейс GitHub. Далее переходим в директорию LR6 командой cd LR6 для дальнейшей работы с файлами.

![image](https://user-images.githubusercontent.com/116668932/199716178-ba113cf8-da40-461d-a661-71c565fd17c5.png)

Подтянем изменения из веб-интерфейса GitHub для клиента Git. Для этого используем команду git pull.

![image](https://user-images.githubusercontent.com/116668932/199716225-3201000e-a66f-4409-9548-2a58a83d6653.png)

Посмотрим коммиты ветки master, используя команду git log.

![image](https://user-images.githubusercontent.com/116668932/199716297-137a760f-73a3-4944-b682-655b67bcdfe6.png)

Просмотрим существующие ветки в текущем репозитории командой git branch.

![image](https://user-images.githubusercontent.com/116668932/199716363-3b1416b2-e899-4032-838d-58805183bd69.png)

Перейдем в ветку branch1 командой git checkout branch1.

![image](https://user-images.githubusercontent.com/116668932/199716412-5f1ff9cf-0c05-48d2-9fbc-b07fdbd78ad7.png)

Посмотрим коммиты ветки branch1 с помощью команды git log.

![image](https://user-images.githubusercontent.com/116668932/199716491-6ebc50d4-04ff-43a9-9e8e-80c664227c87.png)

Рассмотрим коммиты с помощью команды git log -p.

![image](https://user-images.githubusercontent.com/116668932/199716555-94315684-e9c7-47db-a5a0-4119d09ebd32.png)

![image](https://user-images.githubusercontent.com/116668932/199716592-6ebf6505-36c5-425c-8b88-921eccd07ac1.png)

Вернемся в ветку master.

![image](https://user-images.githubusercontent.com/116668932/199716688-5a3042d5-51d1-4733-95c1-806486d17fd7.png)

Выполним слияние в ветку master. Слияние производится при помощи команды git merge branch1.

![image](https://user-images.githubusercontent.com/116668932/199716732-a7e194d9-4e48-4910-aba9-8520c3d5b75e.png)

Произошел конфликт. Вероятно, что файл mergefile.txt не отслеживается. Используем команду git status.

![image](https://user-images.githubusercontent.com/116668932/199716780-914ca47a-4c74-4ecb-b81d-b0dbc892a9b4.png)

Так и оказалось. Добавим файл для отслеживания командой git add mergefile.txt.

![image](https://user-images.githubusercontent.com/116668932/199716818-60269576-e521-4c94-ad06-eee1094bd532.png)

Проверим еще раз, отслеживается ли файл.

![image](https://user-images.githubusercontent.com/116668932/199716874-fb99da4e-5722-4acd-b1b0-8f673cebb11c.png)

Конфликт разрешен, оставляем коммит при помощи команды git commit -m "Branches".

![image](https://user-images.githubusercontent.com/116668932/199716933-4c9e09fc-cedd-4342-9fa2-95ac85de1959.png)

Удаляем побочную ветку после успешного слияния при помощи команды git branch -d branch1.

![image](https://user-images.githubusercontent.com/116668932/199716981-d044bf57-39ff-4566-a919-c9a0de0ddb32.png)

Создадим изменения и комментарии для них. Создавать будем текстовые файлы прямо в терминале. Для создания текстовика используем команду echo hello > change1.txt, зафиксируем его git add change1.txt. Оставим комментарий git commit -m "Change1.txt". Повторим все то же самое еще раз, только название указываем другое - change2.txt.

![image](https://user-images.githubusercontent.com/116668932/199717038-9f102750-b6bd-4eec-a7bf-2e727dcf1e9d.png)

Посмотрим комментарии.

![image](https://user-images.githubusercontent.com/116668932/199717114-1731c6c2-d56b-4ef1-8d27-8af29ffa41b6.png)

Теперь сделаем "хард" откат коммита. Вводим git reset --hard HEAD~1.

![image](https://user-images.githubusercontent.com/116668932/199717178-2ec4fac0-b9e1-45d9-a85e-badc7c528fa6.png)

Создадим ветку для отчета и перейдем в нее, вводя команду git branch report.

![image](https://user-images.githubusercontent.com/116668932/199717224-a7e1d530-ed40-4f76-a196-87841c15c403.png)

Получим итоговую историю операций.

![image](https://user-images.githubusercontent.com/116668932/199717284-75c90e21-4e2f-44a3-a760-7fab11fe3c22.png)

После редактирования отчета, его нужно будет сохранить и произвести команды git add и git commit. В конце работы необходимо будет отправить все локальные изменения в сетевое хранилище GitHub командой git push.
