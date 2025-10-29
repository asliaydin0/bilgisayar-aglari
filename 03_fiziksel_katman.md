# 03 | Fiziksel Katman (Physical Layer)

## 🔹 Katmanın Temel Görevi

Fiziksel katman, **verinin elektriksel, optik veya radyo sinyalleri** şeklinde **iletilmesinden sorumludur**.  
Yani bu katman, "bit"lerin bir noktadan diğerine **fiziksel ortam aracılığıyla taşınmasını** sağlar.

> Bu katmanda veri “bit” düzeyindedir (0 ve 1).  
> Üst katmanlardan gelen çerçeveler, fiziksel sinyallere dönüştürülür.

---

## 🔹 Fiziksel Katmanın Görevleri

| Görev | Açıklama |
|:--|:--|
| **Bit İletimi** | Veriyi bit düzeyinde iletir. |
| **Fiziksel Topoloji** | Cihazların fiziksel bağlantı biçimini belirler. |
| **İletim Ortamı Seçimi** | Bakır, fiber veya kablosuz ortamın seçimi. |
| **Sinyal Kodlama** | 0 ve 1’lerin elektriksel/optik sinyallere dönüştürülmesi. |
| **Veri Hızı ve Zamanlama** | Bit hızını ve senkronizasyonu belirler. |

---

## 🔹 Veri İletim Türleri

### 1. **Senkron İletim**
- Veriler belirli zaman aralıklarıyla iletilir.  
- Gönderici ve alıcı **zaman sinyaliyle senkronizedir.**  
- Yüksek hız gerektiren iletişimlerde kullanılır (örnek: Ethernet).

### 2. **Asenkron İletim**
- Her veri karakteri başlama ve durdurma bitiyle gönderilir.  
- Düşük hızlarda ve kısa mesafelerde uygundur (örnek: seri portlar).

### 3. **Seri ve Paralel İletim**
| Tür | Açıklama | Kullanım Alanı |
|:--|:--|:--|
| **Seri** | Bitler art arda iletilir. | USB, Ethernet |
| **Paralel** | Bitler aynı anda birden fazla hat üzerinden iletilir. | Eski yazıcı bağlantıları |

---

## 🔹 Sinyal Türleri

| Tür | Açıklama | Örnek |
|:--|:--|:--|
| **Analog Sinyal** | Sürekli değişen değerler alır. | Radyo, ses |
| **Dijital Sinyal** | Kesikli değerler (0 ve 1) kullanır. | Bilgisayar verisi |

![Analog ve Dijital Sinyal Karşılaştırması](https://upload.wikimedia.org/wikipedia/commons/thumb/8/8d/Analogue_vs_digital_wave.svg/640px-Analogue_vs_digital_wave.svg.png)
> Görsel: Analog (sürekli) ve dijital (kesikli) sinyal farkı.

---

## 🔹 İletim Ortamları

Fiziksel katmanda iletim üç temel ortam üzerinden yapılır:

### 🧵 1. **Bakır Kablolar**
- **UTP (Unshielded Twisted Pair):** Ethernet kablolarında kullanılır.  
- **STP (Shielded Twisted Pair):** Parazitli ortamlarda tercih edilir.  
- **Koaksiyel Kablo:** TV sistemleri ve eski ağlarda kullanılır.

### 🔥 2. **Fiber Optik Kablolar**
- Işık sinyalleriyle veri taşır.  
- **Yüksek hız ve uzun mesafe** avantajına sahiptir.  
- Elektromanyetik gürültüden etkilenmez.

### 📡 3. **Kablosuz Ortamlar**
- Radyo, mikrodalga, kızılötesi gibi dalgalarla veri iletir.  
- **Wi-Fi, Bluetooth, 5G** gibi teknolojiler bu kategoridedir.

---

## 🔹 Bant Genişliği, Hız ve Gecikme

| Kavram | Açıklama |
|:--|:--|
| **Bant Genişliği** | Kanalın taşıyabileceği maksimum veri miktarıdır. (bps, Mbps, Gbps) |
| **Gecikme (Latency)** | Verinin bir noktadan diğerine ulaşma süresi. |
| **Veri Hızı (Throughput)** | Gerçekte iletilen veri miktarı. |

> 📘 Gerçek hız = Bant genişliği - Kayıplar (gecikme, hata, protokol yükü)

---

## 🔹 Kodlama Teknikleri

| Teknik | Açıklama | Görsel |
|:--|:--|:--|
| **NRZ (Non-Return to Zero)** | 1 → yüksek, 0 → düşük voltaj. Basit ama senkronizasyon zor. | ![NRZ Kodlama](https://upload.wikimedia.org/wikipedia/commons/thumb/5/52/NRZ_encoding.svg/640px-NRZ_encoding.svg.png) |
| **Manchester** | Her bit ortasında seviye değişimi olur (senkron kolay). | ![Manchester Kodlama](https://upload.wikimedia.org/wikipedia/commons/thumb/8/8b/Manchester_encoding_both_conventions.svg/640px-Manchester_encoding_both_conventions.svg.png) |
| **NRZI** | 1 için geçiş yapılır, 0 için seviye korunur. | ![NRZI Kodlama](https://upload.wikimedia.org/wikipedia/commons/thumb/1/14/NRZI_encoding.svg/640px-NRZI_encoding.svg.png) |

---

## 💡 Örnek: Ethernet Fiziksel Katman

- 10BASE-T, 100BASE-TX, 1000BASE-T gibi standartlar fiziksel katmanda tanımlanır.  
- “BASE” ifadesi **baseband iletim** anlamına gelir.  
- Sayılar veri hızını belirtir:
  - **10BASE-T → 10 Mbps**
  - **100BASE-TX → 100 Mbps**
  - **1000BASE-T → 1 Gbps**

---


