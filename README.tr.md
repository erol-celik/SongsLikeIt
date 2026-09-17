# SongsLikeIt

Şarkıları ses özelliklerine göre analiz edip karşılaştırmayı amaçlayan bir Python projesi. [GTZAN Müzik Türü Veri Seti](http://marsyas.info/downloads/datasets.html) (10 tür: blues, klasik, country, disco, hip-hop, jazz, metal, pop, reggae, rock) üzerine kurulmuştur.

## Proje Durumu

Bu depo henüz erken kurulum aşamasındadır. Şu anda yalnızca proje yapılandırması (`.gitignore`) ile birlikte, git'e dahil edilmeyen yerel bir `data/` (veri seti) klasörü ve yerel bir `venv/` sanal ortamı bulunmaktadır — henüz herhangi bir uygulama kaynak kodu commit edilmemiştir.

## Kullanılan Teknolojiler

Yerel sanal ortamda kurulu olan paketlere bakıldığında, bu projenin şu teknolojilerle inşa edilmesi planlanmaktadır:

- **Python**
- **librosa** — ses dosyalarını yükleme ve özellik çıkarma (ör. MFCC, spektral özellikler)
- **numpy** / **pandas** — sayısal işlemler ve tablo verisi yönetimi
- **soundfile** — ses dosyası okuma/yazma işlemleri

## Veri

`data/` klasörü (git'e dahil değildir — bkz. `.gitignore`) şunları içermesi beklenir:

- `features_30_sec.csv`, `features_3_sec.csv` — önceden çıkarılmış ses özellikleri
- `genres_original/` — türlere göre klasörlenmiş ham ses klipleri
- `images_original/` — türlere göre klasörlenmiş spektrogram görselleri

Boyutları nedeniyle ses dosyaları (`*.wav`, `*.mp3`) ve tüm `data/` klasörü versiyon kontrolünün dışında tutulmuştur. Projeyi yeniden oluşturmak isterseniz, GTZAN veri setini ayrıca indirip yukarıdaki yapıya uygun şekilde `data/` altına yerleştirmeniz gerekir.

## Başlarken

```bash
# Sanal ortam oluşturun ve etkinleştirin
python -m venv venv
venv\Scripts\activate      # Windows
# source venv/bin/activate # macOS/Linux

# Bağımlılıkları kurun (bir requirements dosyası eklendiğinde)
pip install librosa numpy pandas soundfile
```

## Lisans

Bu proje için henüz bir lisans seçilmemiştir.

## Katkıda Bulunma

Bu proje için henüz katkı rehberi bulunmamaktadır. Katkıda bulunmak isterseniz, önerdiğiniz değişiklikleri tartışmak için lütfen önce bir issue açın.
