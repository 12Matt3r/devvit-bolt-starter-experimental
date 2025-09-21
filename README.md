# TripSitter AI

TripSitter AI is a standalone, browser-based audio-visual experience that uses your webcam or a video file to generate real-time psychedelic and glitch art effects with WebGL. It also integrates several AI-powered features to create generative soundscapes, narrate your "trip," and even write new visual shaders on the fly.

![TripSitter AI Preview](https://i.imgur.com/zJd9f8m.png)

---

## Key Features

*   **Real-Time Video Effects:** Applies complex shaders to your webcam feed or an uploaded video/image file in real-time.
*   **Multiple Shader Effects:** Comes with several built-in effects like Datamosh, Pixel Sort, Feedback loops, and Color Shifting.
*   **Fine-Grained Control:** Adjust dozens of parameters like trail length, motion sensitivity, hue, displacement, and color saturation to customize the visuals.
*   **Effect Presets:** Quickly switch between different visual styles with predefined presets like "Psychedelic," "Ghostly," and "Glitchy VHS."
*   **AI Shader Lab:** Describe a visual effect in plain English, and the AI will attempt to generate a new GLSL shader for you to use instantly. You can also paste raw GLSL code directly for testing.
*   **AI Art Interpretation:** Take a snapshot of the current visual and have the AI provide a poetic, critical interpretation of the art.
*   **AI Soundscapes:** Generate an atmospheric, ambient soundscape with Tone.js based on the AI's analysis of the current visuals.
*   **AI Trip Narration:** Let the AI watch your visual stream and generate a surreal, spoken-word narration for your experience, with optional Text-to-Speech.
*   **AI Copilot:** Control the visual parameters using natural language commands (e.g., "make it more chaotic").
*   **Autonomous Mode:** Let the AI take full control, continuously evolving the shader code and narrating the journey for a unique, hands-free experience.
*   **Recording & Snapshots:** Easily record your visual creations as video files or save high-resolution snapshots.
*   **Share Your Settings:** Generate a unique URL that saves all your current control settings, allowing you to share your exact visual setup with others.
*   **No Installation Required:** Runs entirely in your web browser from a single HTML file.

---

## How to Use

This application is a single, self-contained HTML file and requires no complex installation or build steps.

### Option 1: Run Directly in the Browser

The easiest way to use TripSitter AI is to simply open the `index.html` file in a modern web browser.

1.  Download the `index.html` file to your computer.
2.  Navigate to the folder where you saved it.
3.  Double-click the `index.html` file, or right-click it and select "Open with" and choose a browser like Google Chrome, Mozilla Firefox, or Microsoft Edge.
4.  The application will request permission to use your webcam. You must **Allow** this for the main feature to work.

### Option 2: Run from a Local Web Server (Recommended for some features)

Some browsers have security restrictions about accessing local files (`file://`). For the best experience, especially with file uploads, it's recommended to run it from a simple local web server.

1.  **If you have Python installed:**
    *   Open a terminal or command prompt.
    *   Navigate to the directory containing `index.html`.
    *   Run the command: `python -m http.server`
    *   Open your web browser and go to `http://localhost:8000`.

2.  **If you have Node.js installed:**
    *   Open a terminal or command prompt.
    *   Install a simple server package if you don't have one: `npm install -g serve`
    *   Navigate to the directory containing `index.html`.
    *   Run the command: `serve .`
    *   Open your web browser and go to the local address provided in the terminal (usually `http://localhost:3000`).

---

## Important: AI Features API Key

To use the AI-powered features (Shader Lab, Art Interpretation, Soundscapes, Narration, Copilot), you must provide your own Google Gemini API key.

1.  Open the `index.html` file in a text editor.
2.  Find the line (around line 1250) that looks like this:
    ```javascript
    async function geminiApiCall(payload) {
        const apiKey = ""; // <--- PASTE YOUR API KEY HERE
        // ...
    }
    ```
3.  Paste your Google Gemini API key between the double quotes.
4.  Save the file and open it in your browser. The AI features will now be enabled.

---

## Technology Stack

*   **Frontend:** HTML5, CSS3, Vanilla JavaScript (ES6+)
*   **Graphics:** WebGL for hardware-accelerated real-time shader processing.
*   **Audio:** [Tone.js](https://tonejs.github.io/) for generative soundscapes.
*   **AI:** [Google Gemini API](https://ai.google.dev/) for all generative text and analysis features.
*   **No backend or server-side logic is required.** The application runs entirely on the client-side.
