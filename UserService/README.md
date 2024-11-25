# springboot-with-actuator

This service is containing the CRUD operation of userDetails and implemented the Actuator endpoints to monitor the application.

## Usage Of API

To test the API, you can use the following `cURL` command:
<details>
    <summary>Create API</summary>

### using window OS use Below URL
```bash
Invoke-WebRequest -Uri "http://localhost:8082/api/v1/users" `
    -Method POST `
    -Headers @{Accept="*/*"; "Content-Type"="application/json"} `
    -Body '{"firstName": "Santosh", "lastName": "Kumar", "contact": "802228181", "email": "sant@Gmail.com"}'

```
### using OS AS Linux/MAC use Below URL
```bash
curl -X 'POST' \
  'http://localhost:8082/api/v1/users' \
  -H 'accept: */*' \
  -H 'Content-Type: application/json' \
  -d '{
   "firstName": "Santosh",
  "lastName": "Kumar",
  "contact": "802228181",
  "email": "sant@Gmail.com"
}'
```

### Explanation:
1. **Markdown Syntax**:
    - The backticks define the code block.
    - Adding `bash` after the opening backticks ensures proper syntax highlighting.

2. **Command Breakdown**:
    - `-X POST`: Specifies the HTTP method.
    - `-H`: Adds a header, like `Content-Type`.
    - `-d`: Specifies the data payload.

3. **Rendered Output**:
   When above CURl will execute, it will appear output as a formatted code block as below:
````json 
{
   "userId": 1,
   "firstName": "Santosh",
   "lastName": "Kumar",
   "contact": "802228181",
   "email": "sant@Gmail.com"
   }
````
</details>

<details>
    <summary>Get All Users details</summary>

### using window OS use Below URL
```bash
Invoke-WebRequest -Uri "http://localhost:8082/api/v1/users" `
    -Method GET `
    -Headers @{Accept="*/*"; "Content-Type"="application/json"} `
    
```
### using OS AS Linux/MAC use Below URL
```bash
curl -X 'GET' \
  'http://localhost:8082/api/v1/users' \
  -H 'accept: */*'
```

### Explanation:
1. **Markdown Syntax**:
    - The backticks define the code block.
    - Adding `bash` after the opening backticks ensures proper syntax highlighting.

2. **Command Breakdown**:
    - `-X POST`: Specifies the HTTP method.
    - `-H`: Adds a header, like `Content-Type`.

3. **Rendered Output**:
   When above CURl will execute, it will appear output as a formatted code block as below:
````json 
[
  {
    "userId": 1,
    "firstName": "Santosh",
    "lastName": "Kumar",
    "contact": "802228181",
    "email": "sant@Gmail.com"
  }
]
````
</details>

<details>
    <summary>Get Specific User details By userId</summary>

### using window OS use Below URL
```bash
Invoke-WebRequest -Uri "http://localhost:8082/api/v1/users/{userId}?userId=1" `
    -Method GET `
    -Headers @{Accept="*/*";
     "Content-Type" = "application/json"}

```
### using OS AS Linux/MAC use Below URL

```bash
curl -X 'GET' \
  'http://localhost:8082/api/v1/users/{userId}?userId=2' \
  -H 'accept: */*'
```

### Explanation:
1. **Markdown Syntax**:
    - The backticks define the code block.
    - Adding `bash` after the opening backticks ensures proper syntax highlighting.

2. **Command Breakdown**:
    - `-X POST`: Specifies the HTTP method.
    - `-H`: Adds a header, like `Content-Type`.

3. **Rendered Output**:
   When above CURl will execute, it will appear output as a formatted code block as below:
````json 
{
    "userId": 2,
    "firstName": "Santosh",
    "lastName": "Kumar",
    "contact": "802228181",
    "email": "sant@Gmail.com"
  }
````
</details>

<details>
    <summary>Update Specific User By userId</summary>

### use Below command on windows machine 
```bash
Invoke-WebRequest -Uri "http://localhost:8082/api/v1/users/{userId}?userId=1" `
    -Method PUT `
    -Headers @{Accept="*/*"; "Content-Type"="application/json"} `
    -Body '{"firstName": "Santosh", "lastName": "Kumar", "contact": "802228381", "email": "sant@Gmail.com"}'

```
### Use below command on Linux/MAC
```bash
curl -X 'PUT' \
  'http://localhost:8082/api/v1/users/{userId}?userId=1' \
  -H 'accept: */*' \
  -H 'Content-Type: application/json' \
  -d '{
  "firstName": "Santosh",
  "lastName": "Kumar",  
  "contact": "802228181",
  "email": "sant@Gmail.com"
}'
```

### Explanation:
1. **Markdown Syntax**:
    - The backticks define the code block.
    - Adding `bash` after the opening backticks ensures proper syntax highlighting.

2. **Command Breakdown**:
    - `-X POST`: Specifies the HTTP method.
    - `-H`: Adds a header, like `Content-Type`.

3. **Rendered Output**:
   When above CURl will execute, it will appear output as a formatted code block as below:
````json 
{
    "userId": 2,
    "firstName": "Santosh",
    "lastName": "Kumar",
    "contact": "802228181",
    "email": "sant@Gmail.com"
  }
````
</details>

<details>
    <summary>Delete Specific User By userId</summary>

### use Below command on windows machine 
```bash
Invoke-WebRequest -Uri "http://localhost:8082/api/v1/users/{userId}?userId=1" `
    -Method DELETE `
    -Headers @{
        Accept = "*/*"; 
        "Content-Type" = "application/json"
    }
    
```
### Use below command on Linux/MAC
```bash
curl -X 'DELETE' \
  'http://localhost:8082/api/v1/users/{userId}?userId=2' \
  -H 'accept: */*'
```

### Explanation:
1. **Markdown Syntax**:
    - The backticks define the code block.
    - Adding `bash` after the opening backticks ensures proper syntax highlighting.

2. **Command Breakdown**:
    - `-X POST`: Specifies the HTTP method.
    - `-H`: Adds a header, like `Content-Type`.

3. **Rendered Output**:
   When above CURl will execute, it will appear output as a formatted code block as below:
````String 
User deleted by UserId : 2
````
</details>