# VGBTY
"# Работа с ветками

 **bash**
_Есть master (публичная версия сайта), хотим масштабно что-то поменять (переверстать «шапку»), но по ходу работ возникает необходимость подправить критичный баг (неправильно указан контакт в «подвале»)._

#git checkout -b new_page_header # создадим новую ветку для задачи изменения «шапки» и перейдём в неё
***subl inc/header.html # редактируем и сохраняем разметку «шапки»***

git commit -a -m "Новая шапка: смена логотипа" # делаем первый коммит (работа еще не завершена)
# тут выясняется, что есть баг с контактом в «подвале»
**_git checkout master # возвращаемся к ветке master_**

git checkout -b footer_hotfix # создаём ветку (основанную на master) для решения проблемы
subl inc/footer.html # устраняем баг и сохраняем разметку «подвала»

**_git commit -a -m "Исправление контакта в подвале" # делаем коммит_**

git checkout master # переключаемся в ветку master

**_git merge footer_hotfix # вливаем в master изменения из ветки footer_hotfix_**

git branch -d footer_hotfix # удаляем ветку footer_hotfix

**_git checkout new_page_header # переключаемся в ветку new_page_header для продолжения работ над «шапкой»_**

subl inc/header.html # редактируем и сохраняем разметку «шапки»

**_git commit -a -m "Новая шапка: смена навигации" # делаем коммит (работа над «шапкой» завершена)_**

git checkout master # переключаемся в ветку master
**_git merge new_page_header # вливаем в master изменения из ветки new_page_header_**

git branch -d new_page_header # удаляем ветку new_page_header_**
```
