# 🔐 11. Bölüm – Ağ Güvenliği (Network Security)

## 🎯 Bölüm Amaçları
Bu bölümde;
- Ağ güvenliğinin neden gerekli olduğunu,
- Temel tehdit türlerini,
- Güvenlik mekanizmalarını,
- Firewall, IDS/IPS, VPN gibi kavramları  
öğreneceksin.

---
## 1. Ağ Güvenliği Nedir?

**Ağ güvenliği**, ağ üzerindeki veri, cihaz ve servislerin yetkisiz erişimlere, saldırılara ve veri kayıplarına karşı korunmasıdır.

### Ağ güvenliğinin temel hedefleri:
- **Gizlilik (Confidentiality)**
- **Bütünlük (Integrity)**
- **Erişilebilirlik (Availability)**

Bu üçlüye **CIA Triad** adı verilir.

---

## 2. Temel Güvenlik Tehditleri

### 🔴 1. Yetkisiz Erişim
- Sisteme izinsiz giriş
- Zayıf parola kullanımı

### 🔴 2. Malware (Kötü Amaçlı Yazılım)
- Virüs
- Worm
- Trojan
- Ransomware

### 🔴 3. DoS / DDoS Saldırıları
- Sistemi aşırı trafikle devre dışı bırakma
- Hizmet kesintisine yol açar

### 🔴 4. Man-in-the-Middle (MitM)
- İki taraf arasındaki iletişimi gizlice dinleme veya değiştirme

---
## 3. Firewall (Güvenlik Duvarı)

**Firewall**, gelen ve giden ağ trafiğini belirlenen kurallara göre kontrol eden güvenlik sistemidir.

### Firewall Türleri:
- **Packet Filtering Firewall**
- **Stateful Firewall**
- **Application Layer Firewall**
- **Next-Generation Firewall (NGFW)**

Firewall genellikle **Ağ Katmanı** ve **Taşıma Katmanı** üzerinde çalışır.

---

## 4. IDS & IPS

### 🔍 IDS (Intrusion Detection System)
- Saldırıları **tespit eder**
- Loglar ve uyarı verir
- Müdahale etmez

### 🛡️ IPS (Intrusion Prevention System)
- Saldırıları **tespit eder ve engeller**
- Trafiği aktif olarak kesebilir

---
## 5. VPN (Virtual Private Network)

VPN, internet üzerinden **şifreli bir tünel** oluşturarak güvenli iletişim sağlar.

### VPN Ne Sağlar?
- Veri gizliliği
- Güvenli uzaktan erişim
- IP gizleme

### Yaygın VPN Protokolleri:
- IPsec
- SSL / TLS
- L2TP
- OpenVPN

---

## 6. Kimlik Doğrulama ve Yetkilendirme

### 🔐 Kimlik Doğrulama (Authentication)
Kullanıcının kim olduğunu doğrular.
- Parola
- SMS / OTP
- Biyometrik veriler

### 🧾 Yetkilendirme (Authorization)
Kullanıcının ne yapabileceğini belirler.

---
## 7. Şifreleme (Encryption)

Verilerin okunamaz hale getirilmesidir.

### Şifreleme Türleri:
- **Simetrik Şifreleme** (AES)
- **Asimetrik Şifreleme** (RSA)

### Nerelerde Kullanılır?
- HTTPS
- VPN
- E-posta güvenliği
- Wi-Fi güvenliği

---

## 8. Ağ Güvenliği Önlemleri

- Güçlü parola politikaları
- Firewall yapılandırması
- Güncel yazılım kullanımı
- IDS/IPS sistemleri
- Segmentasyon (VLAN)
- Loglama ve izleme

---
