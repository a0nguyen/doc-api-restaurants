---
title: API Reference

language_tabs: # must be one of https://git.io/vQNgJ
  - shell
  - python
  - javascript

includes:
  - errors

search: true

code_clipboard: true
---

# Introduction

Welcome to Vech Connect Restaurants! You can use our API to access marketplaces data for restaurants

You can view code examples in the dark area to the right, and you can switch the programming language of the examples with the tabs in the top right.

# Authentication

> To authorize, use this code:

```python
headers = {
    'x-api-key': 'your_api_key',
}

```

```shell
# With shell, you can just pass the correct header with each request
curl "api_endpoint_here" \
  -H "x-api-key: your_api_key"
```

```javascript
const headers = {
  'x-api-key': 'your_api_key'
}
```

> Make sure to replace `your_api_key` with your API key.

Vech connect uses API keys to allow access to the API. We'll personnally send you your api key.

Vech connect expects for the API key to be included in all API requests to the server in a header that looks like the following:

`x-api-key: your_api_key`

<aside class="notice">
You must replace <code>your_api_key</code> with your personal API key.
</aside>

# Rappi for restaurants
## Create a user

```python
import requests

url = 'https://www.vech-connect.com/restaurants/rappi/users'

payload = {
    'email': 'm.colag@mirazur.fr',
    'password': 'MirazurMenton*',
    'user_id': '11'
}

headers = {
  'x-api-key': 'your_api_key',
  'Content-Type': 'application/json'
}

response = requests.request('POST', url, headers=headers, json=payload)

print(response.text)

```

```shell
curl --location --request POST 'https://www.vech-connect.com/restaurants/rappi/users' \
--header 'x-api-key: your_api_key' \
--header 'Content-Type: application/json' \
--data-raw '{
    "email": "m.colag@mirazur.fr",
    "password": "MirazurMenton*",
    "user_id": "11"
}'
```

```javascript
const axios = require('axios')
const data = JSON.stringify({'email':'m.colag@mirazur.fr','password':'MirazurMenton*','user_id':'11'});

const config = {
  method: 'post',
  url: 'https://www.vech-connect.com/restaurants/rappi/users',
  headers: { 
    'x-api-key': 'your_api_key', 
    'Content-Type': 'application/json'
  },
  data : data
};

(() => {
  try {
  const { data } = await axios(config)
  console.log(JSON.stringify(response.data))
  } catch (error) {
      console.log(error)
  }
})()
```

> The above command returns JSON structured like this:

```json
{
    
}
```

This endpoint allows you to create and get data for a restaurant using rappi.

### HTTP Request

`POST https://www.vech-connect.com/restaurants/rappi/users`

### Payload

Parameter | Description
--------- | -----------
email|User's email used to log in Rappi
password|User's password used to log in Rappi
user_id|User's id in your backend


## Get a user

```python
import requests

url = 'https://www.vech-connect.com/restaurants/rappi/users/2'

headers = {
  'x-api-key': 'your_api_key',
  'Content-Type': 'application/json'
}

response = requests.request('GET', url, headers=headers)

print(response.text)

```

```shell
curl 'https://www.vech-connect.com/restaurants/rappi/users/2' \
--header 'x-api-key: your_api_key' \
--header 'Content-Type: application/json'
```

```javascript
const axios = require('axios')

const config = {
  method: 'get',
  url: 'https://www.vech-connect.com/restaurants/rappi/users',
  headers: { 
    'x-api-key': 'your_api_key', 
    'Content-Type': 'application/json'
  },
}

(() => {
  try {
  const { data } = await axios(config)
  console.log(JSON.stringify(response.data))
  } catch (error) {
      console.log(error)
  }
})()
```

> The above command returns JSON structured like this:

```json
{
    
}
```

This endpoint allows you get data for a restaurant using rappi you have previously created

### HTTP Request

`GET https://www.vech-connect.com/restaurants/rappi/users/<ID>`

## Response
Whenever you create or get a user, the response is the same.

```json
{
    
}
```
<aside class="notice">
From our experience here is the most important data:
</aside>
Parameter | Description
--------- | -----------
email|User's email used to log in Rappi
password|User's password used to log in Rappi
user_id|User's id in your backend

# Didi Food for restaurants

## Create a user

```python
import requests

url = 'https://www.vech-connect.com/restaurants/didi-food/users'

payload = {
    'phone': '15576749098',
    'password': 'MirazurMenton*',
    'user_id': '11'
}

headers = {
  'x-api-key': 'your_api_key',
  'Content-Type': 'application/json'
}

response = requests.request('POST', url, headers=headers, json=payload)

print(response.text)

```

```shell
curl --location --request POST 'https://www.vech-connect.com/restaurants/didi-food/users' \
--header 'x-api-key: your_api_key' \
--header 'Content-Type: application/json' \
--data-raw '{
    "email": "m.colag@mirazur.fr",
    "password": "MirazurMenton*",
    "user_id": "11"
}'
```

```javascript
const axios = require('axios')
const data = JSON.stringify({'email':'m.colag@mirazur.fr','password':'MirazurMenton*','user_id':'11'});

const config = {
  method: 'post',
  url: 'https://www.vech-connect.com/restaurants/didi-food/users',
  headers: { 
    'x-api-key': 'your_api_key', 
    'Content-Type': 'application/json'
  },
  data : data
};

(() => {
  try {
  const { data } = await axios(config)
  console.log(JSON.stringify(response.data))
  } catch (error) {
      console.log(error)
  }
})()
```

> The above command returns JSON structured like this:

```json
{
    
}
```

This endpoint allows you to create and get data for a restaurant using didi-food.

### HTTP Request

`POST https://www.vech-connect.com/restaurants/didi-food/users`

### Payload

Parameter | Description
--------- | -----------
phone|User's phone used to log in Didi Food
password|User's password used to log in Didi Food
user_id|User's id in your backend


## Get a user

```python
import requests

url = 'https://www.vech-connect.com/restaurants/didi-food/users/2'

headers = {
  'x-api-key': 'your_api_key',
  'Content-Type': 'application/json'
}

response = requests.request('GET', url, headers=headers)

print(response.text)

```

```shell
curl 'https://www.vech-connect.com/restaurants/didi-food/users/2' \
--header 'x-api-key: your_api_key' \
--header 'Content-Type: application/json'
```

```javascript
const axios = require('axios')

const config = {
  method: 'get',
  url: 'https://www.vech-connect.com/restaurants/didi-food/users',
  headers: { 
    'x-api-key': 'your_api_key', 
    'Content-Type': 'application/json'
  },
}

(() => {
  try {
  const { data } = await axios(config)
  console.log(JSON.stringify(response.data))
  } catch (error) {
      console.log(error)
  }
})()
```

> The above command returns JSON structured like this:

```json
{
    
}
```

This endpoint allows you get data for a restaurant using didi-food you have previously created

### HTTP Request

`GET https://www.vech-connect.com/restaurants/didi-food/users/<ID>`

