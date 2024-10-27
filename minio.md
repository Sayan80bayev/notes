```bash
minio server start
```

Вот краткое резюме на русском языке о том, как вы настроили политику доступа для MinIO с использованием клиента mc.
**Резюме:**

1. **Проблема с доступом к** mc:

Сначала вы столкнулись с ошибкой command not found, когда пытались выполнить команду mc policy set download minio_alias/addy, что означало, что клиент MinIO не был установлен.

2. **Установка MinIO Client**:

Вы скачали бинарный файл клиента MinIO с помощью команды:
```bash
curl -O https://dl.min.io/client/mc/release/darwin-amd64/mc
```
Это загрузило файл mc на ваш компьютер.

  

3. **Предоставление прав на выполнение**:

Вы предоставили исполняемые права для скачанного файла:
```bash
chmod +x mc
```

4. **Перемещение в директорию PATH**:

Чтобы сделать mc доступным глобально, вы переместили его в директорию /usr/local/bin/ с помощью команды:
```bash
sudo mv mc /usr/local/bin/
```

5. **Проверка установки**:

После этого вы проверили установку клиента MinIO с помощью команды:
```bash
mc --version
```

Это подтвердило успешную установку клиента.

6. **Настройка доступа**:

Вы настроили алиас для вашего MinIO сервера с помощью команды:

  
```bash
mc alias set minio_alias http://localhost:9000 <access_key> <secret_key>
```


Это позволило вам получить доступ к вашему MinIO серверу.

7. **Настройка политики доступа**:

Вы пытались снова установить политику доступа для addy и получили сообщение о том, что необходимо использовать команду mc anonymous. Затем вы выполнили команду:

  
```bash
mc anonymous set download minio_alias/addy
```
Это успешно установило политику доступа download для бакета addy, позволяя публичный доступ к объектам в этом бакете.

**Заключение:**

Теперь у вас есть установленный клиент MinIO, и вы успешно настроили политику доступа для бакета, позволяя всем пользователям загружать объекты из него. Это позволит вам избежать ошибок AccessDenied при обращении к объектам в вашем бакете addy.

#client #minio #minio-client  #access