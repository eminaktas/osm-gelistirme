## [OSM Geliştirme - Ana sayfa](../README.md)

# OSM Geliştirme ortamı hazırlanması

OSM ortamında geliştirme çalışmaları yapılabilmesi için kullanılacak modül için Python sanal ortamın hazırlanması (venv) ve Python paketlerin kurulması Pycharm IDE ve IDE bağımsız olarak iki farklı şekilde bütün adımlar bu sayfada bahsedilmektedir.

OSM Python3 versiyonu kullanılmaktadır. Specific olarak Python3.8 kullanılabilir.
```bash
# Python version kontrolü
python3 -V
``` 

## Python sanal ortam oluşturma (venv)

Modül bazlı çalışma gerçekleştirirken her modülün kullandığı paketler ve versiyonları farklıdır. Bu paket versiyonların karışmaması için venv kullanılması karışıklığın önüne geçerek ortamın daha sade olması sağlanır.

### IDE'siz kurulum

```bash
# 1. Yöntem
# Sanal ortal oluşturulması için gerekli paket kurulumu
sudo apt install python3-venv
# Sanal ortamın oluşturulması için gerekli komut
python3 -m venv <hedef-klasör-ismi>
python3 -m venv <modül-klasör-ismi>/venv
# 2. Yöntem
# virtualenv apt paketi kurulumu
sudo apt install virtualenv
# Komut sonrasında 
virtualenv <hedef-klasör-ismi> -p/--python <python-exe>
virtualenv <modül-klasör-ismi>/venv -p python3
```

Sanal ortam mutlaka modül içerisinde oluşturulmalıdır.

### Pycharm IDE ile kurulum

Pycharm ile modül klasöürünü proje olarak açtığınız anda size sanal ortam kurulması için soracaktır. Bununla birlikte `requirements.txt` dosyası aynı klasör içerisinde bulunduğu için paket kurulumlarınında yapılması sağlanabilmektedir. Paket kurulumu için [buraya](#paket-kurulumu) gidin.

![pycharm venv sorgusu](ekran-goruntuleri/pycharm-venv-sorgusu.png)

Ekran görüntüsünde görüldüğü gibi `OK` tıklanarak ortamın paket kurulumuyla birlikte sağlanır.

Eğer bu sorgu ile karşılaşılmaz ise Pycharm arayüzü üzerinden sağ alt köşeden `<No interpreter>` seçilerek (burada seçili Python interpreter olabilir) ardından `Add Interpreter` tıklanır.

![no interpreter](ekran-goruntuleri/no-interpreter.png)

Karşınıza çıkan ekran size yeni bir sanal ortam oluştur seçeneği hali hazırda ekran görüntüsünde görüldüğü gibi gelcektir.

![add new interpreter](ekran-goruntuleri/add-new-interpreter.png)

`OK` seçilerek yeni sanal ortam oluşturulur.

## Paket Kurulumu

TODO

OSM topluluğu tarafından hazırlanan geliştirme ortamı hazırlanması rehberi:
- https://osm.etsi.org/docs/developer-guide/02-developer-how-to.html