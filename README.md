# Service-worker-generator-
A simple script to give your web app native abilities 







# Service Worker Generator

A simple web-based tool to generate a service worker (`sw.js`) script for your projects by selecting your project folder and caching your files automatically. It also supports excluding specific files or folders from caching and allows downloading the generated `sw.js` file.

## Features

- Pick your project folder using a directory picker in the browser.
- Recursively scans all files and folders.
- Option to exclude specific files or folders from being cached.
- Generates a basic service worker script that caches your selected files.
- Provides a button to download the generated `sw.js` file.
- Easy integration with your HTML through a registration snippet.

## How to use

1. Open the `index.html` file in a modern browser (Google Chrome, Microsoft Edge) supporting the File System Access API.
2. Click **Pick Folder** and select your project folder.
3. (Optional) Enter file or folder names to exclude from caching, separated by commas.
4. View the list of cached files and the generated service worker code.
5. Click **Download sw.js** to save the service worker script.
6. Add the downloaded `sw.js` to your project root or desired location.

## Registering Service Worker in your project

Add this script to your `index.html` (or main HTML file) to register the service worker:




<script> if ('serviceWorker' in navigator) { window.addEventListener('load', () => { navigator.serviceWorker.register('/sw.js') .then(registration => { console.log('Service Worker registered with scope:', registration.scope); }) .catch(error => { console.error('Service Worker registration failed:', error); }); }); } </script>




Make sure the path in `register('/sw.js')` matches the location of your service worker file.

## Requirements

- A modern browser that supports the File System Access API (e.g., Chrome, Edge).
- HTTPS or `localhost` for service worker registration when deployed.
  
## Limitations

- The directory picker API might not be supported in all browsers.
- The generated service worker script is basic and intended for caching static assets. Customize as needed for advanced use cases.

## License

MIT License

---

Created with ❤️ by [Kinen Key Samson]
