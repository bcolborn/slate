# Networks

## Modify network

### HTTP request

`PUT /networks/{uuid}`

### Query parameters

Parameter | Default | Description | Schema
----------|---------|-------------|-------
uuid | implied | UUID of the network | #/definitions/network

### Responses

Response Code | Meaning
--------------|--------
200 | Success
default | Error schema: #/definitions/network_status

## Get details for a network

### HTTP Request

`GET /networks/{uuid}`

### Query parameters

Parameter | Default | Description | Schema
----------|---------|-------------|-------
uuid | implied | UUID of the network | #/definitions/network

### Responses

Response Code | Meaning
--------------|--------
200 | Success
default | Error schema: #/definitions/network_status

## Delete a network

### HTTP Request

`DELETE /networks/{uuid}`

### Query parameters

Parameter | Default | Description | Schema
----------|---------|-------------|-------
uuid | implied | UUID of the network | #/definitions/network

### Responses

Response Code | Meaning
--------------|--------
200 | Success
default | Error schema: #/definitions/network_status