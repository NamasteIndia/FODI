Fast OneDrive Index / FODI — A fast OneDrive listing program that requires no server.

🔍 Preview
DEMO

✨ Features
Specify display paths

Password protection for specific folders

Free deployment with no server required

Preview support for basic text, images, audio, video, and Office documents

⚠️ Limitations
Simple features, minimalistic UI

Not compatible with Internet Explorer and UWP version of Microsoft Edge

📌 Updates
2025.02.12
Partial WebDAV functionality added (list, upload, download, copy, move)

2024.09.15
Upload support added (create a .upload file in the upload directory)

2019.12.23
Improved speed

Added Cloudflare Workers backend

2019.12.07
Improved speed

Added Python 3.6 backend

🚀 Installation
Deploy FODI backend on Cloudflare

FODI Deployment Helper

📖 Notes
WEBDAV
Account & Password Setup:
Set secrets in Environment Variables, with the variable name WEBDAV, like this:

json
Copy
Edit
{
  "user1": "password",
  "user2": "password"
}
File upload limits:

Free Plan: 100MB

Business Plan: 200MB

Enterprise Plan: 500MB

Preview Support
PDF: For local PDF previews, download and extract PDF.js, rename the folder to pdfjs.
Comment out the condition fileOrigin !== viewerOrigin in viewer.mjs, and change the URL prefix //mozilla.github.io/pdf.js/web/viewer.html?file=.

Markdown: Enable GitHub-style alerts and KaTeX formatting through the "Optional Markdown extensions" settings in the UI.

Download
Use return downloadFile(file, requestUrl.searchParams.get('format'), true); — the third argument allows the Worker to act as a proxy.

Access via https://example.com/a.html?format= to specify the output format.
Supported conversion formats
