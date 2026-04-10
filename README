# QR Code Generator

Small static web app for generating QR codes from URLs. The interface lets you choose the protocol, enter a destination URL, preview the QR code in the browser, open the generated link for testing, and download the QR code as a PNG file.

## Overview

This project consists of a single HTML page with embedded CSS and JavaScript. QR generation is handled in the browser using the `qrcode` library loaded from a CDN. The repository also includes a minimal httpd-based Docker Compose setup for serving the page locally or behind a reverse proxy.

## Features

- Generate a QR code for any HTTP or HTTPS URL
- Choose the URL protocol from a dropdown
- Customize QR foreground and background colors
- Preview the generated QR code in-browser
- Open the target URL with a built-in test link
- Download the generated QR code as a PNG file
- Use a filename derived from the target URL for downloads

## Requirements

You only need one of the following:

- A modern web browser, if you want to open the page directly
- Docker and Docker Compose, if you want to serve it with httpd

## Run Locally

Because the application is fully client-side, the fastest way to use it is to open `index.html` in a browser.

### Option 1: Open the HTML file directly

1. Open `index.html` in your browser.
2. Select `http://` or `https://`.
3. Enter the target URL without the protocol.
4. Choose the QR dark and light colors.
5. Click **Generate QR Code**.
6. Use **Test QR Code Link** to verify the destination.
7. Use **Download QR Code** to save the PNG.

### Option 2: Serve it locally with any static file server

If you prefer serving the file over HTTP, any static server will work. For example:

```bash
python3 -m http.server 8080
```

Then open `http://localhost:8080` in your browser.

## Run With Docker Compose

The repository includes an httpd service that mounts `index.html` into the default apache web root.

### Start the app
cd into the directory of the project and run the following command
```bash
docker-compose up -d
```

### Stop the app
cd into the directory of the project and run the following command
```bash
docker-compose down
```

### Default container behavior

- Uses the latest httpd image
- Serves `index.html` from `/usr/share/httpd/html/index.html`
- You can create a `docker_compose.override.yml` file to expose port 80 or change settings specific to your environment

## How It Works

1. Enter a URL
2. Choose your colors
3. Test the address
4. Download the QR code as a .png image

## Notes

- The URL input expects a value without `http://` or `https://`, although the script also removes either protocol if the user includes it.

## License

MIT License &copy; 2025 Harbor City Church, Derek Peterson
