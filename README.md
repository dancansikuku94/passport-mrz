#  Passport MZR scanner

 Python backend API with flask to extract text informations from a passport image file.

## ROLE
THIS APP ONLY SERVES TO DEMONSTRATE  USE OF [PassportEye] library (https://pypi.org/project/PassportEye/) TO SCAN THE MACHINE READABLE ZONES (MRZ) THEN IMPROVE THE RESULT WITH [Tesseract OCR] library (https://github.com/tesseract-ocr/tesseract).

## Prerequisite
To use the API, ensure you have installed  [Docker](https://docs.docker.com/engine/installation/) Engine in your system.

## Quickstart
 Build the app with docker compose.
```
docker-compose up --build
```
## Endpoint `http://0.0.0.0:5000/api/v1/OCR`
This is the API  endpoint and accept one `POST` parameter :
- `imagefile` : An image file of the passport. For mobile app, we use the camera.

##### A sample  Json response of the API:
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

