# Flight-Tracking-Application

![ağ projesi](https://github.com/user-attachments/assets/b8644e3a-a493-4f3c-a66c-3ab614c66fac)

# Uçuş Verileri Görselleştirme Projesi

Bu proje, OpenSky Network API'si ve statik veri dosyalarını kullanarak uçuş verilerini dinamik ve statik bir şekilde görselleştiren bir web uygulamasıdır. Proje, dünya haritası üzerinde uçakların hızlarını, rotalarını ve konumlarını etkileşimli olarak göstermeyi amaçlar.

## Özellikler

- **Dinamik Veri Kullanımı:**
  - OpenSky Network API'sinden gerçek zamanlı uçuş verileri alınır.
  - Kullanıcı tarafından belirlenen coğrafi sınırlar dahilinde uçakların konum ve hız bilgileri görselleştirilir.

- **Statik Veri Kullanımı:**
  - CSV formatında 4500 uçuş kaydı içeren bir veri dosyası kullanılır.
  - Uçuş hızları dünya haritası üzerinde renkli bir skala ile gösterilir.
  - Kaynak ülke ile uçakların mevcut konumları arasında rotalar çizilir.

- **Etkileşimli Haritalar:**
  - Uçakların hızlarına göre renkli ve boyutlandırılmış noktalar.
  - Kaynak ülke ve uçak rotalarını gösteren çizgiler.
  - Hover özelliği ile uçak ID'si, hız ve kaynak ülke gibi ek bilgiler.

- **Kolay Kullanıcı Arayüzü:**
  - Streamlit ile sade bir web uygulaması.
  - API kullanıcı adı ve şifre girişi, coğrafi sınırların ayarlanması.

---

## Kullanılan Teknolojiler ve Kütüphaneler

### Programlama Dili:
- **Python**

### Framework ve Kütüphaneler:
1. **[Streamlit](https://streamlit.io/):**
   - Kullanıcı arayüzü ve web uygulaması geliştirme.
2. **[Requests](https://pypi.org/project/requests/):**
   - API'den uçuş verilerini çekmek için HTTP isteği.
3. **[Pandas](https://pandas.pydata.org/):**
   - Veri işleme ve düzenleme.
4. **[Plotly](https://plotly.com/):**
   - Etkileşimli haritalar ve grafikler.
   - `plotly.express` ve `plotly.graph_objects` modülleri.
5. **[OpenSky Network API](https://opensky-network.org/):**
   - Gerçek zamanlı uçuş verilerini sağlama.

### Diğer:
- **Ortografik Harita Projeksiyonu:**
  - Dünya haritasını küresel bir görünümde gösterme.
- **CSV Veri İşleme:**
  - Statik uçuş verilerinin işlenmesi.

---

## Kurulum ve Kullanım

### 1. Gereksinimler
- Python 3.8+ sürümü.
- `pip` paket yöneticisi.

### 2. Gerekli Kütüphanelerin Kurulumu
Aşağıdaki komut ile gerekli kütüphaneleri yükleyin:
```bash
pip install streamlit pandas plotly requests
```

### 3. Projenin Çalıştırılması
1. **`app.py` Dosyası (Dinamik Veri):**
   - OpenSky Network API kullanıcı adı ve şifrenizi girin.
   - Aşağıdaki komut ile uygulamayı başlatın:
     ```bash
     streamlit run app.py
     ```

2. **`app2.py` Dosyası (Statik Veri):**
   - Statik veri dosyasını (`tum_dunya.csv`) kullanarak uçuş verilerini görselleştirir.
   - Aşağıdaki komut ile uygulamayı başlatın:
     ```bash
     streamlit run app2.py
     ```

---

## Proje Yapısı

```
.
├── app.py                # Dinamik veri (API) kullanan uygulama
├── app2.py               # Statik veri (CSV) kullanan uygulama
├── tum_dunya.csv         # Statik veri dosyası
└── README.md             # Proje açıklama dosyası
```

---

## Örnek Veri

### **`tum_dunya.csv` İçeriğinden Örnek:**
```csv
,id,icao24,Çağrı İşareti,Kaynak Ülke,Zaman Pozisyonu,Son Temas,Long,Lat,Baro İrtifası,Yerde,Hız,Gerçek İz,Dikey Hız,Sensörler,Geo Yükseklik,Squawk,Spi,Konum Kaynağı
0,7c35e7,KXL     ,Australia,1714025360,1714025360,150.8523,-31.0833,396.24,false,53.5,313.05,-0.98,Veri Yok,441.96,4405,false,0
1,88044a,AIQ377  ,Thailand,1714025411,1714025411,102.2897,2.7496,9966.96,false,240.47,321.34,3.25,Veri Yok,10668.0,Veri Yok,false,0
2,88044f,AIQ3230 ,Thailand,1714025383,1714025383,100.6092,13.9266,Veri Yok,true,0,118.12,Veri Yok,Veri Yok,Veri Yok,Veri Yok,false,0
```

---

## Görseller

1. **Uçak Hızları Haritası:**
   - Dünya haritası üzerinde hızların renk skalası ile gösterimi.
2. **Uçak Rotaları Haritası:**
   - Kaynak ülke ile uçakların mevcut konumları arasındaki rotalar.

---

## Katkıda Bulunma
Proje ile ilgili katkıda bulunmak isterseniz, lütfen bir **pull request** gönderin veya bir **issue** açarak bize ulaşın.

---

**Geliştiriciler:**  
- **Arif Özcan** - 200541024  
- **Furkan Taşan** - 210541010

