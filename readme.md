You can create a **simple API wrapper class in Python** that:

1. Stores `api_url`, `business_id`, and `api_name`
2. Validates the API URL
3. Sends a **POST request**
4. Returns the **response to frontend**
5. If an error occurs, returns the **exception**

Here is a clean example.

```python
import requests
from urllib.parse import urlparse

class APIWrapper:
    
    def __init__(self, api_url, business_id, api_name):
        self.api_url = api_url
        self.business_id = business_id
        self.api_name = api_name

    # function to validate url
    def is_valid_url(self):
        try:
            result = urlparse(self.api_url)
            return all([result.scheme, result.netloc])
        except:
            return False

    # function to call api
    def call_api(self, payload):

        try:
            # check url
            if not self.is_valid_url():
                return {"error": "Invalid API URL"}

            # request body
            data = {
                "business_id": self.business_id,
                "api_name": self.api_name,
                "payload": payload
            }

            # send POST request
            response = requests.post(self.api_url, json=data)

            # check response
            if response.status_code == 200:
                return response.json()
            else:
                return {"error": f"API returned status {response.status_code}"}

        except Exception as e:
            return {"exception": str(e)}
```

### Example Usage

```python
api = APIWrapper(
    api_url="https://example.com/api",
    business_id="B123",
    api_name="get_user"
)

payload = {
    "user_id": 101
}

result = api.call_api(payload)

print(result)
```

### How this works (simple explanation)

1. **Class `APIWrapper`** → wraps the API logic.
2. **`__init__()`** → stores `api_url`, `business_id`, `api_name`.
3. **`is_valid_url()`** → checks if URL is valid.
4. **`call_api()`**

   * validates URL
   * sends **POST request**
   * returns response to frontend
   * catches errors and returns exception.

### Example Output

Success:

```json
{
 "name": "John",
 "age": 25
}
```

Error:

```json
{
 "exception": "Connection error"
}
```

---

If you want, I can also show you a **more professional API wrapper used in real AI/ML backend projects (FastAPI / production ready)** which will help you in **AI developer interviews**. 🚀
You can create a **simple API wrapper class in Python** that:

1. Stores `api_url`, `business_id`, and `api_name`
2. Validates the API URL
3. Sends a **POST request**
4. Returns the **response to frontend**
5. If an error occurs, returns the **exception**

Here is a clean example.

```python
import requests
from urllib.parse import urlparse

class APIWrapper:
    
    def __init__(self, api_url, business_id, api_name):
        self.api_url = api_url
        self.business_id = business_id
        self.api_name = api_name

    # function to validate url
    def is_valid_url(self):
        try:
            result = urlparse(self.api_url)
            return all([result.scheme, result.netloc])
        except:
            return False

    # function to call api
    def call_api(self, payload):

        try:
            # check url
            if not self.is_valid_url():
                return {"error": "Invalid API URL"}

            # request body
            data = {
                "business_id": self.business_id,
                "api_name": self.api_name,
                "payload": payload
            }

            # send POST request
            response = requests.post(self.api_url, json=data)

            # check response
            if response.status_code == 200:
                return response.json()
            else:
                return {"error": f"API returned status {response.status_code}"}

        except Exception as e:
            return {"exception": str(e)}
```

### Example Usage

```python
api = APIWrapper(
    api_url="https://example.com/api",
    business_id="B123",
    api_name="get_user"
)

payload = {
    "user_id": 101
}

result = api.call_api(payload)

print(result)
```

### How this works (simple explanation)

1. **Class `APIWrapper`** → wraps the API logic.
2. **`__init__()`** → stores `api_url`, `business_id`, `api_name`.
3. **`is_valid_url()`** → checks if URL is valid.
4. **`call_api()`**

   * validates URL
   * sends **POST request**
   * returns response to frontend
   * catches errors and returns exception.

### Example Output

Success:

```json
{
 "name": "John",
 "age": 25
}
```

Error:

```json
{
 "exception": "Connection error"
}
```

---

If you want, I can also show you a **more professional API wrapper used in real AI/ML backend projects (FastAPI / production ready)** which will help you in **AI developer interviews**. 🚀
You can create a **simple API wrapper class in Python** that:

1. Stores `api_url`, `business_id`, and `api_name`
2. Validates the API URL
3. Sends a **POST request**
4. Returns the **response to frontend**
5. If an error occurs, returns the **exception**

Here is a clean example.

```python
import requests
from urllib.parse import urlparse

class APIWrapper:
    
    def __init__(self, api_url, business_id, api_name):
        self.api_url = api_url
        self.business_id = business_id
        self.api_name = api_name

    # function to validate url
    def is_valid_url(self):
        try:
            result = urlparse(self.api_url)
            return all([result.scheme, result.netloc])
        except:
            return False

    # function to call api
    def call_api(self, payload):

        try:
            # check url
            if not self.is_valid_url():
                return {"error": "Invalid API URL"}

            # request body
            data = {
                "business_id": self.business_id,
                "api_name": self.api_name,
                "payload": payload
            }

            # send POST request
            response = requests.post(self.api_url, json=data)

            # check response
            if response.status_code == 200:
                return response.json()
            else:
                return {"error": f"API returned status {response.status_code}"}

        except Exception as e:
            return {"exception": str(e)}
```

### Example Usage

```python
api = APIWrapper(
    api_url="https://example.com/api",
    business_id="B123",
    api_name="get_user"
)

payload = {
    "user_id": 101
}

result = api.call_api(payload)

print(result)
```

### How this works (simple explanation)

1. **Class `APIWrapper`** → wraps the API logic.
2. **`__init__()`** → stores `api_url`, `business_id`, `api_name`.
3. **`is_valid_url()`** → checks if URL is valid.
4. **`call_api()`**

   * validates URL
   * sends **POST request**
   * returns response to frontend
   * catches errors and returns exception.

### Example Output

Success:

```json
{
 "name": "John",
 "age": 25
}
```

Error:

```json
{
 "exception": "Connection error"
}
```

---

If you want, I can also show you a **more professional API wrapper used in real AI/ML backend projects (FastAPI / production ready)** which will help you in **AI developer interviews**. 🚀
You can create a **simple API wrapper class in Python** that:

1. Stores `api_url`, `business_id`, and `api_name`
2. Validates the API URL
3. Sends a **POST request**
4. Returns the **response to frontend**
5. If an error occurs, returns the **exception**

Here is a clean example.

```python
import requests
from urllib.parse import urlparse

class APIWrapper:
    
    def __init__(self, api_url, business_id, api_name):
        self.api_url = api_url
        self.business_id = business_id
        self.api_name = api_name

    # function to validate url
    def is_valid_url(self):
        try:
            result = urlparse(self.api_url)
            return all([result.scheme, result.netloc])
        except:
            return False

    # function to call api
    def call_api(self, payload):

        try:
            # check url
            if not self.is_valid_url():
                return {"error": "Invalid API URL"}

            # request body
            data = {
                "business_id": self.business_id,
                "api_name": self.api_name,
                "payload": payload
            }

            # send POST request
            response = requests.post(self.api_url, json=data)

            # check response
            if response.status_code == 200:
                return response.json()
            else:
                return {"error": f"API returned status {response.status_code}"}

        except Exception as e:
            return {"exception": str(e)}
```

### Example Usage

```python
api = APIWrapper(
    api_url="https://example.com/api",
    business_id="B123",
    api_name="get_user"
)

payload = {
    "user_id": 101
}

result = api.call_api(payload)

print(result)
```

### How this works (simple explanation)

1. **Class `APIWrapper`** → wraps the API logic.
2. **`__init__()`** → stores `api_url`, `business_id`, `api_name`.
3. **`is_valid_url()`** → checks if URL is valid.
4. **`call_api()`**

   * validates URL
   * sends **POST request**
   * returns response to frontend
   * catches errors and returns exception.

### Example Output

Success:

```json
{
 "name": "John",
 "age": 25
}
```

Error:

```json
{
 "exception": "Connection error"
}
```

---

If you want, I can also show you a **more professional API wrapper used in real AI/ML backend projects (FastAPI / production ready)** which will help you in **AI developer interviews**. 🚀
You can create a **simple API wrapper class in Python** that:

1. Stores `api_url`, `business_id`, and `api_name`
2. Validates the API URL
3. Sends a **POST request**
4. Returns the **response to frontend**
5. If an error occurs, returns the **exception**

Here is a clean example.

```python
import requests
from urllib.parse import urlparse

class APIWrapper:
    
    def __init__(self, api_url, business_id, api_name):
        self.api_url = api_url
        self.business_id = business_id
        self.api_name = api_name

    # function to validate url
    def is_valid_url(self):
        try:
            result = urlparse(self.api_url)
            return all([result.scheme, result.netloc])
        except:
            return False

    # function to call api
    def call_api(self, payload):

        try:
            # check url
            if not self.is_valid_url():
                return {"error": "Invalid API URL"}

            # request body
            data = {
                "business_id": self.business_id,
                "api_name": self.api_name,
                "payload": payload
            }

            # send POST request
            response = requests.post(self.api_url, json=data)

            # check response
            if response.status_code == 200:
                return response.json()
            else:
                return {"error": f"API returned status {response.status_code}"}

        except Exception as e:
            return {"exception": str(e)}
```

### Example Usage

```python
api = APIWrapper(
    api_url="https://example.com/api",
    business_id="B123",
    api_name="get_user"
)

payload = {
    "user_id": 101
}

result = api.call_api(payload)

print(result)
```

### How this works (simple explanation)

1. **Class `APIWrapper`** → wraps the API logic.
2. **`__init__()`** → stores `api_url`, `business_id`, `api_name`.
3. **`is_valid_url()`** → checks if URL is valid.
4. **`call_api()`**

   * validates URL
   * sends **POST request**
   * returns response to frontend
   * catches errors and returns exception.

### Example Output

Success:

```json
{
 "name": "John",
 "age": 25
}
```

Error:

```json
{
 "exception": "Connection error"
}
```

---

If you want, I can also show you a **more professional API wrapper used in real AI/ML backend projects (FastAPI / production ready)** which will help you in **AI developer interviews**. 🚀
You can create a **simple API wrapper class in Python** that:

1. Stores `api_url`, `business_id`, and `api_name`
2. Validates the API URL
3. Sends a **POST request**
4. Returns the **response to frontend**
5. If an error occurs, returns the **exception**

Here is a clean example.

```python
import requests
from urllib.parse import urlparse

class APIWrapper:
    
    def __init__(self, api_url, business_id, api_name):
        self.api_url = api_url
        self.business_id = business_id
        self.api_name = api_name

    # function to validate url
    def is_valid_url(self):
        try:
            result = urlparse(self.api_url)
            return all([result.scheme, result.netloc])
        except:
            return False

    # function to call api
    def call_api(self, payload):

        try:
            # check url
            if not self.is_valid_url():
                return {"error": "Invalid API URL"}

            # request body
            data = {
                "business_id": self.business_id,
                "api_name": self.api_name,
                "payload": payload
            }

            # send POST request
            response = requests.post(self.api_url, json=data)

            # check response
            if response.status_code == 200:
                return response.json()
            else:
                return {"error": f"API returned status {response.status_code}"}

        except Exception as e:
            return {"exception": str(e)}
```

### Example Usage

```python
api = APIWrapper(
    api_url="https://example.com/api",
    business_id="B123",
    api_name="get_user"
)

payload = {
    "user_id": 101
}

result = api.call_api(payload)

print(result)
```

### How this works (simple explanation)

1. **Class `APIWrapper`** → wraps the API logic.
2. **`__init__()`** → stores `api_url`, `business_id`, `api_name`.
3. **`is_valid_url()`** → checks if URL is valid.
4. **`call_api()`**

   * validates URL
   * sends **POST request**
   * returns response to frontend
   * catches errors and returns exception.

### Example Output

Success:

```json
{
 "name": "John",
 "age": 25
}
```

Error:

```json
{
 "exception": "Connection error"
}
```

---

If you want, I can also show you a **more professional API wrapper used in real AI/ML backend projects (FastAPI / production ready)** which will help you in **AI developer interviews**. 🚀
You can create a **simple API wrapper class in Python** that:

1. Stores `api_url`, `business_id`, and `api_name`
2. Validates the API URL
3. Sends a **POST request**
4. Returns the **response to frontend**
5. If an error occurs, returns the **exception**

Here is a clean example.

```python
import requests
from urllib.parse import urlparse

class APIWrapper:
    
    def __init__(self, api_url, business_id, api_name):
        self.api_url = api_url
        self.business_id = business_id
        self.api_name = api_name

    # function to validate url
    def is_valid_url(self):
        try:
            result = urlparse(self.api_url)
            return all([result.scheme, result.netloc])
        except:
            return False

    # function to call api
    def call_api(self, payload):

        try:
            # check url
            if not self.is_valid_url():
                return {"error": "Invalid API URL"}

            # request body
            data = {
                "business_id": self.business_id,
                "api_name": self.api_name,
                "payload": payload
            }

            # send POST request
            response = requests.post(self.api_url, json=data)

            # check response
            if response.status_code == 200:
                return response.json()
            else:
                return {"error": f"API returned status {response.status_code}"}

        except Exception as e:
            return {"exception": str(e)}
```

### Example Usage

```python
api = APIWrapper(
    api_url="https://example.com/api",
    business_id="B123",
    api_name="get_user"
)

payload = {
    "user_id": 101
}

result = api.call_api(payload)

print(result)
```



### Example Output

Success:

```json
{
 "name": "John",
 "age": 25
}
```

Error:

```json
{
 "exception": "Connection error"
}
```

---

