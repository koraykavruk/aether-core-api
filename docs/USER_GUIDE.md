# 📖 aether-core-api - Kullanıcı Kılavuzu

Bu belge, **DevHive AI** tarafından otonom olarak inşa edilen **aether-core-api** uygulamasının son kullanıcı ve operasyon ekibi tarafından nasıl kullanılacağını adım adım açıklar.

---

## 1. Uygulama Genel Bakışı
- **Teknoloji Altyapısı:** Python (FastAPI)
- **Erişim Türü:** Modern Web Arayüzü & REST API Servisi
- **Konteyner Desteği:** Docker & Docker Desktop 1-Tık Yayını

## 2. Web Arayüzü Nasıl Kullanılır?
1. Tarayıcınızdan uygulamanın tahsis edilen adresine (`http://localhost:8080`) gidin.
2. Ana sayfada yer alan **"🚀 Canlı Veri Girişi & Test"** alanına başlık veya içerik girin.
3. **"Ekle"** butonuna bastığınızda veriniz anında servis katmanına kaydedilir ve listede görüntülenir.

## 3. Sıkça Sorulan Sorular (SSS)
- **S: Veriler nereye kaydediliyor?**  
  C: Servis katmanı bellek içi (in-memory) veri deposu ve CRUD modelleriyle çalışır.
- **S: Port çakışması olursa ne yapmalıyım?**  
  C: Docker Compose veya `docker run -p <yeni_port>:8080` komutuyla portu kolayca değiştirebilirsiniz.
