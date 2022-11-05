# **LR6**

## Лабораторная работа №6
## Система контроля версий

**Цель лабораторной работы:**
изучение базовых возможностей системы управления версиями, опыт работы с Git Api, опыт работы с локальным и удаленным репозиторием.

------------

## Ход работы
1. Создаётся аккаунт на сайте GitHub

    ![1.png](./images/1.png)
2. Была сделана копия репозитория https://github.com/Kurtyanik/LR6/ в личное хранилище (fork).

    ![2.png](./images/2.png)
3. Устанавливается Git.
    
    ![3.png](./images/3.png)
4. Настройка клиента Git, вводится имя пользователя и email.

    ```console
    git config --global user.name "4118 Кужлев А.А."
    git config --global user.email "kuzhlev.artem@mail.ru"
    ```
    ![4.png](./images/4.png)
5. Личный удалённый репозиторий клонируется на компьютер.

    ```console
    git clone https://github.com/catopes22/LR6.git
    ```
    ![5.png](./images/5.png)
6. Был добавлен текстовый файл task6.txt в репозиторий через интерфейс GitHub, затем изменения были подтянуты в локальный репозиторий.

    ![6.png](./images/6.png)
    ```console
    git branch
    git pull
    ```
    ![6.1.png](./images/6.1.png)
    ![6.2.png](./images/6.2.png)
7. Была получена история операций для каждой из веток.

    ```console
    git log
    ```
    ![7.png](./images/7.png)
    ```console
    git checkout branch1
    git log
    ```
    ![7.1.png](./images/7.1.png)
8. Были просмотрены последние изменения.

    ```console
    git status
    ```
    ![8.png](./images/8.png)
    ![8.1.png](./images/8.1.png)
9.  Было выполнено слияние в ветку master с разрешением конфликтов при помощи графического интерфейса Visual Studio Code.

    ```console
    git merge branch1
    ```
    ![9.png](./images/9.png)
    ```console
    git add mergefile.txt
    git commit -m "merged master fixed conflict"
    ```
    ![9.1.png](./images/9.1.png)
    ![9.2.png](./images/9.2.png)
    ![9.3.png](./images/9.3.png)
    ![9.4.png](./images/9.4.png)
10. Удаляется побочная ветка.

    ```console
    git branch -d branch1
    ```
    ![10.png](./images/10.png)
11. Были сделаны и зафиксированы изменения c 3 комментариями.

    ```console
    git add .
    git commit -m "feat: add greetings SUAI"
    ```
    ![11.png](./images/11.png)

    ```console
    git add .
    git commit -m "feat: add hello 4118"
    ```
    ![11.1.png](./images/11.1.png)

     ```console
    git add .
    git commit -m "feat: add equation"
    ```
    ![11.2.png](./images/11.2.png)

    Вид файла task6.txt:

    ![11.3.png](./images/11.3.png)
12. Был сделан откат коммита.

    Коммит, который будет удалён:
    ![12.png](./images/12.png)

    ```console
    git reset --hard HEAD~
    ```
    ![12.1.png](./images/12.1.png)

    Файл task6.txt после отката:

    ![12.2.png](./images/12.2.png)
13. Была создана ветка report для отчёта.

    ```console
    git branch
    git branch report
    ```
    ![13.png](./images/13.png)
14. Была получена история операций в форматированном виде *(сокращённый хэш | дата коммитера | имя автора: комментарий)*.

    ```console
    git log --pretty=format:"%h | %cd | %an: %s"
    ```
    ![14.png](./images/14.png)
 
--------

## Вывод: 
В ходе данной лабораторной работы были изучены базовые возможности системы управления версиями, был получен опыт работы с Git Api и с локальным и удаленным репозиторием.