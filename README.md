# Açık Erişim İK Puantaj ve Bordro Hesaplama Mimarisi

[![Puantaj Cetveli](https://img.shields.io/badge/A%C3%A7%C4%B1k_Eri%C5%9Fim-Ayl%C4%B1k_Puantaj-1E3A8A?style=flat-square)](https://generalist.tr/hesaplama/puantaj.php)
[![Bordro Simülatörü](https://img.shields.io/badge/A%C3%A7%C4%B1k_Eri%C5%9Fim-Br%C3%BCt_%E2%86%94_Net_Bordro-0F172A?style=flat-square)](https://generalist.tr/hesaplama/bordro.php)

> İK yöneticileri, mali müşavirler ve uygulayıcılar için oturum açmadan doğrudan tarayıcı üzerinde çalışan **Aylık Puantaj Cetveli** ve **Brüt ↔ Net Maaş / İşveren Maliyeti Simülatörü** mimari özeti.

## 1. Canlı Araçlar (Ücretsiz & Açık Erişim)
1. **[Aylık Puantaj & Eksik Gün Hesaplama Cetveli](https://generalist.tr/hesaplama/puantaj.php)**
   - 30 gün / parmak hesabı (28-29-30-31 gün çeken aylar) SGK gün kuralı uyumu
   - Hafta tatili, genel tatil, ücretsiz izin, rapor ve fazla mesai saatlerinin anlık hesaplanması
   - Yazdırılabilir resmi puantaj cetveli çıktısı
2. **[Brüt ↔ Net Bordro & İşveren Maliyeti Simülatörü](https://generalist.tr/hesaplama/bordro.php)**
   - 12 aylık kümülatif gelir vergisi matrahı ve dilim geçişlerinin otomatik takibi
   - Asgari ücret gelir ve damga vergisi istisnası hesaplaması
   - 5510 sayılı kanun 5 puanlık hazine teşviki dahil/hariç toplam işveren maliyeti analizi
   - Netten brüte (iteratif yakınsama motoru) ve brütten nete çift yönlü hesaplama

## 2. Hesaplama Motoru Akışı

```mermaid
flowchart LR
    P["Günlük Devam & Mesai Verisi"] --> S["SGK 30-Gün / Eksik Gün Kural Motoru"]
    S --> B["Brüt Kazanç & İstisna Hesaplayıcı"]
    B --> V["Kümülatif Gelir Vergisi Dilim Motoru"]
    V --> N["Net Ödeme & İşveren Toplam Maliyet Çıktısı"]
```

## 3. Erişim Bağlantıları
- **Bordro Simülatörü:** [https://generalist.tr/hesaplama/bordro.php](https://generalist.tr/hesaplama/bordro.php)
- **Puantaj Cetveli:** [https://generalist.tr/hesaplama/puantaj.php](https://generalist.tr/hesaplama/puantaj.php)
- **Kişisel Karargâh:** [https://generalist.tr](https://generalist.tr)
