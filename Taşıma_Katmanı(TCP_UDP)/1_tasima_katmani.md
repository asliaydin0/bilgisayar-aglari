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


---

## 🔸 TCP Bağlantı Sonlandırma (4 Adım)

1) FIN  
2) ACK  
3) FIN  
4) ACK

Toplamda 4 paketle bağlantı kapatılır.

---

## 📦 TCP Segment Yapısı (Kısaca)

- Source Port  
- Destination Port  
- Sequence Number  
- Acknowledgment Number  
- Flags (SYN, ACK, FIN, RST…)  
- Window Size  

TCP, veriyi **segment** adı verilen parçalara böler.

---

# 🚀 UDP (User Datagram Protocol)

UDP, **bağlantısız** ve **hızlı** bir iletim protokolüdür.

## 🔹 UDP’nin Özellikleri:
- Bağlantı kurmaz  
- Paketlerin alınıp alınmadığını kontrol etmez  
- Sıralama yoktur  
- Hata kontrolü yok denecek kadar az  
- Çok hızlıdır  
- Canlı yayın veya gerçek zamanlı uygulamalar için idealdir

---

# 🔄 TCP vs UDP Karşılaştırma

| Özellik | TCP | UDP |
|---------|------|------|
| Bağlantı | Bağlantılı | Bağlantısız |
| Güvenilirlik | Yüksek | Düşük |
| Sıralama | Var | Yok |
| Yeniden gönderme | Var | Yok |
| Hız | Orta / Yavaş | Çok hızlı |
| Kullanım alanı | Web, FTP, Mail | Oyun, VoIP, Video stream |

---

# 🎮 Hangi Uygulama Hangisini Kullanır?

### **TCP kullanan örnekler:**
- Web siteleri (HTTP/HTTPS)
- E-posta (SMTP, IMAP, POP3)
- Dosya aktarımı (FTP)
- SSH

### **UDP kullanan örnekler:**
- Online oyunlar
- Canlı video yayınları
- VoIP (sesli aramalar: WhatsApp, Zoom)
- DNS sorguları

---

# 🔍 Akış Kontrolü (Flow Control)

TCP, alıcı tarafın kapasitesine göre veri gönderimini ayarlar.  
**Sliding Window** mekanizması kullanılır.

Amaç:
- Çok hızlı gönderim yapılmasını engellemek  
- Tampon (buffer) taşmasını önlemek  

---

# 🔥 Tıkanıklık Kontrolü (Congestion Control)

Ağ yoğunlaşırsa TCP yavaşlar, trafik açılınca hızlanır.  
Algoritmalar:
- Slow Start  
- Congestion Avoidance  
- Fast Recovery  

---

# 📘 Özet

- Taşıma Katmanı, uçtan uca güvenilir veri iletiminden sorumludur.  
- TCP güvenilir ve bağlantılı; UDP hızlı ve bağlantısızdır.  
- Port numaraları uygulamaları ayırt etmek için kullanılır.  
- TCP bağlantı kurarken 3-Way Handshake kullanır.  
- UDP düşük gecikme isteyen uygulamalarda kullanılır.


