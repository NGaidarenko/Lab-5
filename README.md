# Лабораторная работа №5
## Задача
#### Интегрировать Git Flow в проект для управления циклом разработки, создания релизов и управления hotfixes.
## Решение
#### Убедимся, что Git Flow установлен на локальной машине используя команду `sudo apt-get install git-flow`, получим:
![](https://github.com/NGaidarenko/Lab-5/blob/main/image_lab_5/install_git_flow.jpg)
#### 
#### Выполним инициализацию Git Flow, командой `git flow init`, получим:
![](https://github.com/NGaidarenko/Lab-5/blob/main/image_lab_5/git_flow_init.jpg)
####
#### Создадим ветку для новой функциональности "task-management", при помощи команды `git flow feature start task-management`, получим:
![](https://github.com/NGaidarenko/Lab-5/blob/main/image_lab_5/start_task_management.jpg)
#### 
#### Создадим файл task_manager.py и изменим файл при помощи команд:
```
touch task_manager.py
gedit task_manager.py
```
Запиши в этот файл следующую функцию:
```
def create_task(title, description):
    # Логика создания задачи
    print(f"Создана новая задача: {title}")
```
После выполним коммит, получим:
![](https://github.com/NGaidarenko/Lab-5/blob/main/image_lab_5/commit_py_file.jpg)
#### 
#### Объеденим с основной веткой при помощи команды `git flow feature finish task-management`, получим:
![](https://github.com/NGaidarenko/Lab-5/blob/main/image_lab_5/finish_task_management.jpg)
#### 
#### Переключимся на ветку "develop" и начнем создание релиза при помощи команд:
```
git checkout develop
git flow release start v1.0.0
```
Получим:
![](https://github.com/NGaidarenko/Lab-5/blob/main/image_lab_5/start_v1.0.0.jpg)
#### 
#### Внесем изменения связанные с релизом, используя следующие команды:
```
echo "v1.0.0" > version.txt
git add version.txt
git commit -m "Обновлена версия для релиза v1.0.0"
```
Получим:
![](https://github.com/NGaidarenko/Lab-5/blob/main/image_lab_5/create_version_file.jpg)
#### 
#### Отправьте изменения на удаленный репозиторий при помощи команд:
```
git push origin develop
git push origin main
```
Получим:
![](https://github.com/NGaidarenko/Lab-5/blob/main/image_lab_5/push.jpg)
#### 
## Вывод:
#### Интегрировали Git Flow в проект для управления циклом разработки, созданием релизов.


