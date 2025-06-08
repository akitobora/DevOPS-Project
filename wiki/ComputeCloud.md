# Compute Cloud

## 🚀 Создание виртуальной машины
```bash
yc compute instance create \
  --name my-vm \
  --zone ru-central1-a \
  --image-id fd8q2h7gqv1f \
  --platform standard-v3 \
  --cores 2 \
  --memory 4 \
  --disk size=20,type=network-hdd
