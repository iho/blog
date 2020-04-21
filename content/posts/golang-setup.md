---
title: "Golang Setup"
date: 2020-04-21T19:29:25+03:00
---
По дефолту Goland не автоформатує файли при збережені як це роблять інші редактори коду. Принаймі є шорткат щоб це зробити самостійно: `Ctrl+Shift+Alt+f`

Go має гороші тулзи і я постійно забуваю як налаштовувавти Goland тому збережу це тут:
1. потрібно встановити бінарник GolangCI Lint
```bash
curl -sSfL https://raw.githubusercontent.com/golangci/golangci-lint/master/install.sh | sh -s -- -b $(go env GOPATH)/bin v1.24.0
```
2. додати файлвотчери для `goimports` та `golanci-lint`:
![alt text](/img/goland.png "Logo Title Text 1")

Для `golanci-lint` має сенс додати певні опції для більш розширеного виводу:

```run --disable=typecheck $FileDir$ --enable=golint --enable=maligned --enable=prealloc --enable=goconst```