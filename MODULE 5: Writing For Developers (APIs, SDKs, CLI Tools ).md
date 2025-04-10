# Module 5: Writing for Developers (APIs, SDKs, CLI Tools)

👨‍💻 **Understanding How Developers Use Documentation**

Before diving into the specifics of writing developer documentation, it's essential to understand how developers actually use it. Developer documentation is not just about explaining features—it's about enabling developers to integrate, extend, and troubleshoot software effectively. It acts as a bridge between software products and their users, who, in this case, are developers.

**Key ways developers use documentation:**

- 📚 **Learning**: Understand how to use a new API, SDK, or CLI tool.
- 🔍 **Reference**: Look up syntax, parameters, return types, and error codes.
- 🧪 **Testing**: Try out endpoints or functions with sample data.
- 🔧 **Troubleshooting**: Diagnose issues using error messages and logs.

Good developer documentation is fast to navigate, accurate, and code-focused. It should be up-to-date and clearly show how to implement something with working code examples.

---

🔌 **Documenting REST APIs**

REST APIs are the backbone of many web services today. Writing clear, structured, and comprehensive documentation for REST APIs is crucial for adoption and usage.

**What to include in REST API documentation:**

1. **Overview**
   - 🔍 Brief introduction to what the API does.
   - 🧭 Authentication methods (API keys, OAuth).
   - 🔐 Security details (HTTPS, tokens).

2. **Endpoints**
   - Each endpoint should have:
     - URL path (e.g., `/api/users`)
     - HTTP method (GET, POST, PUT, DELETE)
     - Description of what it does

3. **Request Format**
   - Required headers (e.g., `Authorization`, `Content-Type`)
   - Query parameters and path variables
   - Request body (JSON examples)

4. **Response Format**
   - Status codes (200, 201, 400, 401, 404, 500)
   - JSON structure returned by the server
   - Headers returned

5. **Error Codes**
   - Detailed descriptions for all possible error codes
   - Suggestions or steps to resolve common issues

6. **Examples**
   - Realistic code samples using curl, Postman, or programming languages (Python, JavaScript)

```bash
# Example GET request using curl
curl -H "Authorization: Bearer <token>" https://api.example.com/v1/users
```

```json
{
  "id": "12345",
  "name": "Jane Doe",
  "email": "jane@example.com"
}
```

---

🔮 **Writing for GraphQL and WebSockets**

### **GraphQL**
GraphQL is different from REST in that clients specify what data they need. This makes documentation even more important.

**What to document:**
- 📄 Schema overview (types, queries, mutations, subscriptions)
- 🛠️ Arguments for queries/mutations
- 🔄 Returned fields
- ⚠️ Error handling (validation, authorization errors)
- 🔬 Examples of queries and expected responses

```graphql
query GetUser {
  user(id: "123") {
    name
    email
  }
}
```

### **WebSockets**
WebSockets allow bi-directional communication. They're used for real-time apps like chats and live notifications.

**Documentation should cover:**
- 🔗 Connection details (e.g., wss://)
- 🔐 Authentication flow
- 📤 Events that can be sent and received
- 🧾 Message format (JSON payloads)
- 🔁 Reconnect logic

```json
{
  "event": "message",
  "data": {
    "user": "John",
    "text": "Hello World"
  }
}
```

---

📦 **Documenting SDKs (JavaScript, Python, etc.)**

SDKs are libraries that simplify API use in specific programming languages. Developers rely on SDK docs to learn how to call the API efficiently.

**Important things to include:**

1. **Installation Guide**
   - NPM, pip, Maven, etc.
   - System requirements

```bash
npm install example-sdk
# or
pip install example-sdk
```

2. **Authentication Setup**
   - How to import and configure the client

```js
import { Client } from 'example-sdk';
const client = new Client({ token: 'YOUR_API_TOKEN' });
```

3. **Usage Examples**
   - Clear, working code for each function
   - Include parameters and return types

```python
from example_sdk import Client

client = Client(api_key="abc123")
user = client.get_user("123")
print(user.email)
```

4. **Reference Section**
   - Full API surface with parameters and types
   - Default values and optional/required flags

5. **Versioning**
   - API/SDK version numbers
   - Changelog

6. **Best Practices**
   - Handling rate limits
   - Caching responses
   - Error retry strategies

---

🧰 **Using OpenAPI, Swagger, and Postman**

**OpenAPI/Swagger** provides a standardized way to describe your REST APIs. This helps generate interactive documentation automatically.

### **OpenAPI Specification (OAS)**
- YAML or JSON file defining the API
- Supports request/response modeling
- Describes security, tags, and endpoints

```yaml
paths:
  /users:
    get:
      summary: Get all users
      responses:
        '200':
          description: Successful response
```

### **Swagger UI**
- Generates interactive HTML documentation from OAS
- Allows devs to test endpoints directly in the browser

### **Postman**
- Tool for testing APIs manually
- Allows you to create shared collections with:
  - Environments
  - Authorization headers
  - Automated tests and monitors

**Best Practices:**
- Keep OAS files in version control
- Automate documentation updates on API changes
- Use tags to group endpoints logically

---

🌍 **Creating Multilingual Code Samples**

Multilingual code samples help make documentation more inclusive. Developers come from different language backgrounds, and seeing their preferred language can accelerate adoption.

**Languages to prioritize:**
- JavaScript (Node.js)
- Python
- Java
- Go
- Ruby
- C#

**Tips:**
- Provide the same functionality in each language.
- Use syntax highlighting and tabs in web-based docs.
- Keep comments consistent and helpful.

```js
// JavaScript: Fetch user
fetch('https://api.example.com/users/123', {
  headers: {
    Authorization: 'Bearer TOKEN'
  }
})
  .then(res => res.json())
  .then(console.log);
```

```python
# Python: Fetch user
import requests
headers = {"Authorization": "Bearer TOKEN"}
response = requests.get("https://api.example.com/users/123", headers=headers)
print(response.json())
```

```java
// Java: Fetch user
HttpClient client = HttpClient.newHttpClient();
HttpRequest request = HttpRequest.newBuilder()
    .uri(URI.create("https://api.example.com/users/123"))
    .header("Authorization", "Bearer TOKEN")
    .build();

HttpResponse<String> response = client.send(request, BodyHandlers.ofString());
System.out.println(response.body());
```

---

✅ **Conclusion: The Developer-First Mindset**

Writing for developers means writing with empathy and clarity. Keep these guiding principles in mind:

- 🧠 **Be concise** but thorough.
- 🛠️ **Show, don’t tell** – code examples are everything.
- 🚦 **Anticipate errors** and provide troubleshooting guidance.
- 🧩 **Structure content logically** for fast navigation.
- 🔁 **Keep docs in sync** with codebase changes.

Well-documented APIs, SDKs, and CLI tools don’t just enhance developer experience—they drive product adoption and success.

