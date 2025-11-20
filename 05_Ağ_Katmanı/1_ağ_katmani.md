# 05 - Ağ Katmanı (Network Layer)

Ağ Katmanı, OSI modelinin 3. katmanıdır ve paketlerin ağlar arasında iletilmesinden sorumlu olan kritik bir katmandır.  
Bu bölümde, IP adresleme, yönlendirme, paket yapıları ve önemli kavramları adım adım öğreneceksin.

---

## 🎯 1. Ağ Katmanının Temel Görevleri

Ağ Katmanı aşağıdaki temel işlevleri yerine getirir:

### **1️⃣ Mantıksal Adresleme (Logical Addressing)**
- Cihazlara **IP adresi atanmasını** sağlar.
- IP adresleri MAC adreslerinden farklı olarak **ağ üzerinde yönlendirme** için kullanılır.

### **2️⃣ Yönlendirme (Routing)**
- Veri paketlerinin **hangi yolu izleyeceğine karar verir.**
- Router (yönlendirici) cihazları bu katmanda çalışır.
- Kaynak → Hedef arasındaki en iyi yolu seçer.

### **3️⃣ Paketleme / Parçalama (Packetization / Fragmentation)**
- Üst katmandan gelen veriyi **paketlere böler**.
- Gerekirse ağın MTU (Maximum Transmission Unit) değerine göre parçalar.

### **4️⃣ Hata Raporlama ve Kontrol (ICMP)**
- ICMP protokolü bu katmanda çalışır (örnek: “ping” komutu).
- Paket iletim hataları hakkında bilgi sağlar.

---
