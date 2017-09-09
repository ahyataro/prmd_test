# Sample API JSON Schema

In this schema file, we represents the public interface of Sample API in JSON Hyper Schema draft v4.

## <a name="resource-product">Product</a>

Stability: `prototype`

FIXME

### Attributes

| Name | Type | Description | Example |
| ------- | ------- | ------- | ------- |
| **created_at** | *date-time* | when product was created | `"2015-01-01T12:00:00Z"` |
| **id** | *uuid* | unique identifier of product | `"01234567-89ab-cdef-0123-456789abcdef"` |
| **name** | *string* | unique name of product | `"example"` |
| **updated_at** | *date-time* | when product was updated | `"2015-01-01T12:00:00Z"` |

### <a name="link-POST-product-/products">Product Create</a>

Create a new product.

```
POST /products
```


#### Curl Example

```bash
$ curl -n -X POST https://example.com/products \
  -d '{
}' \
  -H "Content-Type: application/json"
```


#### Response Example

```
HTTP/1.1 201 Created
```

```json
{
  "created_at": "2015-01-01T12:00:00Z",
  "id": "01234567-89ab-cdef-0123-456789abcdef",
  "name": "example",
  "updated_at": "2015-01-01T12:00:00Z"
}
```

### <a name="link-DELETE-product-/products/{(%23%2Fdefinitions%2Fproduct%2Fdefinitions%2Fidentity)}">Product Delete</a>

Delete an existing product.

```
DELETE /products/{product_id_or_name}
```


#### Curl Example

```bash
$ curl -n -X DELETE https://example.com/products/$PRODUCT_ID_OR_NAME \
  -H "Content-Type: application/json"
```


#### Response Example

```
HTTP/1.1 200 OK
```

```json
{
  "created_at": "2015-01-01T12:00:00Z",
  "id": "01234567-89ab-cdef-0123-456789abcdef",
  "name": "example",
  "updated_at": "2015-01-01T12:00:00Z"
}
```

### <a name="link-GET-product-/products/{(%23%2Fdefinitions%2Fproduct%2Fdefinitions%2Fidentity)}">Product Info</a>

Info for existing product.

```
GET /products/{product_id_or_name}
```


#### Curl Example

```bash
$ curl -n https://example.com/products/$PRODUCT_ID_OR_NAME
```


#### Response Example

```
HTTP/1.1 200 OK
```

```json
{
  "created_at": "2015-01-01T12:00:00Z",
  "id": "01234567-89ab-cdef-0123-456789abcdef",
  "name": "example",
  "updated_at": "2015-01-01T12:00:00Z"
}
```

### <a name="link-GET-product-/products">Product List</a>

List existing products.

```
GET /products
```


#### Curl Example

```bash
$ curl -n https://example.com/products
```


#### Response Example

```
HTTP/1.1 200 OK
```

```json
[
  {
    "created_at": "2015-01-01T12:00:00Z",
    "id": "01234567-89ab-cdef-0123-456789abcdef",
    "name": "example",
    "updated_at": "2015-01-01T12:00:00Z"
  }
]
```

### <a name="link-PATCH-product-/products/{(%23%2Fdefinitions%2Fproduct%2Fdefinitions%2Fidentity)}">Product Update</a>

Update an existing product.

```
PATCH /products/{product_id_or_name}
```


#### Curl Example

```bash
$ curl -n -X PATCH https://example.com/products/$PRODUCT_ID_OR_NAME \
  -d '{
}' \
  -H "Content-Type: application/json"
```


#### Response Example

```
HTTP/1.1 200 OK
```

```json
{
  "created_at": "2015-01-01T12:00:00Z",
  "id": "01234567-89ab-cdef-0123-456789abcdef",
  "name": "example",
  "updated_at": "2015-01-01T12:00:00Z"
}
```


