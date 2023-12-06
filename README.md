# ik-project

# Culturama Backend Documentation
Repository for cloud computing

## Culturama API Documentation
### Authentication
#### Register

* Endpoint: /api/auth/register
* Method: POST
* Request Body:
  * fullname (string): User’s fullname
  * email (string): User's email
  * password (string): User's password

* Response
  * If successful:
    * Status Code: 200
    * JSON Response:
      ```json
      {
        "error": false,
        "message": "Berhasil Mendaftarkan Akun. Silahkan Login"
      }

  * If email is already taken:
    * Status Code: 404
    * JSON Response:
      ```json
      {
        "error": true,
        "message": "Email Sudah Digunakan oleh orang lain"
      }

### Login 
* Endpoint: /api/auth/login
* Method: POST
* Request Body:
  * email (string): User's email
  * password (string): User's password

* Response:
  * If successful:
  * Status Code: 200
  * JSON Response:
    ```json
    {
      "error": false,
      "loginResult": {
        "email": "muhammadfattah@gmail.com",
        "fullname": "Muhammad Fattah Al Rasyidin",
        "token": "<access_token>",
        "userid": 1
      },
      "message": "Login Success"
    }
  * If email or password is incorrect:
    * Status Code: 200
    * JSON Response:
      ```json
      {
        "error": true,
        "message": "Wrong Password or Account not found"
      }

 
