# spoofDPI to router
Скрипт установки [spoofDPI](https://github.com/xvzc/SpoofDPI) на роутер, с установленным репозитарием [Entware](https://github.com/Entware/Entware), для обхода блокировки youtube в России

# Установка:
>Проверьте ваше устройство ````uname -m````, должно быть что-то из этого: ````aarch64````, ````mips````, ````mipsel````

Необходимо подключить репозитарй [Entware](https://github.com/Entware/Entware) и установить из него пакеты dtach и curl
````sh
opkg install dtach curl
````
spoofDPI
````sh
curl https://raw.githubusercontent.com/gray1717/spoofDPI_to_router/main/install.sh | bash
````
проверьте настройки, по необходимости измените прослушиваемый адрес и порт
````
/opt/etc/spoofDPI/spoofDPI.conf
````
запустите spoofDPI
````sh
sh /opt/etc/init.d/S8080spoofDPI start
````
Настройте proxy в браузере, укажите порт из конфигурационного файла ````/opt/etc/spoofDPI/spoofDPI.conf```` и адрес роутера

# Сборка пакета *.ipk
````curl https://raw.githubusercontent.com/gray1717/spoofDPI_to_router/main/ipkg-build | bash````
или под определенную архитектуру, из этого: ````aarch64````, ````mips````, ````mipsel````
````curl https://raw.githubusercontent.com/gray1717/spoofDPI_to_router/main/ipkg-build | bash -s aarch64````
установка как обычно
````opkg install spoof-dpi*.ipk````
