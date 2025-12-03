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
www.google.com → 142.251.40.78

> DNS olmasa sitelere IP adresleriyle bağlanmak zorunda kalırdık.

### DNS Nasıl Çalışır?

1. Kullanıcı alan adını yazar.  
2. Cihaz DNS sunucusuna sorar.  
3. DNS sunucusu ilgili IP adresini döner.  
4. Tarayıcı IP’ye bağlanarak siteyi açar.

### Yaygın DNS Kayıt Türleri

| Kayıt | Açıklama |
|------|----------|
| **A** | Domain → IPv4 |
| **AAAA** | Domain → IPv6 |
| **MX** | E-posta sunucusu |
| **CNAME** | Takma ad |
| **NS** | Yetkili DNS sunucusu |

---

# 📌 3. SMTP, POP3, IMAP (E-posta Protokolleri)

E-posta trafiği üç ana protokolle yönetilir:

### 📤 SMTP (Simple Mail Transfer Protocol)
- E-posta **göndermek** için kullanılır.  
- Varsayılan port: **25** (güvensiz), **587** (TLS)

### 📥 POP3 (Post Office Protocol v3)
- E-postayı **sunucudan indirir**, genelde cihazda saklar.
- Varsayılan port: **110**

### 🌐 IMAP (Internet Message Access Protocol)
- E-postalar sunucuda kalır.
- Cihazlar arasında **senkronizasyon** sağlar.
- Varsayılan port: **143**

---

