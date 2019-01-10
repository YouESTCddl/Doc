# API Retrieve

## Retrieve

### Evaluate

**GET** /api/retrieve/evaluate/:cid

#### Request

* **description** string

#### Response

* Success

    HTTP 200

    ```json
    {
        "message": "OK",
        "price": 123
    }
    ```

* Cloth not found

    HTTP 404

    ```json
    {
        "message": "CLOTH_NOT_FOUND"
    }
    ```

### Reserve

**POST** /api/retrieve/reserve

#### Request

* **time** string
* **place** string
* **remark** string
* **phone** string

#### Response

* Success

    HTTP 200

    ```json
    {
        "message": "OK",
        "rid": "asdasdasd"
    }
    ```

* Invalid Form

    HTTP 422

    ```json
    {
        "message": "INVALID_FORM"
    }
    ```

### QueryReservationInfo

**GET** /api/retrieve/:rid

#### Response

* Success

    HTTP 200

    ```json
    {
        "message": "OK",
        "time": "time",
        "place": "place",
        "remark": "remark",
        "phone": "1231231233"
    }
    ```

* Invalid rid

    HTTP 422

    ```json
    {
        "message": "INVALID_RID"
    }
    ```

### QueryClothInfo

**GET** /api/cloth/:cid

#### Response

* Success

    HTTP 200

    ```json
    {
        "message": "OK",
        "price": "asdasd",
        "validity": "time",
        "picture": "cdn.asd.com/static/asd",
        "retrieved": true,
        "retrieve_time": "time"
    }
    ```

* Cloth not found

    HTTP 404

    ```json
    {
        "message": "CLOTH_NOT_FOUND"
    }
    ```
