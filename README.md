# Coworking Sektöründe Müşteri Destek Taleplerinin Veri Analizi ile Operasyonel Süreç Verimliliğinin Geliştirilmesi

Bir coworking ağının 2025 yılına ait 19.489 destek talebini betimleyici istatistik ve keşifsel veri analizi yöntemleriyle inceleyen, operasyonel darboğazları ve süreç iyileştirme fırsatlarını ortaya koyan bitirme projesi.

Bu repository, İstanbul Medipol Üniversitesi Yönetim Bilişim Sistemleri Bölümü kapsamında hazırlanan bitirme projesini içermektedir.

## Proje Konusu

49 lokasyondan, 24 ana ve 125 alt kategoriye ayrılmış toplam 19.489 destek talebi; kategori, lokasyon ve lokasyon tipi (Main / Enterprise / Suites) kırılımlarında incelenmiştir. İncelenen başlıca kategoriler:

- Bakım ve Onarım
- Üyelik İşlemleri
- Kurulum ve Teknik Destek
- Temizlik
- Acil Durumlar

## Projenin Amacı

ITSM destek taleplerini veri analitiği yöntemleriyle inceleyerek tekrar eden problemleri, hizmet performansını (SLA uyumu, çözüm süresi) ve süreç iyileştirme fırsatlarını belirlemek; bulguları operasyonel ve stratejik önerilere dönüştürmek.

## Metodoloji

- **Veri seti:** 2025 yılına ait, talep yönetim sisteminden çekilen 19.489 destek talebi (49 lokasyon, 24 ana / 125 alt kategori). Kişisel ve kurumsal veriler anonimleştirilmiştir (lokasyonlar L01–L49 olarak kodlanmıştır).
- **Veri hazırlama:** Kategori alanındaki 808 boş kaydın kural tabanlı geri kazanımı; sınıflandırılamayan 81 talebin analiz dışı bırakılması.
- **Analiz yöntemi:** Betimleyici istatistik + keşifsel veri analizi. Medyan çözüm süresi, FRT (ilk yanıt süresi) ve EST (tahmini çözüm süresi) uyum oranları; kapasiteye göre normalize edilmiş TicketPerOccupiedSeat / TicketPerAccount metrikleri; lokasyon karşılaştırması için z-skor tabanlı kompozit problem endeksi; Pareto analizi.
- **Araçlar:** Veri işleme, modelleme ve istatistiksel analiz Python ile; görselleştirme ve dashboard Microsoft Power BI ile yapılmıştır.

## Bulgular

- Taleplerin **%85'i** sadece dört kategoride toplanmaktadır: Bakım-Onarım (5.557), Üyelik İşlemleri (4.416), Kurulum ve Teknik Destek (3.554), Temizlik (3.218).
- Genel SLA uyum oranları (FRT %62,25 / EST %57,59) literatürdeki %90 hedefinin belirgin altında kalmaktadır — ortalamalar iyi görünse de alt kırılımlarda ciddi performans farkları var ("Karpuz SLA" sendromu).
- Lokasyonlar arası medyan çözüm süresi **2,2 saat ile 15,1 saat arasında** değişmekte (~7 kat fark), standart bir müdahale refleksinin oturmadığını gösteriyor.
- HVAC/Klima gibi kritik alt kategorilerde FRT uyumu **%32,9**'a kadar düşüyor; bu alanlar dış tedarikçi bağımlılığından kaynaklanan yapısal darboğazlar.
- Lokasyon tipleri arasında proaktiflik farkı belirleyici: Main **%39,49**, Enterprise **%23,70**, Suites **%0** proaktif talep oranı — proaktif tespit çözüm süresini %33 hızlandırıyor.
- Toplam talep hacminin %80'i yalnızca 27 alt kategoriden geliyor (Pareto analizi) — kaynak optimizasyonu buraya odaklanmalı.

## Öneriler (özet)

- Saha ekiplerine proaktif ticket hedefleri ve ziyaret KPI'ları tanımlanması (kısa vade).
- Kronikleşen HVAC/tedarikçi kaynaklı sorunlar için SLA sözleşmelerinin sıkılaştırılması.
- Chatbot ve yapay zeka destekli otomatik kategorizasyon/yönlendirme (orta-uzun vade).
- Problem endeksi yüksek lokasyonlarda churn riski yönetimi ve düzenli saha denetimi.
- Merkezi, gerçek zamanlı yönetici KPI dashboard'u.

## Görseller

Power BI dashboard'undan öne çıkan panolar:

- Şekil 1. Genel Operasyonel Performans Panosu
- Şekil 2. Kategori Bazlı Problem Endeksi ve Pareto Analizi
- Şekil 3. Alt Kategori Bazlı Problem Endeksi (İlk 15)
- Şekil 4. Lokasyon Bazlı Proaktiflik Oranı ve Medyan Çözüm Süresi
- Şekil 5. Lokasyon Bazlı Üye Başına Ticket Yoğunluğu
- Şekil 6. Lokasyon Tipi Bazlı Performans Analizi

## Kullanılan Araçlar

- Python (veri işleme, istatistiksel analiz, modelleme)
- Microsoft Power BI (görselleştirme, dashboard)
- Microsoft Excel
- Microsoft Word

## Dosya

- `coworking-itsm-bitirme-projesi.docx`: Projenin tam metni (literatür, metodoloji, bulgular, sonuç ve öneriler dahil)

## Yazar

**Cengizhan Çelik**
İstanbul Medipol Üniversitesi
Yönetim Bilişim Sistemleri

## Lisans

Bu çalışma akademik amaçlarla [CC BY-NC 4.0](https://creativecommons.org/licenses/by-nc/4.0/deed.tr) lisansı ile paylaşılmıştır. Çalışmadan yararlanılması durumunda uygun şekilde kaynak gösterilmelidir.
