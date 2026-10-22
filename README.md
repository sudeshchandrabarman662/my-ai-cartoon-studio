# My AI Cartoon Studio — 1080p browser prototype

## What this is
A static, browser-only prototype that applies a lightweight cartoon-like color/edge effect to video frames and records a WebM output at a selected output canvas size (1080p/720p/480p). The filter itself runs at a lower working resolution to reduce CPU/memory use, then is scaled up.

## Important limitations
- This is **not generative AI** and does not create true 3D animated characters.
- Output is WebM, not MP4.
- The app attempts to include the original video's audio track. Browser MediaRecorder re-encodes media, so audio is not guaranteed bit-for-bit identical. Check playback and sync.
- 1080p output may be slow on an 8 GB RAM PC with Intel integrated graphics. Start with 5–10 second clips; 720p is recommended for smoother operation.
- Videos are processed locally in the browser; the app does not upload selected videos to a server.
- GitHub Pages hosting is public. Do not upload private videos, passwords, or API keys to your repository.
- True AI 3D cartoon conversion requires a separate licensed AI model and a backend/GPU service. Free GPU hosting is limited and not guaranteed.

## Test locally
Extract the ZIP and open `index.html` in current Chrome or Edge. Select a short video and click the start button.

## Deploy free with GitHub Pages
1. Sign in at https://github.com/
2. Create a repository named `my-ai-cartoon-studio`.
3. Upload `index.html` and `README.md` to the repository root.
4. Go to Settings → Pages.
5. Under Build and deployment, choose `Deploy from a branch`.
6. Select `main` and `/(root)`, then Save.
7. Wait for the published URL shown in Pages settings.

GitHub Free Pages requires a public repository; the website is publicly reachable. See https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site

## Next step for true AI
Add a separate backend that runs a compatible video-to-video model. A static GitHub Pages site cannot run a server-side AI model itself.
