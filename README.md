""\
# Docker Redis Project

## 📌 Docker Komutları

### 🔹 Docker Görüntüleri (Images) ile İlgili Komutlar
- `docker images`: Mevcut Docker görüntülerini listeler.
- `docker pull redis`: Redis imajını Docker Hub'dan indirir.
- `docker rmi <image_id>`: Belirtilen Docker görüntüsünü siler.
- `docker inspect <image_id>`: Docker görüntüsü hakkında detaylı bilgi verir.

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
- `docker inspect <container_id>`: Çalışan bir konteyner hakkında detaylı bilgi verir.

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

## 📌 `docker inspect` Nedir?

`docker inspect <container_id>` veya `docker inspect <image_id>` komutları, bir Docker konteyneri veya imajı hakkında detaylı JSON formatında bilgi sağlar.

Örnek Kullanım:
```bash
docker inspect my-redis
```

Geri dönen bilgiler:
- IP Adresi
- Bağlantı Noktaları
- Çalışan Process'ler
- Volume Bilgileri
- Network Ayarları
- Ortam Değişkenleri (Environment Variables)

---

## 📄 Lisans
MIT Lisansı altında sunulmaktadır.
""
