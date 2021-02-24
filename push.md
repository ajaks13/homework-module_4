## git push — вносим изменения в удаленный репозиторий
---

После проведения работы в экспериментальной ветке, слияния с основной, необходимо обновить удаленный репозиторий (удаленную ветку). Для этого используется команда git push.

*Отправляет свои изменения в удаленную ветку, созданную при клонировании по умолчанию:*
```
git push
```

*Отправляет изменения из ветки master в ветку experimental удаленного репозитория:*
```
git push ssh://yourserver.com/~you/proj.git master:experimental
```

*В удаленном репозитории origin удаляет ветку experimental:*
```
git push origin :experimental
```

*Отправляет в удаленную ветку master репозитория origin (синоним репозитория по умолчанию) ветки локальной ветки master:*
```
git push origin master:master
```

*Отправляет метки в удаленную ветку master репозитория origin:*
```
git push origin master --tags
```

*Изменяет указатель для удаленной ветке master репозитория origin (master будет такой же как и develop):*
```
git push origin origin/develop:master
```

*Добавляет ветку test в удаленный репозиторий origin, указывающую на коммит ветки develop:*
```
git push origin origin/develop:refs/heads/test
```