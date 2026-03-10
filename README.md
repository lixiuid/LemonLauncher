# LemonLauncher — GitHub Pages Kurulum Rehberi

## Repo Yapısı

```
lemonlauncher/
├── index.html                        ← Ana sayfa (bu dosya)
└── LemonLauncher-Setup-1.0.0.exe    ← Setup dosyası (indirme için)
```

## Adım Adım Yayınlama

### 1. GitHub Repo Oluştur
- GitHub'da yeni bir repo oluştur (örn: `lemonlauncher`)
- Public olarak ayarla

### 2. Dosyaları Yükle
```bash
git init
git add index.html LemonLauncher-Setup-1.0.0.exe
git commit -m "İlk yayın"
git branch -M main
git remote add origin https://github.com/KULLANICI_ADI/lemonlauncher.git
git push -u origin main
```

### 3. GitHub Pages'i Aç
- Repo → **Settings** → **Pages**
- Source: **Deploy from a branch**
- Branch: **main** → **/root (/)** seç
- **Save**'e tıkla

### 4. Sitenin Açılmasını Bekle
Birkaç dakika içinde şu adreste yayına girer:
```
https://KULLANICI_ADI.github.io/lemonlauncher/
```

---

## Notlar

- `index.html` adı zorunludur — GitHub Pages bu dosyayı otomatik tanır
- `.exe` dosyası 25 MB sınırını geçiyorsa **GitHub Releases** kullanmanı öneririm:
  1. Repo → **Releases** → **Create a new release**
  2. `.exe` dosyasını oraya yükle
  3. `index.html` içindeki indirme linkini Release URL'siyle güncelle:
     ```
     href="https://github.com/KULLANICI_ADI/lemonlauncher/releases/download/v1.0.0/LemonLauncher-Setup-1.0.0.exe"
     ```

## Yapılan Düzeltmeler (orijinal dosyaya göre)

- `main.html` → `index.html` (GitHub Pages zorunluluğu)
- SEO meta etiketleri eklendi (`description`, `og:title`, `og:description`, `theme-color`)
- Mobil/dokunmatik cihazlarda özel cursor gizlendi
- İndirme butonuna `download` attribute'u eklendi
- 85 MB stat sayacı düzeltildi (`data-count="0"` → `data-count="85"`)
