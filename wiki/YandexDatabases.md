---
title: Глава 2
---

## Как подключиться к MySql? ##

### Установите сертификат: ###

```
mkdir -p ~/.mysql && \
wget "https://storage.yandexcloud.net/cloud-certs/CA.pem" \
   --output-document ~/.mysql/root.crt && \
chmod 0600 ~/.mysql/root.crt
```
### Установите утилиту mysql: ###
```
sudo apt update && sudo apt install --yes mysql-client
```
### Подключитесь к базе данных: ###
```
mysql --host=rc1a-h6pdlh88vbhudii9.mdb.yandexcloud.net \
      --port=3306 \
      --ssl-ca=~/.mysql/root.crt \
      --ssl-mode=VERIFY_IDENTITY \
      --user=user1 \
      --password \
      db1
```

После выполнения команды введите пароль пользователя для завершения процедуры подключения.

Для проверки успешности подключения выполните запрос:


    SELECT version();


## 🛠️ Создание базы данных PostgreSQL
```bash
yc managed-postgresql cluster create \
  --name my-db \
  --network-name default \
  --host zone=ru-central1-a \
  --resources disk-size=10,disk-type=network-ssd
