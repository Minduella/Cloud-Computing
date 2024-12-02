
# Dictionary API

Sebuah API Backend Service yang menyediakan kumpulan aksara-aksara bali.API ini sudah berjalan dalam server cloud dengan base url https://kaliatra.et.r.appspot.com/

## Endpoint route 




#### Ambil semua Data Dictionary

```http
  /api/entry
```
- Method
  - Get
- Body
  - ```id``` as ```int```
  - ```aksara``` as ```string```
  - ```tulisanlatin``` as ```string```
  - ```deskripsi``` as ```string```
  - ```category``` as ```string```
  - ```imageUrl``` as ```file```
  - ```createdAt``` as ```Timestamp```
- Response
```
{
        "id": "0CNvPPfZKclQ7qXncRIz",
        "aksara": "᭄ᬖ",
        "tulisanlatin": "gantungan ga gora",
        "deskripsi": "aksara yang menyimbulkan \"gantungan ga gora\"",
        "category": "gantungan_swalalita",
        "imageUrl": "https://storage.googleapis.com/kaliatra/1732165885132-Gantungan_Ga_gora.png",
        "createdAt": "2024-11-21T05:11:25.197Z"
} 
```
#### Ambil Data Dictionary Berdasarkan Kategory

```http
   /api/entry/categories/:category
```
- Method
  - Get
-  Body
  - ```id``` as ```int```
  - ```aksara``` as ```string```
  - ```tulisanlatin``` as ```string```
  - ```deskripsi``` as ```string```
  - ```category``` as ```string```
  - ```imageUrl``` as ```file```
  - ```createdAt``` as ```Timestamp```
- Response
```
{
        "id": "0CNvPPfZKclQ7qXncRIz",
        "aksara": "᭄ᬖ",
        "tulisanlatin": "gantungan ga gora",
        "deskripsi": "aksara yang menyimbulkan \"gantungan ga gora\"",
        "category": "gantungan_swalalita",
        "imageUrl": "https://storage.googleapis.com/kaliatra/1732165885132-Gantungan_Ga_gora.png",
        "createdAt": "2024-11-21T05:11:25.197Z"
} 
```

- cateogry
  - Angka Aksara Bali
  - Aksara Swara Pendek Hreswa
  - Pangangge Ardhaswara
  - Pangangge Tengenan
  - Aksara Wyanjana Deret Modern Swalalita
  - Aksara Wyanjana Deret Modern Wresastra
  - gantungan_swalalita
  - gantungan_wresastra
  - tanda_baca





## FAQ

#### 1.Kok pas dicoba get kategori atau entry nya nampilin error cannot get %0A

Ini dapat diakibatkan dari url yang menyisakan spasi di akhir url contohnya "/api/entry " hal ini dianggap invalid oleh sistem dan akan menampilkan pesan error tersebut sehingga tolong pastikan agar tidak menambahkan atau mengurangi endpoint yang sudah diberikan.



## Bug/Error

Untuk Bug dan Error baru yang ditemukan dapat menghubungi contributor yang bersangkutan


