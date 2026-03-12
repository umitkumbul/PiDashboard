# Proje Kuralları (Gemini Agent Talimatları)

Bu projede yapılan her değişiklikte aşağıdaki adımların izlenmesi ZORUNLUDUR:

## 1. PWA Versiyon Güncelleme
Uygulama bir PWA (Progressive Web App) olarak çalışmaktadır. Yapılan değişikliklerin kullanıcının cihazında (özellikle iOS ana ekran eklemelerinde) anında görünmesi için:
- Her commit öncesinde `sw.js` dosyası içindeki `CACHE_NAME` değişkenindeki sürüm numarasını (v1, v2, v3...) bir artır.
- `index.html` içindeki Service Worker kayıt mantığını bozma.

## 2. Deployment & Infrastructure
- Proje GitHub Actions ile **Raspberry Pi** (`raspberrypi`) üzerine otomatik deploy edilmektedir.
- Cihaz Tailscale ağı üzerindedir, kullanıcı adı: `umitkumbul`. Gerekirse SSH ile müdahale edilebilir.
- `.github/workflows/deploy.yml` dosyasını bozma.
- Push işlemini her zaman `master` branch'ine yap.

## 3. Mimari
- Bu basit bir HTML/JS Dashboard projesidir, gereksiz karmaşıklıktan kaçın.
