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

## 🌐 2. IP Adresleri

### **IPv4**
- 32 bit uzunluğundadır.
- Örnek: `192.168.1.10`
- 4 oktetten oluşur (0–255 aralığı).

**Yaygın IPv4 sınıfları:**
| Sınıf | Aralık | Kullanım |
|------|--------|----------|
| A | 0.0.0.0 – 127.255.255.255 | Çok büyük ağlar |
| B | 128.0.0.0 – 191.255.255.255 | Orta büyüklükte ağlar |
| C | 192.0.0.0 – 223.255.255.255 | Küçük ağlar |

---

### **IPv6**
- 128 bit uzunluğundadır.
- Çok daha büyük adres kapasitesi sağlar.
- Örnek: `2001:0db8:85a3:0000:0000:8a2e:0370:7334`

**Avantajları:**
- Daha büyük adres alanı  
- Daha hızlı yönlendirme  
- Otomatik adres yapılandırma (SLAAC)  

---

## 🔄 3. Yönlendirme (Routing)

Ağ Katmanı paketlerin hedefe **hangi yoldan gideceğini belirler**.

### **Statik Routing**
- Yönlendiriciye manuel olarak yol girilir.
- Küçük ağlarda kullanılır.

### **Dinamik Routing**
- Routerlar birbirleriyle bilgi paylaşarak yolları otomatik öğrenir.  
- Protokoller:
  - **RIP**
  - **OSPF**
  - **EIGRP**
  - **BGP**

---

## 📦 4. Ağ Katmanı Protokolleri

| Protokol | Açıklama |
|----------|----------|
| **IP** | Paketlerin adreslenmesi ve yönlendirilmesini sağlar. |
| **ICMP** | Hata raporlama (örneğin ping). |
| **ARP*** | IPv4 için IP ↔ MAC çözümlemesi yapar (*Data Link katmanı ile ortak çalışır*). |
| **NAT** | Özel IP → Genel IP dönüşümü yapar. |

---
