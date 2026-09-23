# ⚙️ aether-core-api - Teknik Dokümantasyon

## 1. Mimari Mimarisi
- **Programlama Dili:** Python (FastAPI)
- **Katmanlar:** 
  1. *Presentation Layer (UI):* HTML5, TailwindCSS, Fetch API
  2. *API Gateway / Controller:* REST HTTP Uç Noktaları
  3. *Business Logic Layer:* Entity Service CRUD mantığı
  4. *Data Models:* Tip korumalı modeller

## 2. REST API Spesifikasyonu

### `GET /`
- **Açıklama:** Servis sağlık durumu (Health Check) ve web arayüzü sunumu.
- **Dönen Kod:** `200 OK`

### `GET /api/items`
- **Açıklama:** Kayıtlı tüm nesnelerin listesini döner.
- **Örnek cURL:**
  ```bash
  curl -X GET http://localhost:8080/api/items
  ```

### `POST /api/items`
- **Açıklama:** Yeni bir nesne oluşturur.
- **İstek Gövdesi (JSON):**
  ```json
  {
    "title": "Yeni Görev",
    "description": "Detaylı açıklama"
  }
  ```
- **Örnek cURL:**
  ```bash
  curl -X POST http://localhost:8080/api/items \
       -H "Content-Type: application/json" \
       -d '{"title": "Test Nesnesi"}'
  ```

## 3. Docker Dağıtım Talimatı
```bash
docker build -t devhive-aether-core-api .
docker run -d -p 8080:8080 devhive-aether-core-api
```
