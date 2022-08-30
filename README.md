1. Спулить 4 папки (apiserver, cabinet, nginx, reciever)
2. Создать docker-compose файл
3. Выполнить команду `docker save docker-nginx(или docker-apiserver или docker-cabinet или docker-reciever):someone_tag > nazvanie_arhiva.tar` для каждого докерфайла
4. Залить это на удаленный сервер
   1. `ssh nazvanie@ip`
   2. `scp [путь к файлу] [имя пользователя]@[имя сервера/ip-адрес]:[путь к файлу]` через линукс
   3. `pscp [путь к файлу] [имя пользователя]@[имя сервера/ip-адрес]:[путь к файлу]` через windows
5. Установить докер на удаленный сервер
6. Разархивировать архивы
   1. `docker load --input nazvanie_arhiva.tar`
7. Запустить docker-compose
   1. `docker-compose up`
