# VGBTY
"### Работа с ветками

``` **bash**
~~Есть master (публичная версия сайта), хотим масштабно что-то поменять (переверстать «шапку»), но по ходу работ возникает необходимость подправить критичный баг (неправильно указан контакт в «подвале»).~~

##git checkout -b new_page_header # создадим новую ветку для задачи изменения «шапки» и перейдём в неё##

subl inc/header.html # редактируем и сохраняем разметку «шапки»
git commit -a -m "Новая шапка: смена логотипа" # делаем первый коммит (работа еще не завершена)
# тут выясняется, что есть баг с контактом в «подвале»
git checkout master # возвращаемся к ветке master
git checkout -b footer_hotfix # создаём ветку (основанную на master) для решения проблемы
subl inc/footer.html # устраняем баг и сохраняем разметку «подвала»
git commit -a -m "Исправление контакта в подвале" # делаем коммит
git checkout master # переключаемся в ветку master
git merge footer_hotfix # вливаем в master изменения из ветки footer_hotfix
git branch -d footer_hotfix # удаляем ветку footer_hotfix
git checkout new_page_header # переключаемся в ветку new_page_header для продолжения работ над «шапкой»
subl inc/header.html # редактируем и сохраняем разметку «шапки»
git commit -a -m "Новая шапка: смена навигации" # делаем коммит (работа над «шапкой» завершена)
git checkout master # переключаемся в ветку master
git merge new_page_header # вливаем в master изменения из ветки new_page_header
git branch -d new_page_header # удаляем ветку new_page_header
```
