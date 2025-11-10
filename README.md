# Webcam Capture

A simple static webpage to access your webcam in the browser and capture snapshots in real-time using the MediaDevices API.

## Features
- Request camera permissions and stream live video
- Capture a frame to a canvas/image
- Works as a standalone static HTML page (no backend required)

## How to use
1. Open `webcam.html` in a modern browser (Chrome, Edge, Firefox)
2. Allow camera permission when prompted
3. Use the on-page controls to take a snapshot

## Notes
- Some browsers require HTTPS for camera access. Running from `file://` may be blocked; use a local server or deploy to HTTPS hosting.
- On GitHub Pages, place this folder in a Pages-enabled repo (this one) and open the `webcam.html` URL in your site.

## License
This project is provided as-is by the repository owner. Add a license file if you intend to distribute.
