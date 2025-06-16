# 🎯 HCM Select Component

Modern, özelleştirilebilir ve erişilebilir select komponenti. Baklava Design System'den referans alınarak geliştirilmiştir.

## ✨ Özellikler

- 🎨 **Modern Tasarım**: Temiz ve profesyonel görünüm
- 🔧 **Özelleştirilebilir**: Boyut, renk ve stil seçenekleri
- 🌐 **Erişilebilir**: ARIA standartlarına uygun
- 📱 **Responsive**: Tüm cihazlarda mükemmel görünüm
- 🔍 **Arama Desteği**: Seçenekler arasında hızlı arama
- ✅ **Validasyon**: Hata, uyarı ve başarı durumları
- 🎭 **Icon Desteği**: Emoji ve Font Awesome iconları
- 📦 **Çoklu Seçim**: Checkbox ve radio button stilleri
- 🚀 **Performanslı**: Shadow DOM ve portal rendering

## 🚀 Hızlı Başlangıç

### HTML
```html
<!DOCTYPE html>
<html>
<head>
  <link rel="stylesheet" href="https://use.fontawesome.com/releases/v6.4.0/css/all.css">
</head>
<body>
  <hcm-select label="Ülke Seçin" placeholder="Bir ülke seçin">
    <hcm-select-option value="tr">Türkiye</hcm-select-option>
    <hcm-select-option value="us">Amerika Birleşik Devletleri</hcm-select-option>
    <hcm-select-option value="de">Almanya</hcm-select-option>
  </hcm-select>

  <script src="hcm-select.js"></script>
</body>
</html>
```

### JavaScript ile Seçenekler
```javascript
const select = document.querySelector('hcm-select');
select.options = [
  { value: 'tr', label: 'Türkiye' },
  { value: 'us', label: 'Amerika Birleşik Devletleri' },
  { value: 'de', label: 'Almanya' }
];
```

## 📖 Kullanım Örnekleri

### Temel Kullanım
```html
<hcm-select 
  label="Şehir" 
  placeholder="Şehir seçin"
  clearable>
  <hcm-select-option value="istanbul">İstanbul</hcm-select-option>
  <hcm-select-option value="ankara">Ankara</hcm-select-option>
  <hcm-select-option value="izmir">İzmir</hcm-select-option>
</hcm-select>
```

### Icon ile Kullanım
```html
<!-- Emoji Icon -->
<hcm-select 
  label="Kategori" 
  placeholder="Kategori seçin"
  icon="📁"
  icon-position="left">
  <hcm-select-option value="tech">Teknoloji</hcm-select-option>
  <hcm-select-option value="design">Tasarım</hcm-select-option>
</hcm-select>

<!-- Font Awesome Icon -->
<hcm-select 
  label="Kullanıcı" 
  placeholder="Kullanıcı seçin"
  icon-class="fas fa-user"
  icon-position="left">
  <hcm-select-option value="admin">Admin</hcm-select-option>
  <hcm-select-option value="user">Kullanıcı</hcm-select-option>
</hcm-select>
```

### Arama Özelliği
```html
<hcm-select 
  label="Programlama Dili" 
  placeholder="Dil seçin"
  search-bar
  search-bar-placeholder="Dil ara..."
  search-not-found-text="Sonuç bulunamadı">
  <hcm-select-option value="js">JavaScript</hcm-select-option>
  <hcm-select-option value="py">Python</hcm-select-option>
  <hcm-select-option value="java">Java</hcm-select-option>
</hcm-select>
```

### Çoklu Seçim
```html
<hcm-select 
  label="Hobiler" 
  placeholder="Hobiler seçin"
  multiple
  option-style="checkbox">
  <hcm-select-option value="reading">Okuma</hcm-select-option>
  <hcm-select-option value="music">Müzik</hcm-select-option>
  <hcm-select-option value="sports">Spor</hcm-select-option>
</hcm-select>
```

### Validasyon Durumları
```html
<!-- Hata Durumu -->
<hcm-select 
  label="Gerekli Alan" 
  placeholder="Seçim yapın"
  validation-state="invalid"
  invalid-text="Bu alan zorunludur!"
  required>
  <hcm-select-option value="1">Seçenek 1</hcm-select-option>
</hcm-select>

<!-- Başarı Durumu -->
<hcm-select 
  label="Onaylandı" 
  placeholder="Seçim yapın"
  validation-state="success"
  success-text="Seçim onaylandı!">
  <hcm-select-option value="1">Seçenek 1</hcm-select-option>
</hcm-select>
```

## 🔧 Attribute Referansı

| Attribute | Tip | Varsayılan | Açıklama |
|-----------|-----|------------|----------|
| `name` | string | - | Form alanının adı |
| `value` | string | null | Seçili değer |
| `label` | string | - | Üst etiket metni |
| `placeholder` | string | "Select an option" | Placeholder metni |
| `size` | small \| medium \| large | medium | Bileşen boyutu |
| `required` | boolean | false | Zorunlu alan |
| `disabled` | boolean | false | Devre dışı durumu |
| `clearable` | boolean | false | Temizle butonu |
| `multiple` | boolean | false | Çoklu seçim modu |
| `search-bar` | boolean | false | Arama çubuğu |
| `search-bar-placeholder` | string | "Search..." | Arama placeholder'ı |
| `search-not-found-text` | string | "No results found" | Sonuç bulunamadı metni |
| `option-borders` | boolean | false | Seçenekler arası çizgi |
| `option-style` | default \| checkbox \| radio | default | Seçenek görünüm stili |
| `validation-state` | default \| invalid \| warning \| success | default | Validation durumu |
| `help-text` | string | - | Yardım metni |
| `invalid-text` | string | - | Hata mesajı |
| `warning-text` | string | - | Uyarı mesajı |
| `success-text` | string | - | Başarı mesajı |
| `icon` | string | - | Emoji veya text icon |
| `icon-class` | string | - | CSS class ile icon |
| `icon-position` | left \| right | left | Icon konumu |

## 🎮 JavaScript API

### Metodlar
```javascript
const select = document.querySelector('hcm-select');

// Dropdown'ı aç/kapat
select.open();
select.close();

// Seçimi temizle
select.clear();

// Elemente odaklan
select.focus();

// Değer al/ayarla
console.log(select.value);
select.value = 'new-value';

// Seçenekleri ayarla
select.options = [
  { value: '1', label: 'Seçenek 1' },
  { value: '2', label: 'Seçenek 2' }
];
```

### Event Dinleme
```javascript
select.addEventListener('hcm-select', (e) => {
  console.log('Seçilen değer:', e.detail.value);
  console.log('Seçilen label:', e.detail.label);
});
```

## 🎨 Özelleştirme

### CSS Custom Properties
```css
hcm-select {
  --hcm-select-border-color: #d1d5db;
  --hcm-select-focus-color: #3b82f6;
  --hcm-select-error-color: #ef4444;
  --hcm-select-success-color: #10b981;
  --hcm-select-warning-color: #f59e0b;
}
```

### Boyut Seçenekleri
- `size="small"`: 36px yükseklik, 14px font
- `size="medium"`: 44px yükseklik, 16px font (varsayılan)
- `size="large"`: 52px yükseklik, 18px font

## 🌐 Tarayıcı Desteği

- ✅ Chrome 54+
- ✅ Firefox 63+
- ✅ Safari 10.1+
- ✅ Edge 79+

## 📦 Kurulum

### CDN
```html
<script src="https://unpkg.com/hcm-select@latest/hcm-select.js"></script>
```

### NPM
```bash
npm install hcm-select
```

### Manuel
1. `hcm-select.js` dosyasını indirin
2. HTML sayfanızda script tag ile ekleyin
3. Font Awesome için CSS linkini ekleyin (isteğe bağlı)

## 🤝 Katkıda Bulunma

1. Fork yapın
2. Feature branch oluşturun (`git checkout -b feature/amazing-feature`)
3. Değişikliklerinizi commit edin (`git commit -m 'Add amazing feature'`)
4. Branch'inizi push edin (`git push origin feature/amazing-feature`)
5. Pull Request oluşturun

## 📄 Lisans

MIT License - detaylar için [LICENSE](LICENSE) dosyasına bakın.

## 🙏 Teşekkürler

- [Baklava Design System](https://github.com/Trendyol/baklava) - Tasarım referansı
- [Font Awesome](https://fontawesome.com/) - Icon desteği
- Web Components standartları

## 📞 İletişim

Sorularınız için issue açabilir veya pull request gönderebilirsiniz.

---

⭐ Bu projeyi beğendiyseniz yıldız vermeyi unutmayın! 