# 🧮 Calculator Microservice

A simple Node.js microservice built with Express to perform basic arithmetic operations via RESTful APIs.

---

## 📦 Features

- Addition (`/add`)
- Subtraction (`/subtract`)
- Multiplication (`/multiply`)
- Division (`/divide`)
- Exponentiation (`/power`)
- Modulo (`/modulo`)
- Square root (`/sqrt`)
- Error handling for invalid inputs and edge cases

---

## 📡 API Endpoints

All endpoints accept **POST** requests with a JSON body.

---

### ➕ `POST /add`

**Request:**
```json
{ "num1": 5, "num2": 3 }
```

**Response:**
```json
{ "result": 8 }
```

---

### ➖ `POST /subtract`

**Request:**
```json
{ "num1": 10, "num2": 4 }
```

**Response:**
```json
{ "result": 6 }
```

---

### ✖️ `POST /multiply`

**Request:**
```json
{ "num1": 6, "num2": 7 }
```

**Response:**
```json
{ "result": 42 }
```

---

### ➗ `POST /divide`

**Request:**
```json
{ "num1": 10, "num2": 2 }
```

**Response:**
```json
{ "result": 5 }
```

⚠️ Returns error if `num2` is 0.

---

### 🧮 `POST /power`

**Request:**
```json
{ "num1": 2, "num2": 3 }
```

**Response:**
```json
{ "result": 8 }
```

---

### ➰ `POST /modulo`

**Request:**
```json
{ "num1": 10, "num2": 3 }
```

**Response:**
```json
{ "result": 1 }
```

⚠️ Returns error if `num2` is 0.

---

### √ `POST /sqrt`

**Request:**
```json
{ "num": 25 }
```

**Response:**
```json
{ "result": 5 }
```

⚠️ Returns error if input is negative.

---

## ❗ Error Handling Examples

### 🔹 Invalid types

**Request:**
```json
{ "num1": "abc", "num2": 5 }
```

**Response:**
```json
{ "error": "The input parameters num1 and num2 must be numeric types" }
```

---

### 🔹 Division by zero

**Request:**
```json
{ "num1": 10, "num2": 0 }
```

**Response:**
```json
{ "error": "The divisor cannot be 0" }
```

