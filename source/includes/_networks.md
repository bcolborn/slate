# Networks

## Get details for a network

```python
clusterURL = self.base_url + "/networks" + self.net_uuid
print "Getting cluster information for cluster %s" % self.serverIpAddress
serverResponse = self.session.get(clusterURL)
return serverResponse.status_code, json.loads(serverResponse.text)
```

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

## Modify network

```python
clusterURL = self.base_url + "/networks" + self.net_uuid
print "Getting cluster information for cluster %s" % self.serverIpAddress
serverResponse = self.session.put(clusterURL)
return serverResponse.status_code, json.loads(serverResponse.text)
```

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

## Delete a network

```python
clusterURL = self.base_url + "/networks" + self.net_uuid
print "Getting cluster information for cluster %s" % self.serverIpAddress
serverResponse = self.session.delete(clusterURL)
return serverResponse.status_code, json.loads(serverResponse.text)
```

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