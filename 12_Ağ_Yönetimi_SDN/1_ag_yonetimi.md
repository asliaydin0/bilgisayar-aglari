# 🛠️ 12. Bölüm – Ağ Yönetimi & SDN (Software Defined Networking)

## 🎯 Bölüm Amaçları
Bu bölümde;
- Ağ yönetiminin ne olduğunu,
- Geleneksel ağ yönetim yöntemlerini,
- SNMP, NetFlow gibi kavramları,
- SDN (Software Defined Networking) mimarisini  
öğreneceksin.

---
## 1. Ağ Yönetimi Nedir?

**Ağ yönetimi**, ağ altyapısının izlenmesi, yapılandırılması, performansının artırılması ve sorunların tespit edilmesi sürecidir.

Amaç:
- Ağın **sürekli çalışır** durumda olması
- Performans sorunlarını erken tespit etmek
- Güvenliği sağlamak
- Kaynakları verimli kullanmak

---
## 2. Ağ Yönetiminin Temel Fonksiyonları (FCAPS)

Ağ yönetimi genellikle **FCAPS modeli** ile açıklanır:

| Harf | Açılım | Açıklama |
|-----|--------|----------|
| **F** | Fault | Hata tespiti ve çözümü |
| **C** | Configuration | Ağ cihazlarının yapılandırılması |
| **A** | Accounting | Kaynak kullanımının takibi |
| **P** | Performance | Performans izleme |
| **S** | Security | Güvenlik yönetimi |

---

## 3. SNMP (Simple Network Management Protocol)

**SNMP**, ağ cihazlarını izlemek ve yönetmek için kullanılan bir protokoldür.

### SNMP Bileşenleri:
- **Manager:** Yönetimi yapan sistem
- **Agent:** Cihaz üzerinde çalışan yazılım
- **MIB:** Yönetim bilgilerini içeren veritabanı

### SNMP Sürümleri:
- SNMPv1 → Temel, güvensiz  
- SNMPv2c → Gelişmiş, hâlâ sınırlı güvenlik  
- SNMPv3 → **Şifreleme ve kimlik doğrulama içerir**

---
