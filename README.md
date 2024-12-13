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

# Model API

Sebuah API Backend Service yang menyediakan kumpulan aksara-aksara bali.API ini sudah berjalan dalam server cloud run dengan base url https://model-api-852069596535.asia-southeast2.run.app

## Endpoint route 




#### Prediksi Aksara 

```http
  /predict
```
- Method
  - POST
-  Header
  - ```Authorization``` value ```Bearer <token>```
- Body
  - ```image``` as ```file```
- Response
```
{
    "status": "success",
    "message": "Prediction successful",
    "data": {
        "id": "91e142cf-de1a-4432-8e7d-70a8c766f7f3",
        "userId": "Fy2VQAxxzWZdTjXK6yKyRtT2p5r1",
        "topPredictions": [
            "ba:100.00%",
            "wa:0.00%",
            "na:0.00%"
        ],
        "imageURL": "https://storage.googleapis.com/kaliatra/result/91e142cf-de1a-4432-8e7d-70a8c766f7f3.jpg?GoogleAccessId=firebase-adminsdk-4z880%40kaliatra.iam.gserviceaccount.com&Expires=1740787200&Signature=N8SzbVQ5KLQzD%2F0oltUNgwon%2FGzko88kcHjjoIV2EcA%2BrgC853yk5G3YDMDfviXyLn56ANcsDV7m90d3%2BzeCZzMMHaYJK7H7JMvZPGazEBqQQO3FiFyMnRwEhYl0ReZ1e31rNng1cBXY6SMLZMckqs7P7DF3MERtWGxt0ibELHupCqUnEXmlVAVPnU6I0ZkXWbAvHyhyR2FTFg2CA0dYgKTHE7wF40gvTR%2BI1pMeMTubJoMzH9UV7NfnlyXcF3Ueer4kfnQVBp%2FZe0lI4BAhH2LQ%2B7NfSC4j9X5nLuheyf24J4I58Tgf9EubGiEIbW87zmIrjxkm60%2BC3H56xKI6Gw%3D%3D",
        "createdAt": "2024-12-09T16:23:10.771Z"
    }
}
```
#### Prediksi Result

```http
   /predict/latest
```
- Method
  - Get
-  Header
  - ```Authorization``` value ```Bearer <token>```
- Response
```
{
    "status": "success",
    "message": "Latest prediction retrieved successfully",
    "data": {
        "id": "b18531e3-73f5-4500-9801-c36b5d8667f2",
        "topPredictions": [
            "ga:100.00%",
            "ja:0.00%",
            "wa:0.00%"
        ],
        "imageURL": "https://storage.googleapis.com/kaliatra/result/b18531e3-73f5-4500-9801-c36b5d8667f2.jpg?GoogleAccessId=firebase-adminsdk-4z880%40kaliatra.iam.gserviceaccount.com&Expires=1740787200&Signature=oP%2FG3nn7SRLjNScp6JbENwMuwfWCjHsJ2VjV9bU7Q6%2FG19yzYf0r6lqZt2%2Fde3cObdBwI43uITYucPUgk1cIozr9yQgu9bFRAaj8zi4J%2F%2FsAh3t7JNpHHqsoBmXDzYNBYs6kxKMK1xpkRJai0dRPGGZPlPUyJeovl9qXE7dyIxQFBirZkNCGj%2FcVqI9SDPeLLwPb702WbvYb9P%2BfYFr7pFtsTmUC%2B5TurEkzCSa4wk49yKpY9Mhtqu%2FCmkmnmpx66woFBeakuB0dtc1ZxdEiGiz7xZU6JtxoKilkmCoFpSQUMrFSqGnC4V0lXbZOc%2F9brsWLzqFv0bRd8RnkzUGuCw%3D%3D",
        "createdAt": "2024-12-09T16:25:10.108Z"
    }
}
```
#### Prediksi Handwriting

```http
   /predict/handwrite
```
- Method
  - POST
-  Header
  - ```Authorization``` value ```Bearer <token>```
-  Body
  - ```image``` as ```file```
- Response
```
{
    "status": "success",
    "message": "Prediction successful",
    "data": {
        "id": "a88c2a04-c438-432e-aa3c-c0f01403a4a7",
        "userId": "Fy2VQAxxzWZdTjXK6yKyRtT2p5r1",
        "topPredictions": [
            "ga:99.55%",
            "ja:0.45%",
            "wa:0.00%"
        ],
        "imageURL": "https://storage.googleapis.com/kaliatra/result/a88c2a04-c438-432e-aa3c-c0f01403a4a7.jpg?GoogleAccessId=firebase-adminsdk-4z880%40kaliatra.iam.gserviceaccount.com&Expires=1740787200&Signature=eoOMabQzi0Z03vNPeZS9i3KOwQ285nuZW0idHoTXgevsKm%2FM9viGv7IfLz9dCN5WNevCGgso4YrA8tS3mAJUY2aMifKdqgrmpaUNI8Ejzzhqh2%2FJt29%2B%2FD74LIeWH1Y%2FPGnBd6e3RXVcNZjJ5AbHT0EOvemZ8J4nUZ2dG3fejcaj4jio4DlkpqV9xcLk2v1rPbum5yDtM1dCfxMAh4K07L9k9VA36WGM%2BIcXQq%2F24IY7MXzXASUmoaSHCo1%2Bxyc0ydEmkJ%2BZidVOpKl6winnwvlMZv9odgUDcpQtI207rOvJmQak8yrR%2BWjxM%2FTAPV0BKnUCs8ilsUk1Byts6LHYjw%3D%3D",
        "createdAt": "2024-12-09T16:24:22.427Z"
    }
}
```
#### Prediksi Histories

```http
   /predict/histories
```
- Method
  - GET
-  Header
  - ```Authorization``` value ```Bearer <token>```
- Response
```
{
    "status": "success",
    "message": "Histories retrieved successfully",
    "data": [
        {
            "id": "6fb95820-cd86-4a9a-befc-d163d629e90a",
            "topPredictions": [
                "ga:100.00%",
                "ja:0.00%",
                "wa:0.00%"
            ],
            "imageURL": "https://storage.googleapis.com/kaliatra/result/6fb95820-cd86-4a9a-befc-d163d629e90a.jpg?GoogleAccessId=firebase-adminsdk-4z880%40kaliatra.iam.gserviceaccount.com&Expires=1740787200&Signature=KbuR08P00pIeEk7ec0DKnl1c3qjpdnzP3X%2F2zpH3%2BmpIBd2he2p23IYboZ1aY%2FvI50BRv%2BWn%2Bq%2F2VlIf3lcc8GH6kc7pD2qcO7%2BssFOmqjk3GDF3UhFiH17lnlgYRMXSxfw40NRspv7bTJ346BnLhV%2BNx2BwJO7CeJ3zNmPfqV9ENuH8QO89dPpzp8M4xrXxhbJz8E3Z3PEwGwB2W4c3LE%2FbwBrDz6UP2daCTWPVTlE9uVmUyflzMT0kwdeX9UiODQQR%2Fi6juJ9iuwpyaPqIvAkVDsfGcWyJI4Xx5FADjO58JYBvR%2BkB0Ded7bhbDDEInSce1kYXo6DW8FhXj7lkUQ%3D%3D",
            "createdAt": "2024-12-09T16:25:49.816Z"
        },
}
```
#### Hapus Prediksi Histories

```http
   /predict/histories/:id
```
- Method
  - DELETE
-  Header
  - ```Authorization``` value ```Bearer <token>```
- Response
```
{
    "status": "success",
    "message": "Prediction with ID 7cd73138-8043-4144-b6d4-8208f5d76a66 deleted successfully"
}
```
untuk :id berasal dari id prediction bukan user id


## Bug/Error

Untuk Bug dan Error baru yang ditemukan dapat menghubungi contributor yang bersangkutan


