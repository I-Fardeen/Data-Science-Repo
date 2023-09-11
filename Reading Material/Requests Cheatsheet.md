# Requests Library in Python Cheat Sheet 🐍🌐

Made with :heart: by **Fardeen Ahmad Khan**

Welcome to the world of web requests in Python using the Requests library! This cheat sheet is your essential guide to making HTTP requests and interacting with web APIs. Be sure to follow the author, [Fardeen Ahmad Khan](https://github.com/I-Fardeen), for more Python insights and updates! 🙌

🚀 **1. Installation**:
   - Install the Requests library using pip.

   ```python
   pip install requests
   ```

🌐 **2. Sending GET Requests**:
   - Use `requests.get()` to send a GET request to a URL.

   ```python
   import requests

   response = requests.get('https://example.com')
   ```

📤 **3. Sending POST Requests**:
   - Send POST data with `requests.post()`.

   ```python
   data = {'key': 'value'}
   response = requests.post('https://example.com', data=data)
   ```

🔑 **4. Headers**:
   - Add custom headers to your request.

   ```python
   headers = {'User-Agent': 'My-App'}
   response = requests.get('https://example.com', headers=headers)
   ```

🔍 **5. Query Parameters**:
   - Include query parameters in the URL.

   ```python
   params = {'param1': 'value1', 'param2': 'value2'}
   response = requests.get('https://example.com', params=params)
   ```

🔒 **6. Handling Authentication**:
   - Authenticate using various methods (Basic, OAuth, etc.).

   ```python
   auth = ('username', 'password')
   response = requests.get('https://example.com', auth=auth)
   ```

🚦 **7. Response Handling**:
   - Access response content and attributes.

   ```python
   content = response.text
   status_code = response.status_code
   ```

🕒 **8. Handling Timeouts**:
   - Set timeouts for requests to prevent long waits.

   ```python
   response = requests.get('https://example.com', timeout=5)
   ```

🔄 **9. Session Handling**:
   - Use sessions to persist certain parameters across requests.

   ```python
   session = requests.Session()
   session.get('https://example.com')
   session.post('https://example.com/login', data={'user': 'username'})
   ```

📦 **10. Error Handling**:
  - Implement error handling for robust code.

    ```python
    try:
        response = requests.get('https://example.com')
        response.raise_for_status()
    except requests.exceptions.HTTPError as e:
        print(f"HTTP error occurred: {e}")
    ```

Now that you've mastered the Requests library, you're ready to build powerful Python applications that interact with web services and APIs! 🚀🌐

Made with :heart: by **Fardeen Ahmad Khan**
