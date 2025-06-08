# Object Storage

## 📤 Загрузка файла в хранилище
```bash
yc storage bucket create --name my-bucket
yc storage object upload --bucket-name my-bucket --source myfile.txt
