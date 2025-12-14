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

