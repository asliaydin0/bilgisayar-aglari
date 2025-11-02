# 04 | Veri Bağlantı Katmanı (Data Link Layer)

## 🔹 Katmanın Temel Görevi

Veri bağlantı katmanı, **fiziksel katman ile ağ katmanı arasındaki iletişimi sağlar.**  
Bu katmanın görevi, fiziksel ortamda taşınan bitleri **hatalardan arındırılmış çerçevelere (frames)** dönüştürmektir.

> 🌐 OSI modelinin 2. katmanıdır ve veri güvenli, düzenli biçimde aktarılmasını sağlar.

---

## 🔹 Veri Birimi: Frame (Çerçeve)

Veri bağlantı katmanında veriler **çerçeve (frame)** adı verilen birimlerle taşınır.  
Çerçeve, adresleme bilgileri (ör. kaynak ve hedef MAC adresleri) ile hata denetimi bilgilerini içerir.

**Bir çerçeve şu bölümlerden oluşur:**

| Bölüm | Açıklama |
|:--|:--|
| **Başlık (Header)** | Kaynak ve hedef MAC adresleri, kontrol bilgileri |
| **Veri (Payload)** | Üst katmandan gelen asıl veri |
| **Son (Trailer)** | Hata kontrol bilgisi (CRC) |

---

## 🔹 Veri Bağlantı Katmanının Alt Katmanları

| Alt Katman | Açıklama |
|:--|:--|
| **LLC (Logical Link Control)** | Üst katmanlarla iletişimi sağlar. Protokol türünü belirtir (ör. IPv4, ARP). |
| **MAC (Media Access Control)** | Donanımsal adresleme (MAC adresi) ve ortam erişim kontrolünü yapar. |

> 💡 MAC adresi, her ağ kartına (NIC) üretici tarafından atanmış **48 bitlik benzersiz bir kimliktir.**

---

## 🔹 Adresleme: MAC Adresi

- MAC (Media Access Control) adresi 48 bit uzunluğundadır ve genellikle 6 çiftlik onaltılık (hexadecimal) biçimde gösterilir.  
  **Örnek:** `00:1A:92:3F:B2:10`

- İlk 24 bit üretici kimliğini, son 24 bit ise cihazın seri numarasını belirtir.

![MAC Adresi Yapısı](https://upload.wikimedia.org/wikipedia/commons/thumb/2/23/MAC_address_structure.svg/640px-MAC_address_structure.svg.png)
> Görsel: MAC adresi yapısı

---

## 🔹 Hata Tespiti ve Düzeltme

Veri bağlantı katmanı, **hatalı iletilen verileri tespit eder** ve gerekirse yeniden gönderilmesini sağlar.  
Bunun için kullanılan başlıca yöntemler:

| Yöntem | Açıklama |
|:--|:--|
| **Parity Bit** | Basit hata tespiti yöntemi, tek veya çift sayıda 1 biti kontrol edilir. |
| **Checksum** | Verinin toplam değeri gönderilir, alıcıda yeniden hesaplanır. |
| **CRC (Cyclic Redundancy Check)** | En güvenilir hata tespit yöntemidir. Ethernet çerçevelerinde kullanılır. |

> 🧩 Hatalı veri tespit edilirse “ARQ (Automatic Repeat Request)” mekanizmasıyla yeniden gönderim yapılır.

---

## 🔹 Erişim Kontrolü (Media Access Control)

Bu katman, aynı iletim ortamını paylaşan cihazların **çakışmadan veri göndermesini** sağlar.  
Kullanılan bazı erişim yöntemleri:

| Yöntem | Açıklama |
|:--|:--|
| **CSMA/CD (Carrier Sense Multiple Access / Collision Detection)** | Ethernet’te kullanılır. Gönderim öncesi ortam dinlenir; çakışma olursa veri yeniden gönderilir. |
| **CSMA/CA (Collision Avoidance)** | Kablosuz ağlarda kullanılır. Çakışma olmadan veri gönderimi amaçlanır. |
| **Token Passing** | Belirli bir “jeton” (token) cihazdan cihaza geçer; sadece jetona sahip cihaz veri gönderir. |

![CSMA/CD ve CSMA/CA](https://upload.wikimedia.org/wikipedia/commons/thumb/8/8a/CSMA-CD_vs_CSMA-CA.svg/640px-CSMA-CD_vs_CSMA-CA.svg.png)
> Görsel: Ethernet ve Wi-Fi ortam erişim yöntemleri farkı

---

## 🔹 Anahtar (Switch) Çalışma Mantığı

Switch, **veri bağlantı katmanında çalışan** bir ağ cihazıdır.  
Gelen çerçevenin **hedef MAC adresine** bakarak veriyi yalnızca o cihaza yönlendirir.

- **Hub**: Veriyi herkese gönderir (katman 1)
- **Switch**: Veriyi hedefe yönlendirir (katman 2)

> 💡 Switch, zamanla bağlı cihazların MAC adreslerini bir “MAC adres tablosu”nda saklar.

---

## 🔹 Protokoller ve Standartlar

| Protokol / Standart | Açıklama |
|:--|:--|
| **Ethernet (IEEE 802.3)** | En yaygın kablolu ağ standardı. |
| **Wi-Fi (IEEE 802.11)** | Kablosuz ağ standardı. |
| **PPP (Point-to-Point Protocol)** | Noktadan noktaya bağlantılarda kullanılır. |
| **HDLC** | Senkron veri bağlantısı için kullanılır (genellikle WAN bağlantılarında). |
| **ARP (Address Resolution Protocol)** | IP adresini MAC adresine çevirir. |

---
