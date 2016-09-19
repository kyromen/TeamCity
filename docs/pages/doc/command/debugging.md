---
title: Комманды отладки
sidebar: doc_sidebar
permalink: debugging_commands.html
folder: doc/command
---

### dapp list
Вывести список приложений.

```
dapp list [options] [APPS PATTERN ...]
```

### dapp run
Запустить собранное приложение с докерными аргументами **DOCKER ARGS**.

```
dapp run [options] [APPS PATTERN...] [DOCKER ARGS]
```

#### [DOCKER ARGS]
Может содержать докерные опции и/или команду.

Перед командой необходимо использовать группу символов ' -- '.

#### Примеры

##### Запустить приложение с опциями
```bash
$ dapp run -ti --rm
```

##### Запустить с опциями и командами
```bash
$ dapp run -ti --rm -- bash -ec true
```

##### Запустить, передав только команды
```bash
$ dapp run -- bash -ec true
```

##### Посмотреть, что может быть запущено
```bash
$ dapp run app -ti --rm -- bash -ec true --dry-run
docker run -ti --rm app-dappstage:ea5ec7543c809ec7e9fe28181edfcb2ee6f48efaa680f67bf23a0fc0057ea54c bash -ec true
```

{% include links.html %}
