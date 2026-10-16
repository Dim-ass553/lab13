ЗВІТ
до Лабораторної роботи №13
з дисципліни «Веб-програмування»
Студент: Ларін Д. А.
Група: КН-924б
Варіант: №5

Тема: Система контролю версій Git
Мета: Ознайомитися з основами системи контролю версій Git та вивчити базові команди для роботи з нею.

СПИСОК ВИКОНАНИХ КОМАНД ТА КРОКІВ:

1. Налаштування глобальних параметрів:
   git config --global user.name "Dmytro"
   git config --global user.email "dimonlarin553@gmail.com"

2. Генерація та налаштування SSH-ключа:
   ssh-keygen -t ed25519 -C "dimonlarin553@gmail.com"
   cat ~/.ssh/id_ed25519.pub
   ssh -T git@github.com

3. Ініціалізація локального репозиторію та перший коміт:
   git init
   echo "# Лабораторна робота №13" > README.md
   git add README.md
   git commit -m "Initial commit"

4. Робота з гілкою feature-text:
   git checkout -b feature-text
   echo "Додатковий текст у гілці feature-text" >> README.md
   git add README.md
   git commit -m "Update text file"

5. Робота з гілкою feature-image:
   git checkout master
   git checkout -b feature-image
   echo "test image data" > picture.png
   git add picture.png
   git commit -m "Add image file"

6. Злиття гілок у головну гілку main:
   git checkout master
   git merge feature-text
   git merge feature-image
   git branch -M main

7. Відправка змін на GitHub:
   git remote add origin git@github.com:Dim-ass553/lab13.git
   git push -u origin main

Висновок: Оволодіно практичними навичками роботи з розподіленою системою контролю версій Git та сервісом GitHub. Реалізовано авторизацію за допомогою SSH-ключів, створення гілок, фіксацію змін, злиття гілок (merge) та відправку результатів на віддалений репозиторій.
