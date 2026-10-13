# Go Web Server

A small web server written in Go as a practice project. It uses only the standard
library (`net/http`) and demonstrates the basics of routing, form handling, and
serving static pages embedded directly in the binary.

## Features

- Three routes: home page, form page, and a plain-text hello endpoint
- HTML files embedded into the executable with `//go:embed`, so no extra files are needed at runtime
- Form submission handling with `ParseForm` and `FormValue`
- HTTP method checks with proper `405 Method Not Allowed` responses and `Allow` headers
- Support for `HEAD` requests through `http.ServeContent`
- No third-party dependencies

## Routes

| Method | Path     | Description                          |
|--------|----------|--------------------------------------|
| GET    | `/`      | Serves the home page (`index.html`)  |
| GET    | `/form`  | Serves the form page (`form.html`)   |
| POST   | `/form`  | Processes the submitted name/address |
| GET    | `/hello` | Returns `Hello, world!`              |

## Project Structure
