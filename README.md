# 🏛️ MBassy

**MBassy** is a sleek, hyper-lightweight Markdown editor and knowledge hub built for speed, privacy, and portability. It functions as a Single Page Application (SPA) with zero backend, using **Alpine.js** for reactivity and **local storage** for data persistence.

Live at: [m-bassy.netlify.app](https://m-bassy.netlify.app/)

---

## 🚀 Features

* **⚡ Zero-Latency Editing**: Instant Markdown rendering via `marked.js`.
* **🔗 Alpine-Turnout Routing**: A custom-built, lightweight router for seamless SPA navigation.
* **💾 Local-First**: Your data never leaves your browser. Auto-saves to LocalStorage.
* **📡 Transmit & Import**: Share notes via encoded URL hashes. No database required.
* **🎨 High-Contrast UI**: A clean, distraction-free interface built with Tailwind CSS.

## 🛠️ Tech Stack

* **Core**: [Alpine.js](https://alpinejs.dev/)
* **Routing**: [Alpine-Turnout](https://github.com/your-username/alpine-turnout)
* **Styling**: [Tailwind CSS](https://tailwindcss.com/)
* **Parsing**: [Marked.js](https://marked.js.org/)

---

## 📂 Installation & Local Development

Since MBassy is a client-side application, you don't need `npm` or `pip` to run it.

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/your-username/m-bassy.git](https://github.com/your-username/m-bassy.git)
    ```
2.  **Open in Browser:**
    Simply open `index.html` in your favorite browser. 
    
    *Note: For the best experience with the History API, use a local server like Live Server (VS Code extension) or `npx serve`.*

## 🌐 Deployment on Netlify

To ensure clean URLs (e.g., `/note/123`) work correctly after a page refresh on Netlify, create a `netlify.toml` file in your public directory:

```toml
[[redirects]]
  from = "/*"
  to = "/index.html"
  status = 200
```

## 📡 Sharing Protocol

MBassy includes a built-in sharing protocol. When you click Share, the app:

    Compresses your note data (JSON) into a Base64 string.

    Generates a unique URL hash.

    When a recipient opens the link, MBassy detects the hash and offers to import the document into their local vault.

## 📜 License

Distributed under the MIT License. See LICENSE for more information.

Built by [https://github.com/rodezee](https://github.com/rodezee)
