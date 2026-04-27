# 🎓 Scholarship & Opportunity Tracker

AI destekli, otomatik burs ve fırsat takip sistemi.

## Proje Özeti

Bu sistem Gmail gelen kutusunu her 15 dakikada bir tarayarak 
burs, staj ve fellowship fırsatlarını otomatik olarak tespit eder, 
yapay zeka ile sınıflandırır ve takip edilebilir bir pipeline oluşturur.

## Özellikler

- ✅ Gmail entegrasyonu — otomatik e-posta tarama
- ✅ Google Gemini AI — sınıflandırma ve veri çıkarma
- ✅ Duplicate tespiti — aynı fırsat iki kez kaydedilmez
- ✅ Google Sheets — canlı veritabanı
- ✅ Google Calendar — son tarihler otomatik eklenir
- ✅ Telegram bildirimleri — anlık bildirim
- ✅ Günlük özet e-postası — her sabah 08:00
- ✅ Durum takibi — bookmarked / applying / applied
- ✅ Google Sites dashboard — Türkçe arayüz

## Kullanılan Araçlar

| Araç | Kullanım Amacı |
|---|---|
| n8n | Otomasyon ve iş akışı |
| Google Gemini AI | E-posta sınıflandırma |
| Gmail | E-posta kaynağı |
| Google Sheets | Veritabanı |
| Google Calendar | Son tarih takibi |
| Telegram | Anlık bildirimler |
| Google Sites | Dashboard arayüzü |

## Sistem Mimarisi
Gmail → n8n → Gemini AI → Google Sheets
↓
Google Calendar + Telegram + Digest Email
↓
Google Sites Dashboard
## Workflow Yapısı

### Workflow 1 — E-posta Tarayıcı
Her 15 dakikada otomatik çalışır. Gmail'den e-postaları alır,
Gemini AI ile analiz eder, Sheets'e kaydeder, Calendar'a ekler,
Telegram bildirimi gönderir.

### Workflow 2 — Günlük Özet
Her sabah 08:00'de çalışır. Önceki 24 saatte bulunan
tüm yeni fırsatları HTML e-posta olarak gönderir.

### Workflow 3 — Durum Güncelleyici
Form aracılığıyla tetiklenir. Herhangi bir fırsatın
durumunu günceller ve Telegram onayı gönderir.

## Demo Video
https://drive.google.com/drive/folders/1KuYNGtxmStAjl5HQcPMVi6fwW95rjtsN?usp=drive_link

## Dosya Yapısı
📁 scholarship-opportunity-tracker
├── n8n_workflow_1_email_scanner.json
├── n8n_workflow_2_daily_digest.json
├── n8n_workflow_3_status_updater.json
├── dashboard.html
├── 📁 screenshots
│   ├── workflow1.png
│   ├── workflow2.png
│   ├── workflow3.png
│   ├── google_sheets.png
│   └── telegram_notification.png
└── README.md
## Ekip

Kerziban Sicim, İlayda Yılmaz, Hayrunnisa Yavuz

## Challenge

No Code / Low Code Challenge — AI Destekli İş Akışı ve Otomasyon Sistemi
