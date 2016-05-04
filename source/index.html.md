---
title: Nutanix Intentful API Reference

language_tabs:
  - shell
  - python
  - powershell

toc_footers:
  - <a href='#'>Sign Up for a Developer Key</a>
  - <a href='https://github.com/tripit/slate'>Documentation Powered by Slate</a>

includes:
  - networks
  - errors

search: true
---

# Introduction

The Nutanix intentful API moves programming from the user to the machine.

We have language bindings in Shell, Python, and Powershell. You can view code examples in the dark area to the right, and you can switch the programming language of the examples with the tabs in the top right.

This example API documentation page was created with [Slate](https://github.com/tripit/slate). Feel free to edit it and use it as a base for your own API's documentation.

# Authentication

> To authorize, use this code:

```python
import kittn

class TestRestApi():                
  def __init__(self):
    
    self.serverIpAddress = "ip_address"
    self.username = "cluster_username"
    self.password = "cluster_password"
    BASE_URL = 'https://%s:9440/PrismGateway/services/rest/v1/'
    self.base_url = BASE_URL % self.serverIpAddress
    self.session = self.get_server_session(self.username, self.password)
```

```powershell
$ipAddress = "ip_address"
$clusterUserName = "cluster_username"
$clusterPassword = "cluster_password"
Connect-NutanixCluster -Server $ipAddress -UserName $clusterUserName `
  -Password $clusterPassword -AcceptInvalidSSLCerts
```

```shell
# With shell, you can just pass the correct header with each request
curl "api_endpoint_here"
  -H "Authorization: meowmeowmeow"
```