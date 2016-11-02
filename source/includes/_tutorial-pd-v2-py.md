# Protection Domain Tutorial (v2)

This REST API Python tutorial shows you how to: define cluster connection, authenticate to a cluster, get cluster information, create a protection domain, find unprotected VMs, and add the unprotected VMs to a protection domain.

## Before you begin

Install Python library requests.

You can download the completed script at https://github.com/nutanix/Connection-viaREST/blob/master/api_python_authenticate_pd.py.

You can download the sample response to this script at https://github.com/nutanix/Connection-viaREST/blob/master/api_python_authenticate_pd_sample_response.txt.

## Summary


```python
import json
import os
import random
import requests
import sys
import traceback
import pprint

class TestRestApi():                
  def __init__(self):
    
    self.serverIpAddress = "ip_address"
    self.username = "cluster_username"
    self.password = "cluster_password"
    BASE_URL = 'https://%s:9440/PrismGateway/services/rest/v1/'
    self.base_url = BASE_URL % self.serverIpAddress
    self.session = self.get_server_session(self.username, self.password)

def get_server_session(self, username, password):
 
    session = requests.Session()
    session.auth = (username, password)
    session.verify = False                                            
    session.headers.update(
        {'Content-Type': 'application/json; charset=utf-8'})
    return session
```

1.  Import the modules for the Python code. The indicated modules should be included in your script:
2.  Authenticate cluster connection by defining the cluster IP address, user name, password, and base URL.

    The `BASE_URL = 'https://%s:9440/PrismGateway/services/rest/v1/'` line sets up the REST services that are hosted in Prism Gateway.
    - Replace `ip_address` with the cluster virtual IP address.
    - Replace `cluster_username` with the cluster user name.
    - Replace `cluster_password` with the cluster password.
3.  Create a REST client session for a server connection.
    If using a self-signed certificate, disable the SSL certificate verification by setting it to FALSE. Without disabling the SSL certificate verification, the script will not run on the interface.
