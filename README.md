# Kaliatra Cloud Computing Division

## Team Members
| Name                   | ID            | Institution                            | Role               | Status  |
|------------------------|---------------|---------------------------------------|--------------------|---------|
| I Made Andre Sentanu  | c113b4ky1852  | Institut Teknologi dan Bisnis STIKOM Bali | Cloud Computing    | Active  |

## Tools Used
The following tools and technologies were utilized in the development of this cloud computing project:

1. **Visual Studio Code** - Code editor for writing and managing code.
2. **Google Cloud Storage** - Used for storing and managing files in the cloud.
3. **Google Cloud Firestore** - NoSQL database for storing structured data.
4. **JavaScript** - Programming language used for backend development.
5. **Node.js** - Runtime environment for executing JavaScript server-side.
6. **Firebase Admin SDK** - For managing Firebase services programmatically.
7. **Postman** - API testing and documentation tool.

## Project Description
This project focuses on implementing cloud computing solutions using modern tools and technologies. It integrates Google Cloud services and Firebase for authentication backend system for machine learning model with mobile development side.

## API

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

