![VMware Logo](https://github.com/user-attachments/assets/42cc537d-4248-4a41-a8b4-e98992b83f6d)

[![Latest Version](https://img.shields.io/github/release/kriggi/VMware_RUS.svg)](https://github.com/kriggi/VMware_RUS/releases/latest)
[![Total Downloads](https://img.shields.io/github/downloads/kriggi/VMware_RUS/total.svg)](https://github.com/kriggi/VMware_RUS/releases)
[![Latest Release Downloads](https://img.shields.io/github/downloads/kriggi/VMware_RUS/latest/total.svg)](https://github.com/kriggi/VMware_RUS/releases/latest)

## Русификация VMWARE WORKSTATION


### Введение
Начиная с VMware Workstation v12.0 в программе появилась мультиязычная поддержка для основного модуля программы (файл **vmware.exe**) и проигрывателя виртуальных машин (файл **vmplayer.exe**). В оригинальной поставке продукта VMware в наличии есть только два языка: *Японский* и *Китайский*. Языковые файлы – это две библиотеки DLL с локализованными ресурсами, а именно файлы вида **vmappsdk-ХХ.dll** и **vmui-ХХ.dll**, где **ХХ** – это короткое имя языка, и файл сообщений **vmware.vmsg**.

Для переключения языка интерфейса файлы программы vmware.exe и vmplayer.exe необходимо запускать с параметром **--locale=ХХ**, где **ХХ** – это короткое имя соответствующего языка. Например, *Japan* = **ja**, *Russian* = **ru**, *Deutsch* = **de** и т.д. Таким образом командная строка запуска приложения с интерфейсом на Русском языке будет выглядеть следующим образом:
```
  C:\Program Files (x86)\VMware\VMware Workstation\vmware.exe --locale=ru
  C:\Program Files (x86)\VMware\VMware Workstation\vmplayer.exe --locale=ru
```


### Установка
Языковой пакет поставляется в обычных архивах под соответствующий диапазон версий VMware Workstation. Содержимое архива следует распаковать в корневой каталог с установленной программой, обычно по пути "*C:\Program Files (x86)\VMware\VMware Workstation*". Или же вручную создать в папке "**messages**" подпапку с именем "**ru**" и скопировать в неё файлы **vmappsdk-ru.dll**, **vmui-ru.dll** и **vmware.vmsg** из файла архива. Затем, для удобства, создайте ярлыки для запуска приложений с параметром --locale=ru. На этом установка завершена. 

Для тех кто предпочитает автоматическую установку, также опционально предлагается программа установки, которая проверяет установленную версию VmWare Workstation на ПК пользователя и выполняет распаковку соответствующей версии языкового пакета. По желанию пользователя программа установки может записать ярлыки на Рабочий стол и/или меню ПУСК.

### Удаление
Просто удалите папку "**ru**" в каталоге "**messages**", или же удалите полностью весь каталог "**messages**" со всем содержимым. Удалите ярлыки, если они были созданы.


### Особенности
1) Никаких модификаций с оригинальными файлами приложения не производится!
2) Русификатор содержит только три файла: vmappsdk-ru.dll, vmui-ru.dll и vmware.vmsg.
3) Независимо от способа установки языкового пакета вам в любой момент всегда доступна оригинальная версия программы. Без параметра --locale=ru программа запускается с интерфейсом на английском языке.


### Примечания
Мультиязычный интерфейс поддерживается только следующими файлами программы:
 **vmware.exe** – основное приложение по созданию, настройке и запуску ВМ;
 **vmplayer.exe** – проигрыватель виртуальных машин.

Поддержка локализации других модулей приложения, таких как
 **vmnetcfg.exe** – настройка сети;
 **vmware-tray.exe** – значок управления ВМ в трее;
 и т.д. разработчиком не предусмотрено.


### Автор
Создание русификатора: Сергей Нечаев (a.k.a. Wik) © 2004-2025
