- создаем юзера на хост машине ```adduser jenkins``` ```sudo adduser jenkins```
- добавляем юзера в группу докера ```usermod -aG docker jenkins```
- перезапускаем докер ```sudo service docker restart```
- в .env файл записываем в параметр HOST_UID записываем id юзера ```id -u jenkins```
- в .env файл записываем в параметр HOST_GID записываем id группы докера ```getent group | grep docker```
- меняем права на папку src 
```
sudo chgrp -R jenkins src
sudo chown -R jenkins src
```