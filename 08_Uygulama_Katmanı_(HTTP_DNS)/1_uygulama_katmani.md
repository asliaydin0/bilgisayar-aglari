# 📘 08 - Uygulama Katmanı (HTTP, DNS, SMTP, FTP)

## 🎯 Amaç
Bu bölüm, Uygulama Katmanında çalışan temel protokolleri (HTTP, DNS, SMTP, FTP vb.) öğrenmeni amaçlar.  
Kullanıcıya en yakın olan bu katman, uygulamaların ağ ile nasıl iletişim kurduğunu belirler.

---

# 🔹 Uygulama Katmanı Nedir?

Uygulama katmanı, ağ iletişiminin en üst katmanıdır ve **kullanıcı uygulamalarının ağ servislerini kullanmasını sağlar**.

Bu katman:
- Web tarayıcılarının web sunucularına bağlanmasını,
- E-postaların gönderilmesini,
- Dosya aktarımını,
- Alan adlarının çözülmesini sağlar.

Kısacası **internet ile doğrudan etkileşime girdiğimiz katmandır**.

---
# 🌐 Temel Uygulama Katmanı Protokolleri

Aşağıda en yaygın kullanılan uygulama katmanı protokollerini bulabilirsin.

---

# 📌 1. HTTP / HTTPS (Web Protokolleri)

### 🔸 HTTP (HyperText Transfer Protocol)
- Web sayfalarının tarayıcıya iletilmesini sağlar.
- **Stateless** bir protokoldür → Her istek bağımsızdır.
- Varsayılan port: **80**

### 🔸 HTTPS (Secure HTTP)
- HTTP + TLS/SSL şifrelemesi içerir.
- Güvenli iletişim sağlar.
- Varsayılan port: **443**

---

## 🔍 HTTP İstek Yöntemleri (HTTP Methods)

| Yöntem | Açıklama |
|--------|-----------|
| **GET** | Veri talep eder (en yaygın) |
| **POST** | Veri gönderir (form verileri vb.) |
| **PUT** | Bir kaynağı günceller |
| **DELETE** | Bir kaynağı siler |
| **HEAD** | Sadece başlık bilgisi alır |

---

# 📌 2. DNS (Domain Name System)

**DNS**, alan adlarını IP adreslerine çevirir.  
(Bir nevi “internetin telefon rehberi”)

### Örnek:
