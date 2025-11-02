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
