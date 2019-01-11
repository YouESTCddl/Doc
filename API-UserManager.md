# API Document - UserManager

## Login

**POST** /api/login

### Request

* **uid** int
* **passwd** string

### Response

* Success

    HTTP 200

    ```json
    {
        "message": "OK",
        "uid": 2017220101001
    }
    ```

* Uid or Password error

    HTTP 200

    ```json
    {
        "message": "UID_OR_PASSWORD_ERROR"
    }
    ```

* Uid or Password Invalid

    HTTP 200

    ```json
    {
        "message": "UID_OR_PASSWORD_INVALID"
    }
    ```

## Status

**GET** /api/status

### Request

* **Cookie** Cookie || **uid** int

### Response

* Success

    HTTP 200

    ```json
    {
        "message": "OK",
        "uid": 2017220101001
    }
    ```

* Logout

    HTTP 200

    ```json
    {
        "message": "LOGOUT"
    }
    ```

## Logout

**POST** /api/logout

### Request

* **Cookie** Cookie || **uid** int

### Response

* Success

    HTTP 200

    ```json
    {
        "message": "OK"
    }
    ```

* Error

    HTTP 500

    ```json
    {
        "message": "UNKNOWN_ERROR"
    }
    ```

## Reg

**POST** /api/reg

### Request

* **uid** int
* **passwd** string
* **passwd_r** string

### Response

* Success

    HTTP 200

    ```json
    {
        "message": "OK",
        "uid": 2017220101001
    }
    ```

* Uid or Password Invalid

    HTTP 200

    ```json
    {
        "message": "UID_OR_PASSWORD_INVALID"
    }
    ```
