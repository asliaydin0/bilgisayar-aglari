# 🌐 02 - OSI ve TCP/IP Katmanları

## 🎯 Amaç
Bu bölümün amacı, veri iletişiminin katmanlı yapı mantığıyla nasıl gerçekleştiğini anlamak, OSI ve TCP/IP modellerini karşılaştırmalı olarak öğrenmektir.

---

## 🧱 Katmanlı Mimari Nedir?

Ağ iletişimi karmaşık bir süreçtir. Bu karmaşıklığı yönetebilmek için **katmanlı model** kullanılır.  
Her katman belirli bir görevi yerine getirir ve yalnızca alt ve üst katmanla iletişim kurar.

> 🧠 Katmanlı yapı, “**böl ve yönet**” mantığıyla ağ iletişimini basitleştirir.

---

## 🧩 OSI (Open Systems Interconnection) Modeli

OSI modeli, ISO tarafından geliştirilen ve **7 katmandan oluşan teorik bir referans modelidir.**  
Her katman belirli bir işlevi üstlenir.

![OSI Katman Modeli Diyagramı](https://commons.wikimedia.org/wiki/File%3AOSI_Model_v1.svg?utm_source)
> Görsel: OSI modelinin 7 katmanlı yapısını göstermektedir.

### 🔸 1. Fiziksel Katman (Physical Layer)
- **Görev:** Bitlerin fiziksel ortamda iletimi.  
- **Kapsam:** Kablolar, voltaj, hız, konektörler.  
- **Cihazlar:** Hub, tekrarlayıcı (repeater).  
- **Veri birimi:** Bit.

### 🔸 2. Veri Bağlantı Katmanı (Data Link Layer)
- **Görev:** Aynı ağ içindeki cihazlar arası çerçeve (frame) iletişimi.  
- **Hata tespiti ve akış kontrolü** sağlar.  
- **Alt katmanları:**  
  - **MAC (Media Access Control)**  
  - **LLC (Logical Link Control)**  
- **Cihazlar:** Switch, köprü (bridge).  
- **Veri birimi:** Frame.

### 🔸 3. Ağ Katmanı (Network Layer)
- **Görev:** Farklı ağlar arasında veri paketlerinin yönlendirilmesi.  
- **Protokoller:** IP, ICMP.  
- **Cihazlar:** Router.  
- **Veri birimi:** Paket (Packet).

### 🔸 4. Taşıma Katmanı (Transport Layer)
- **Görev:** Uçtan uca iletişim ve veri güvenliği.  
- **Protokoller:** TCP, UDP.  
- **İşlevler:**  
  - Hata kontrolü  
  - Paket sıralama  
  - Bağlantı kurulumu (TCP handshake)  
- **Veri birimi:** Segment.

### 🔸 5. Oturum Katmanı (Session Layer)
- **Görev:** İki cihaz arasındaki oturumların kurulması, yönetimi ve sonlandırılması.  
- **Örnek:** Sunucu ve istemci arasındaki bağlantı oturumları.  

### 🔸 6. Sunum Katmanı (Presentation Layer)
- **Görev:** Veriyi uygun formata çevirir, şifreleme ve sıkıştırma işlemleri yapar.  
- **Örnek:** JPEG, MP3, SSL, TLS.  

### 🔸 7. Uygulama Katmanı (Application Layer)
- **Görev:** Kullanıcının doğrudan etkileşimde bulunduğu katmandır.  
- **Protokoller:** HTTP, FTP, SMTP, DNS.  

---

## 🔁 TCP/IP Modeli

TCP/IP modeli, OSI modelinin pratikte kullanılan halidir.  
Gerçek ağlarda veri iletişimi genellikle bu model üzerinden gerçekleşir.  
Toplam **4 katmandan** oluşur.

![TCP/IP Katman Modeli Diyagramı](https://upload.wikimedia.org/wikipedia/commons/e/e5/TCP-IP_Model_-_en.png)
> Görsel: TCP/IP modelinin 4 katmanlı yapısını göstermektedir.

| TCP/IP Katmanı | OSI Katmanına Karşılığı | Örnek Protokoller |
|----------------|--------------------------|-------------------|
| **Uygulama Katmanı** | 5, 6, 7 | HTTP, FTP, SMTP, DNS |
| **Taşıma Katmanı** | 4 | TCP, UDP |
| **İnternet Katmanı** | 3 | IP, ICMP, ARP |
| **Ağ Erişim Katmanı** | 1, 2 | Ethernet, Wi-Fi |

---

## ⚖️ OSI vs TCP/IP Karşılaştırması

| Özellik | OSI Modeli | TCP/IP Modeli |
|----------|-------------|----------------|
| **Katman Sayısı** | 7 | 4 |
| **Kapsam** | Teorik model | Gerçek uygulama modeli |
| **Geliştiren** | ISO | ABD Savunma Bakanlığı (DARPA) |
| **Protokoller** | Soyut (örnek: teorik HTTP) | Gerçek protokoller (örnek: HTTP, IP, TCP) |
| **Kullanım Alanı** | Öğretici ve açıklayıcı | Günlük ağ uygulamaları |

> 📘 **Özet:**  
> OSI modeli kavramsal bir çerçeve sunar.  
> TCP/IP modeli ise internetin temelini oluşturan gerçek sistemdir.

---

## 🧭 Veri İletim Süreci (Encapsulation)

Veri, gönderici tarafta **üstten alta** doğru her katmanda bir başlık eklenerek iletilir.  
Alıcı tarafta ise bu başlıklar **alttan üste** doğru çözülür.

![Encapsulation Diyagramı](https://commons.wikimedia.org/wiki/File%3ATCP-IP_OSI_comparison_table.jpg?utm_source)
> Görsel: Veri kapsülleme süreci (encapsulation) — her katman, bir üst katmandan gelen veriye kendi başlığını ekler.

**Süreç:**  
> Uygulama → Taşıma → İnternet → Ağ Erişim → (Fiziksel İletim)  

**Veri birimleri:**  
- Application → Data  
- Transport → Segment  
- Internet → Packet  
- Network Access → Frame → Bit

---

## 🧠 Mini Alıştırmalar

1. OSI modelinde yönlendirme hangi katmanda yapılır?  
2. TCP/IP modelinde IP protokolü hangi katmanda bulunur?  
3. Aşağıdaki cihazlardan hangisi **veri bağlantı katmanında** çalışır?  
   - a) Router  
   - b) Switch  
   - c) Modem  
4. “Encapsulation” kavramı neyi ifade eder?

---

## 📘 Özet

- OSI modeli 7, TCP/IP modeli 4 katmandan oluşur.  
- OSI modeli teorik, TCP/IP modeli pratik bir yapıdır.  
- Veri katmanlar arasında başlıklar eklenerek iletilir (Encapsulation).  
- Her katman belirli bir göreve sahiptir ve alt/üst katmanla iletişim kurar.
