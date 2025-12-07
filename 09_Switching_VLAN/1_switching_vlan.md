
# 09. Bölüm – Switching & VLAN

## 🎯 Bölüm Amaçları
Bu bölümde;
- Switch'lerin çalışma mantığını,
- MAC adres tablosunun nasıl oluştuğunu,
- Frame yönlendirme (switching) yöntemlerini,
- VLAN kavramını,
- VLAN türlerini ve trunk bağlantılarını  
detaylı şekilde öğreneceksin.

---

## 1. Switch Nedir?
Switch, OSI modelinin **2. katmanı (Veri Bağlantı Katmanı)** üzerinde çalışan bir ağ cihazıdır ve aynı ağ içinde cihazların birbirine çarpışma olmadan iletişim kurmasını sağlar.

**Temel görevleri:**
- MAC adres tablosu oluşturmak
- Frame'leri hedef MAC adresine göre yönlendirmek
- Broadcast domain yapısını VLAN ile yönetmek

---

## 2. MAC Adres Tablosu (CAM Table)
Switch, gelen her frame üzerinde gönderici MAC adresini inceleyerek **MAC adres tablosuna** ekler.

**MAC Adres Tablosu şu bilgileri içerir:**
| MAC Adresi | Port | Yaşam Süresi |
|------------|------|--------------|
| 00:1A:2B:3C:4D:5E | Fa0/1 | 300 sn |
| 00:B1:8F:44:29:AA | Fa0/3 | 300 sn |

Switch, bu tabloyu kullanarak yalnızca hedef cihazın bulunduğu porta frame gönderir.

### 🎯 Öğrenme Mantığı
- **Kaynak MAC → Tabloya eklenir**
- **Hedef MAC → Tabloya bakılır**
- Yoksa → "Unknown Unicast Flood" (her yere gönderir)

---

## 3. Switching Yöntemleri
Switch’in frame’i işlemeden önce seçebileceği farklı yöntemler vardır:

### **1. Store-and-Forward**
- Frame tamamen alınır → Hata kontrolü (CRC) yapılır → Yönlendirilir.
- **En güvenilir**, ancak en yavaştır.

### **2. Cut-Through**
- Hedef MAC adresi okunur okunmaz frame yönlendirilir.
- Çok hızlı, fakat hatalı frame’ler de geçebilir.

### **3. Fragment-Free**
- Çoğu çarpışma ilk 64 byte’ta oluştuğu için switch ilk 64 byte'ı okur.
- Hız ve güvenilirlik açısından ortada bir seçenektir.

---

## 4. Broadcast, Unicast ve Multicast
### **Unicast**
Tek bir hedef MAC adresine gönderilen frame.

### **Broadcast**
Tüm cihaza gönderilir. Adres:
FF:FF:FF:FF:FF:FF

### **Multicast**
Belirli bir cihaz grubuna gönderilir.

---

## 5. VLAN (Virtual Local Area Network)
VLAN, bir fiziksel switch üzerinde birden fazla **mantıksal ağ** oluşturulmasını sağlar.

Örnek:
- VLAN 10 → Muhasebe  
- VLAN 20 → Personel  
- VLAN 30 → Yönetim  

**Amaç:**  
Güvenlik artırmak, broadcast trafiğini azaltmak, mantıksal grup oluşturmak.

### ✔ VLAN Ne Sağlar?
- Broadcast domain’lerin ayrılması
- Güvenlik
- Esneklik (ofiste düzen değişse bile VLAN yapısı değişmez)

---

## 6. VLAN Türleri

### **1. Port-Based VLAN (En yaygın)**
Her switch portu bir VLAN’a atanır.

### **2. MAC-Based VLAN**
Cihazın MAC adresine göre VLAN atanır.

### **3. Protocol-Based VLAN**
Protokol türüne göre (IP, IPX vb.) VLAN belirlenir.

---
## 7. Access ve Trunk Portlar
Bir VLAN yapısında portların iki ana tipi vardır:

### **Access Port**
- Yalnızca **tek bir VLAN** taşır.
- Bilgisayar, yazıcı gibi son cihazlar bağlanır.  
switchport mode access  
switchport access vlan 10  

### **Trunk Port**
- Birden fazla VLAN taşır.
- Switch–Switch veya Switch–Router bağlantılarında kullanılır.

Trunk protokolleri:
- **IEEE 802.1Q (en yaygın)**
- ISL (Cisco)

802.1Q, frame’e VLAN ID içeren bir **tag** ekler.

---
## 8. VLAN’lar Arası İletişim (Inter-VLAN Routing)
Farklı VLAN'lardaki cihazlar normalde **birbirine erişemez**.  
Erişim sağlanması için:

### ✓ Router-on-a-stick yöntemi  
veya  
### ✓ Layer 3 Switch

kullanılır.

---

## 9. Özet
- Switch, MAC tablosu ile yönlendirme yapar.  
- VLAN, broadcast domain’leri ayırır.  
- Access port → tek VLAN  
- Trunk port → çoklu VLAN  
- Inter-VLAN iletişim için yönlendirme gerekir.

---

