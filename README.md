# 🔗 URL Shortener

A simple and efficient URL Shortener service built with **Go**.  
It allows users to shorten long URLs and redirect back to the original URLs seamlessly.

---

## 🚀 Features

- Shortens any valid URL into a compact hash-based ID
- Redirects shortened URLs back to their original destinations
- In-memory storage using Go's `map`
- Lightweight and fast server using `net/http`
- Easy to run locally — no database needed!

---

## 🛠️ Tech Stack

- [Go (Golang)](https://golang.org/) — Backend server
- [Postman](https://www.postman.com/) — For API testing
- [MD5 Hashing](https://en.wikipedia.org/wiki/MD5) — For URL shortening

---

## 📦 Setup Instructions

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/url-shortener-go.git
cd url-shortener-go
```

### 2. Run the Server

```bash
go run main.go
```

Server will start on:  
```
http://localhost:3000
```

---

## 📄 API Usage

### 1. Shorten a URL

- **Endpoint**: `POST /shorten`
- **Request Body** (JSON):

```json
{
  "url": "https://github.com/realShailendra"
}
```

- **Response** (JSON):

```json
{
  "short_url": "http://localhost:3000/redirect/1a2b3c4d"
}
```

You will get a shortened URL you can use.

---

### 2. Redirect to the Original URL

- **Endpoint**: `GET /redirect/{short_id}`

Example:

```
http://localhost:3000/redirect/1a2b3c4d
```

This will automatically redirect you to:

```
https://github.com/realShailendra
```

---

## 📬 Testing with Postman

1. Set method to **POST**.
2. URL: `http://localhost:3000/shorten`
3. In **Body** tab:
   - Choose **raw** → **JSON** format
   - Add your JSON:

```json
{
  "url": "https://example.com"
}
```

4. Click **Send**.
5. Use the returned `short_url` in your browser!

---

## ⚡ Improvements (Next Steps)

- Persist shortened URLs into a database (e.g., MongoDB, Redis)
- Add expiration time for short links
- Add analytics (click count, country stats, etc.)
- Deploy using Docker
- Use a custom domain for shorter links (like `short.ly/xyz123`)

---



## ✨ Author

Built with ❤️ by Shailendra Gupta (https://github.com/realShailendra)

