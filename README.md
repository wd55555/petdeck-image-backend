# Free Image Upload Backend

This is a simple Node.js/Express server for free local image uploads. It saves images to disk and serves them at `/uploads/<filename>`.

## Setup
1. Install Node.js (https://nodejs.org/)
2. In this folder, run:
   ```powershell
   npm install
   node server.js
   ```
3. The server runs at http://localhost:5050/

## Usage
- POST an image to `http://localhost:5050/upload` as `multipart/form-data` with field name `image`.
- The response is `{ imageUrl: "http://localhost:5050/uploads/<filename>" }`
- Images are saved in `uploads/`.

## Flutter Client Changes
- Update your upload flow to POST to `http://localhost:5050/upload` with the image bytes as `image` field.
- Use the returned `imageUrl` as the card image URL.

## Security
- This backend is for local/dev use only. For production, use a real cloud provider or add authentication and storage limits.
