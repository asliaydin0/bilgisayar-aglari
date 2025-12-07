
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
