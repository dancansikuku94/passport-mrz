# passport-mrz
# Simple passport reader

A very simple python backend API with flask to extract text informations from a passport image file.

## ROLE
THIS APP ONLY SERVES TO DEMONSTRATE THE BASIC USE OF [PassportEye](https://pypi.org/project/PassportEye/) TO SCAN THE MACHINE READABLE ZONES (MRZ) THEN IMPROVE THE RESULT WITH [Tesseract OCR](https://github.com/tesseract-ocr/tesseract).

## Prerequisite
First of all, make sure you have [Docker](https://docs.docker.com/engine/installation/) Engine installed in your system.

## Quickstart
 Build the app with docker compose.
```
docker-compose up --build
```
## Endpoint `http://0.0.0.0:5000/api/v1/OCR`
This is the only one endpoint of this app and accept one `POST` parameter :
- `imagefile` : An image file of the passport. For mobile app, we can use the camera.

##### A sample response:
```json
{
    "country": "Kenya",
    "country_code": "KEN",
    "first_name": "Dancan",
    "last_name": "Sikuku",
    "nationality": "Kenya",
    "number": "X00X00000",
    "sex": "M"
}
```

