# Шпаргалочка
"# Работа с ветками

 **bash**
_Есть master (публичная версия сайта), хотим масштабно что-то поменять (переверстать «шапку»), но по ходу работ возникает необходимость подправить критичный баг (неправильно указан контакт в «подвале»)._

:shipit:

:shipit::shipit::shipit::shipit:

#git checkout -b new_page_header # создадим новую ветку для задачи изменения «шапки» и перейдём в неё
***subl inc/header.html # редактируем и сохраняем разметку «шапки»***

git commit -a -m "Новая шапка: смена логотипа" # делаем первый коммит (работа еще не завершена)
# тут выясняется, что есть баг с контактом в «подвале»
**_git checkout master # возвращаемся к ветке master_**

git checkout -b footer_hotfix # создаём ветку (основанную на master) для решения проблемы
subl inc/footer.html # устраняем баг и сохраняем разметку «подвала»

**_git commit -a -m "Исправление контакта в подвале" # делаем коммит_**

git checkout master # переключаемся в ветку master

![Screenshot of a comment on a GitHub issue showing an image, added in the Markdown, of an Octocat smiling and raising a tentacle.](https://i.getgems.io/sRFb1Mhy9voLE_ddT6On9PzWU6FtLAjbVkXGVYwdSJA/rs:fill:1000:0:1/g:ce/czM6Ly9nZXRnZW1zLW5mdC9uZnQvYy82NjIwMWRmYTgwMTM0NDE2Mjc5OTMwMWIvMTIzL2ltYWdlLnBuZw)

**_git merge footer_hotfix # вливаем в master изменения из ветки footer_hotfix_**

[Клик](https://pages.github.com/)



git branch -d footer_hotfix # удаляем ветку footer_hotfix

> [!NOTE]
> Бегемоты тоже люди

> [!TIP]
> Люблю того кто это читает :shipit:

> [!IMPORTANT]
> я хомяк :shipit:

> [!WARNING]
> опасно это читать

> [!CAUTION]
> мяу

**_git checkout new_page_header # переключаемся в ветку new_page_header для продолжения работ над «шапкой»_**

subl inc/header.html # редактируем и сохраняем разметку «шапки»

**_git commit -a -m "Новая шапка: смена навигации" # делаем коммит (работа над «шапкой» завершена)_**

git checkout master # переключаемся в ветку master

**_git merge new_page_header # вливаем в master изменения из ветки new_page_header_*

**_Сведения о проверках состояния
Проверки состояния позволяют узнать, удовлетворяют ли ваши фиксации условиям, заданным для репозитория, в котором вы работаете._**



