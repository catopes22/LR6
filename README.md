# **LR6**

## Лабораторная работа №6
## Система контроля версий

**Цель лабораторной работы:**
изучение базовых возможностей системы управления версиями, опыт работы с Git Api, опыт работы с локальным и удаленным репозиторием.

------------

## Ход работы
1. Создаётся аккаунт на сайте GitHub

    ![1.png][def]
2. Была сделана копия репозитория https://github.com/Kurtyanik/LR6/ в личное хранилище (fork).

    ![1.png](./assets/1.png)
    ![2.png](./assets/2.png)
3. Git уже был установлен.

    ```console
    git --version
    ```
    Версия git:
    
    ![3.png](./assets/3.png)
4. Был настроен клиент git *(было введено имя пользователя и email)*.

    ```console
    git config --global user.name "4118 Горожанкин А.А."
    git config --global user.email "rememberov.andrei@yandex.ru"
    ```
    ![4.png](./assets/4.png)
5. Личный удалённый репозиторий был склонирован на компьютер.

    ```console
    git clone https://github.com/FugiOG/LR6.git
    ```
    ![5.png](./assets/5.png)
6. Был добавлен новый файл в репозиторий через интерфейс GitHub, затем изменения были подтянуты в локальный репозиторий.

    ![6.png](./assets/6.png)
    ![7.png](./assets/7.png)
    ```console
    git branch
    git pull
    ```
    ![8.png](./assets/8.png)
7. Была получена история операций для каждой из веток.

    ```console
    git log
    ```
    ![9.png](./assets/9.png)
    ```console
    git checkout branch1
    git log
    ```
    ![10.png](./assets/10.png)
8. Были просмотрены последние изменения.

    ```console
    git status
    ```
    ![11.png](./assets/11.png)
9.  Было выполнено слияние в ветку master с разрешением конфликтов при помощи графического интерфейса.

    ```console
    git branch
    git merge branch1
    ```
    ![12.png](./assets/12.png)
    ![13.png](./assets/13.png)
    ```console
    git status
    ```
    ![14.png](./assets/14.png)
    ```console
    git add .
    git commit -m "merge conflict resolution"
    ```
    ![15.png](./assets/15.png)
10. После слиянияю, была удалена побочная ветка.

    ```console
    git branch -d branch1
    git branch
    ```
    ![16.png](./assets/16.png)

    Также была удалена побочная ветка из удалённого репозитория:

    ```console
    git push origin -d branch1
    ```
    ![28.png](./assets/28.png)
11. Были сделаны и зафиксированы изменения, при этом были 3 раза оставлены коментарии.

    ```console
    git status
    ```
    ![17.png](./assets/17.png)

    ```console
    git add .
    git commit -m "feat: add greeting SUAI"
    ```
    ![18.png](./assets/18.png)

    ```console
    git add .
    git commit -m "feat: add greeting 4118"
    ```
    ![19.png](./assets/19.png)

     ```console
    git add .
    git commit -m "feat: add mathematical calculation"
    ```
    ![20.png](./assets/20.png)

    Итоговый вид файла:

    ![21.png](./assets/21.png)
12. Был сделан откат коммита.

    последние коммиты в ветке master до удаления:
        ![22.png](./assets/22.png)

    ```console
    git reset --hard HEAD~
    ```
    ![23.png](./assets/23.png)

    последние коммиты в ветке master после удаления:
        ![24.png](./assets/24.png)
    
    Итоговый файл после отката:

    ![25.png](./assets/25.png)
13. Была создана ветка для отчёта.

    ```console
    git branch
    git branch report
    git branch
    git checkout report
    git branch
    ```
    ![26.png](./assets/26.png)
14. Была получена история операций в форматированном виде *(сокращённый хэш | дата коммитера | имя автора: комментарий)*.

    ```console
    git log --pretty=format:"%h | %cd | %an: %s"
    ```
    ![27.png](./assets/27.png)

--------

## Вывод: 
В ходе данной лабораторной работы были изучены базовые возможности системы управления версиями; был получен опыт работы с Git Api, также был получен опыт работы с локальным и удаленным репозиторием.

[def]: ./images/1.png