# 📘 07 - Taşıma Katmanı (Transport Layer)

## 🎯 Amaç  
Bu bölümde, Taşıma Katmanı’nın görevlerini, TCP ve UDP arasındaki farkları, bağlantı yönetimini ve port numaralarının kullanımını öğreneceğiz.  
Amaç, uygulamalar arasında güvenilir veya hızlı veri iletiminin nasıl sağlandığını anlamaktır.

---

# 🔹 Taşıma Katmanının Görevleri

Taşıma katmanı, uçtan uca iletişimi sağlayan ve verinin güvenilir şekilde iletilmesini yöneten katmandır.

### Başlıca görevleri:
- **Uçtan uca bağlantı yönetimi**
- **Segmentlere ayırma (Segmentation)**
- **Akış kontrolü (Flow Control)**
- **Hata kontrolü**
- **Port numaraları ile süreçlerin ayrılması**
- **Bağlantı kurulumu / sonlandırma (TCP)**

Taşıma Katmanında çalışan en popüler iki protokol:
- **TCP (Transmission Control Protocol)**
- **UDP (User Datagram Protocol)**

---

# 🔸 Port Numaraları

Port numaraları, aynı cihazdaki farklı uygulamaların iletişim kanallarını ayırt etmek için kullanılır.

| Port Aralığı | Tür | Açıklama |
|--------------|------|-----------|
| **0–1023** | Well-Known Ports | HTTP (80), HTTPS (443), DNS (53) |
| **1024–49151** | Registered Ports | Uygulama servisleri |
| **49152–65535** | Dynamic/Private Ports | Rastgele atanan portlar |

Örnek:
- Bir web tarayıcısı → 443 portuna bağlanır (HTTPS)
- Bir DNS sorgusu → 53 portuna gider

---

# 🌐 TCP (Transmission Control Protocol)

TCP, **güvenilir**, **bağlantı tabanlı** bir protokoldür.

## 🔹 TCP’nin Özellikleri:
- Bağlantı kurulumu **zorunludur** (3-Way Handshake)
- Paketler **sıralı** gelir  
- Kaybolan paketler **yeniden gönderilir**
- Akış kontrolü vardır (Flow Control)
- Tıkanıklık kontrolü vardır (Congestion Control)

---

## 🔸 TCP 3-Way Handshake (Bağlantı Kurulumu)

TCP bağlantısı 3 adımda kurulur:

1) **SYN →** Client, bağlantı isteği gönderir  
2) **SYN + ACK →** Server isteği onaylar  
3) **ACK →** Client doğrular ve bağlantı kurulur

Client ---- SYN -----> Server
Client <--- SYN/ACK --- Server
Client ---- ACK -----> Server
