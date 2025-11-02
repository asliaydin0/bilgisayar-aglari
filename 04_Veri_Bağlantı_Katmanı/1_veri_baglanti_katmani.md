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
