# API Document

## UserManager

### Login

**POST** /api/login

#### Request

* **uid** int
* **passwd** string

#### Response

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

### Status

**GET** /api/status

#### Request

* **Cookie** Cookie || **uid** int

#### Response

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

### Logout

**POST** /api/logout

#### Request

* **Cookie** Cookie || **uid** int

#### Response

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

### Reg

**POST** /api/reg

#### Request

* **uid** int
* **passwd** string
* **passwd_r** string

#### Response

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

### Passwd Reset

**PATCH** /std/:uid/passwd/reset

#### Request

* **old_passwd** string
* **new_passwd** string
* **new_passwd_r** string

#### Response

* Success

    HTTP 200

    ```json
    {
        "message": "OK"
    }
    ```

* Uid or Password error

    HTTP 422

    ```json
    {
        "message": "UID_OR_PASSWORD_ERROR"
    }
    ```

* Uid or Password or New Password Invalid

    HTTP 422

    ```json
    {
        "message": "UID_OR_PASSWORD_OR_NEW_PASSWORD_INVALID"
    }
    ```

* New Repeat Password not Same

    HTTP 422

    ```json
    {
        "message": "NEW_REPEAT_PASSWORD_NOT_SAME"
    }
    ```

* New Password same as old one

    HTTP 422

    ```json
    {
        "message": "NEW_PASSWORD_SAME_AS_OLD_ONE"
    }
    ```

* Unknown Error

    HTTP 500

    ```json
    {
        "message": "UNKNOWN_ERROR"
    }
    ```
