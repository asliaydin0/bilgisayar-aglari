# 📘 06 - Yönlendirme & Routerlar (Routing & Routers)

## 🎯 Amaç  
Bu bölümde, ağlar arasında veri iletimini sağlayan **router** cihazlarını, **yönlendirme (routing)** süreçlerini ve yönlendirme protokollerini detaylı şekilde inceleyeceksin.  
Bir IP paketinin kaynaktan hedefe giderken nasıl yol seçtiğini öğreneceğiz.

---

# 🔹 Yönlendirme (Routing) Nedir?

**Yönlendirme**, bir paketin kaynaktan hedefe giderken izlemesi gereken en uygun yolun belirlenmesidir.

Router cihazı gelen IP paketine bakarak karar verir:

- Paket nereye gidiyor? (Hedef IP)
- Hangi ağa ait? (Subnet)
- En uygun rota hangisi?
- Bu paket hangi arayüzden çıkacak?

---

# 🔹 Router (Yönlendirici) Nedir?

**Router**, farklı ağları birbirine bağlayan ve IP yönlendirmesi yapan ağ cihazıdır.

### Router’ın Temel Görevleri:
- IP paketlerini analiz etmek  
- Routing table (yönlendirme tablosu) oluşturmak  
- En uygun rotayı seçmek  
- Ağ maskedeki çakışmaları yönetmek  
- NAT işlemleri gerçekleştirmek (çoğu router)

---

# 🌍 Routing Table (Yönlendirme Tablosu)

Her router, içinde bir **routing table** bulundurur.  
Bu tablo, hangi IP bloğunun hangi arayüz üzerinden yönlendirileceğini belirler.

| Alan | Açıklama |
|------|----------|
| **Destination (Hedef Ağ)** | Nereye gidileceği |
| **Subnet Mask** | Ağın büyüklüğü |
| **Next Hop** | Bir sonraki router |
| **Interface** | Paketin çıkacağı arayüz |
| **Metric** | Yolun maliyet değeri |

**Örnek tablo girişi:**  
Destination: 192.168.10.0  
Mask: 255.255.255.0  
Next Hop: 192.168.1.1  
Interface: eth0  
Metric: 20  

