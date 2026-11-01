# AiPilot araç verileri

AiPilot uygulaması araç verilerini (arıza kodu açıklamaları, **müdahale yöntemleri**, OBDb sinyal
kütüphanesi, tarama kapsamı/puanlama, araç profilleri) bu depodan güncel tutar. Uygulama her dosyayı
APK içinde **yedek** taşır; açılışta `surum.json`'a bakıp değişen dosyaları indirir, yoksa yedeği kullanır.

Temel adres: `https://raw.githubusercontent.com/hsynaltunta/aipilot-veri/main/`

| Dosya | İçerik |
|---|---|
| `ariza_kodlari.json` | DTC kodu → Türkçe açıklama |
| `mudahale_yontemleri.json` | DTC kodu/önek → genel müdahale/kontrol yöntemi (topluluk katkılı) |
| `obdb_library.json` | OBDb sinyal tanımları (CC BY-SA 4.0) |
| `tarama_durumu.json` | Model bazlı taranmış bloklar (kapsam/puanlama) |
| `profiles/*.json` | Hazır araç profilleri |
| `surum.json` | Her dosyanın içerik özeti; uygulama değişeni indirir |

Kaynak asset'ler ana uygulama deposundadır; `tools/veri_yayinla.py` bu klasörü üretir. İçerik kullanıcı
taramalarından türetilip güncellenir; ham kişisel veri (VIN/ICCID) **yayınlanmaz**.
