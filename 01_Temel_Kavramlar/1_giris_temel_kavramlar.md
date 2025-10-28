# 📘 01 - Giriş & Temel Kavramlar

## 🎯 Amaç
Bu bölümün amacı, bilgisayar ağlarının temel kavramlarını, neden kullanıldıklarını ve temel yapı taşlarını anlamaktır. Ağ sistemlerinin genel mantığını öğrenerek sonraki konulara sağlam bir temel oluşturacağız.

---

## 🔹 Bilgisayar Ağı Nedir?

**Bilgisayar ağı**, birden fazla bilgisayarın ve cihazın bilgi, veri ve kaynak paylaşımı yapmak amacıyla birbirine bağlanmasıdır.  
Amaç, iletişimi kolaylaştırmak, verimliliği artırmak ve kaynak kullanımını ortaklaştırmaktır.

**Örnek:**  
Bir ofisteki bilgisayarların aynı yazıcıyı paylaşabilmesi veya dosya aktarımı yapabilmesi.

---

## 🌐 Ağ Türleri

| Ağ Türü | Açıklama | Örnek |
|----------|-----------|--------|
| **PAN (Personal Area Network)** | Kişisel cihazlar arasında kısa mesafeli ağ. | Bluetooth kulaklık, akıllı saat bağlantısı |
| **LAN (Local Area Network)** | Küçük alanlarda (ofis, bina) kullanılan ağ. | Okul laboratuvarı ağı |
| **MAN (Metropolitan Area Network)** | Bir şehir ölçeğinde ağ bağlantısı. | Şehir belediye ağı |
| **WAN (Wide Area Network)** | Ülke veya dünya çapında geniş alan ağı. | İnternet |

---

## ⚙️ Ağın Temel Bileşenleri

1. **İstemci (Client):** Hizmet alan cihaz (örnek: kullanıcı bilgisayarı).  
2. **Sunucu (Server):** Hizmet sağlayan cihaz (örnek: web sunucusu).  
3. **Ağ Cihazları:**
   - **Modem:** İnternete bağlantıyı sağlar.  
   - **Anahtar (Switch):** Aynı ağ içindeki cihazları birbirine bağlar.  
   - **Yönlendirici (Router):** Ağlar arası veri iletimini sağlar.  
4. **İletim Ortamı:** Kablolu (Ethernet) veya kablosuz (Wi-Fi) bağlantı yolları.  
5. **Protokoller:** Verinin nasıl iletileceğini belirleyen kurallar bütünü (örnek: TCP/IP, HTTP, FTP).

---
## 🔑 Protokol Kavramı

**Protokol**, ağ üzerindeki iki cihazın nasıl iletişim kuracağını tanımlayan standartlardır.  
Bir anlamda, ağ iletişiminin “ortak dili”dir.

**Örnek:**  
- **HTTP:** Web sayfalarının aktarımı  
- **FTP:** Dosya aktarımı  
- **SMTP:** E-posta gönderimi  
- **TCP/IP:** İnternetin temel iletişim protokolü  

---
## 🧩 Katmanlı Ağ Mimarisi

Veri iletişimi, bir dizi **katman** üzerinden gerçekleşir. Her katman belirli bir görevi üstlenir.

### 📊 OSI Modeli (Open Systems Interconnection)
1. **Fiziksel Katman:** Donanım, kablolar, voltajlar.  
2. **Veri Bağlantı Katmanı:** MAC adresleri, çerçeveleme, hata denetimi.  
3. **Ağ Katmanı:** IP adresleme, yönlendirme.  
4. **Taşıma Katmanı:** Uçtan uca veri iletimi (TCP, UDP).  
5. **Oturum Katmanı:** İletişim oturumlarını yönetir.  
6. **Sunum Katmanı:** Veriyi uygun formata dönüştürür (şifreleme, sıkıştırma).  
7. **Uygulama Katmanı:** Kullanıcıya en yakın katman (HTTP, FTP, SMTP).

### 🌐 TCP/IP Modeli
| Katman | Örnek Protokoller |
|--------|------------------|
| **Uygulama Katmanı** | HTTP, FTP, SMTP |
| **Taşıma Katmanı** | TCP, UDP |
| **İnternet Katmanı** | IP, ICMP |
| **Ağ Erişim Katmanı** | Ethernet, Wi-Fi |

> 🧠 **Not:** OSI modeli teoriktir, TCP/IP modeli ise pratikte kullanılır.

---

## 🔍 Ağ Performansını Etkileyen Faktörler

- **Bant genişliği (Bandwidth)**  
- **Gecikme (Latency)**  
- **Paket kaybı (Packet Loss)**  
- **Ağ yoğunluğu (Congestion)**  
- **Kanal kalitesi (Noise, interference)**  

---

## 📘 Özet

- Bilgisayar ağları, bilgi paylaşımı için cihazların birbirine bağlanmasıdır.  
- Ağ türleri: PAN, LAN, MAN, WAN.  
- Temel bileşenler: istemci, sunucu, ağ cihazları, protokoller.  
- Katmanlı yapı, veri iletişimini düzenler (OSI ve TCP/IP modelleri).  
