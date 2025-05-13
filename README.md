""\
# Docker Redis Project

## 📌 Docker Komutları

### 🔹 Docker Görüntüleri (Images) ile İlgili Komutlar
- `docker images`: Mevcut Docker görüntülerini listeler.
- `docker pull redis`: Redis imajını Docker Hub'dan indirir.
- `docker rmi <image_id>`: Belirtilen Docker görüntüsünü siler.

### 🔹 Docker Konteynerleri ile İlgili Komutlar
- `docker run --name my-redis -d redis`: Arka planda çalışan bir Redis konteyneri oluşturur.
- `docker ps`: Çalışan tüm konteynerleri listeler.
- `docker ps -a`: Tüm konteynerleri (çalışan/durmayan) listeler.
- `docker stop <container_id>`: Belirtilen konteyneri durdurur.
- `docker start <container_id>`: Durdurulmuş bir konteyneri yeniden başlatır.
- `docker restart <container_id>`: Bir konteyneri yeniden başlatır.
- `docker kill <container_id>`: Konteyneri zorla sonlandırır.
- `docker logs <container_id>`: Konteyner loglarını görüntüler.
- `docker exec -it <container_id> /bin/bash`: Konteyner içine terminal ile girer.
- `docker rm <container_id>`: Belirtilen konteyneri siler.
- `docker rm -f $(docker ps -aq)`: Tüm konteynerleri zorla siler.

### 🔹 Docker Ağ (Network) Komutları
- `docker network ls`: Mevcut ağları listeler.
- `docker network create <network_name>`: Yeni bir ağ oluşturur.
- `docker network connect <network_name> <container_id>`: Bir konteyneri ağa bağlar.
- `docker network disconnect <network_name> <container_id>`: Bir konteyneri ağdan çıkarır.

### 🔹 Docker Hacim (Volume) Komutları
- `docker volume ls`: Mevcut hacimleri listeler.
- `docker volume create <volume_name>`: Yeni bir hacim oluşturur.
- `docker volume rm <volume_name>`: Belirtilen hacmi siler.

---

## 🚀 Redis Docker Uygulaması

### 1️⃣ Redis imajını indirin:
   ```bash
   docker pull redis
   ```

### 2️⃣ Redis konteynerini başlatın:
   ```bash
   docker run --name my-redis -d -p 6379:6379 redis
   ```

### 3️⃣ Redis CLI ile bağlantı kurun:
   ```bash
   docker exec -it my-redis redis-cli
   ```

### 4️⃣ Temel Redis komutları:
   ```redis
   SET foo "bar"
   GET foo
   ```

### 5️⃣ Konteyneri durdurmak için:
   ```bash
   docker stop my-redis
   ```

### 6️⃣ Konteyneri yeniden başlatmak için:
   ```bash
   docker start my-redis
   ```

### 7️⃣ Konteyneri tamamen silmek için:
   ```bash
   docker rm my-redis
   ```

---

## 📄 Lisans
MIT Lisansı altında sunulmaktadır.
""
