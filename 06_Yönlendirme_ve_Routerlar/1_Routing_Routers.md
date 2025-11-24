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

| Alan | Açıklama | Örnek tablo girişi|
|------|----------|---------|
| **Destination (Hedef Ağ)** | Nereye gidileceği | 192.168.10.0 |
| **Subnet Mask** | Ağın büyüklüğü | 255.255.255.0 |
| **Next Hop** | Bir sonraki router | 192.168.1.1 |
| **Interface** | Paketin çıkacağı arayüz | eth0 |
| **Metric** | Yolun maliyet değeri | 20 |


---

# 🔸 Yönlendirme Türleri

## **1) Statik Yönlendirme (Static Routing)**

Ağ yöneticisi tarafından elle tanımlanan yönlendirme kurallarıdır.

### ✏️ Özellikleri:
- Manuel olarak eklenir ve silinir  
- Güncellenmez, değişmez  
- Küçük ağlarda kullanılır  
- Güvenli ve basit yapıya sahiptir  

### ✔️ Avantajları:
- Kolay kontrol edilir  
- Tahmin edilebilir  
- Gereksiz trafik oluşturmaz  

### ❌ Dezavantajları:
- Büyük ağlarda yönetimi zordur  
- Ağda arıza olursa rota değişmez  

**Örnek komut (Linux):**
ip route add 192.168.10.0/24 via 192.168.1.1


---

## **2) Dinamik Yönlendirme (Dynamic Routing)**

Router'ların birbirleriyle iletişim kurarak en uygun rotayı otomatik olarak belirlemeleridir.

### ✨ Özellikleri:
- Router’lar sürekli bilgi alışverişi yapar  
- Büyük ve karmaşık ağlarda kullanılır  
- Otomatik güncellenir  
- Yedek yolları kendisi bulur  

### ✔️ Avantajları:
- Ölçeklenebilir  
- Arıza durumunda alternatif yol seçebilir  
- Yönetimi kolaydır  

### ❌ Dezavantajları:
- Ek işlem yükü oluşturur  
- Trafik artar  

---

# 📡 Dinamik Yönlendirme Protokolleri

Dinamik yönlendirme protokolleri iki ana sınıfa ayrılır:

---

## **1) Distance Vector Protokolleri**

Router sadece **komşularından** aldığı bilgiye göre karar verir.  
Her hedefe olan “mesafe” metric üzerinden hesaplanır.

### Örnek Protokoller:
- **RIP (Routing Information Protocol)**  
  - Metric: *Hop sayısı*  
  - Max hop: 15  
  - Küçük ağlarda kullanılır  

### Özellikler:
- Basit  
- Yavaş yakınsama (convergence)  
- Küçük yapılara uygun  

---

## **2) Link-State Protokolleri**

Router ağdaki tüm topolojiyi bilir ve **kendi haritasını çıkarır**.

### Örnek Protokoller:
- **OSPF (Open Shortest Path First)**  
- **IS-IS**

### Özellikler:
- Büyük kurumsal ağlarda kullanılır  
- Daha hızlı  
- Daha detaylı hesaplama yapar  
- SPF (Dijkstra) algoritması kullanılır  

---

# 🔄 NAT (Network Address Translation)

Router’ların sıkça kullandığı bir diğer yapı da **NAT**’tır.

### NAT’ın Görevi:
- Özel IP → Genel IP dönüşümü  
- Yerel ağdaki birçok cihazın **tek bir IP ile internete çıkmasını** sağlar

### Türleri:
- **SNAT** (Source NAT)  
- **DNAT** (Destination NAT)  
- **PAT** (Port Address Translation)

---

# 📘 Özet

- Router cihazları, ağlar arasında paket iletimini sağlar.  
- Routing table, en uygun yolun belirlenmesinde kullanılır.  
- Statik routing manuel; dinamik routing otomatik çalışır.  
- Dinamik protokoller: RIP, OSPF, IS-IS  
- NAT, özel IP’lerin internet erişimini sağlayan çeviri mekanizmasıdır.

