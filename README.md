# Gradient Text Reader for Google Docs

Gradient Text Reader is a Google Docs add-on that applies smooth, eye-guiding gradients to text.  
Gradient Text Reader reduces eye strain, makes long passages easier to follow, and helps readers avoid skipping lines.

---

## ✨ Features
- **Smooth Flow Mode** – character-by-character gradient for continuous reading flow  
- **Striped Bands Mode** – word-by-word gradient bands (optional)  
- **Theme Presets** – Ocean, Slate, Classic, or custom colors  
- **Live Preview** – instantly see how your settings affect sample text  
- **Options**  
  - Restart gradient at each paragraph  
  - Skip already-colored text (links, annotations)  
  - Record original non-black colors for Restore  
- **One-Click Reset** – return text to black or restore original colors (if recorded)

---

## 🛠 Installation (Development / Testing)

1. Open [Google Apps Script](https://script.google.com/) and create a new **standalone project**.
2. Add two files:
   - `Code.gs` → paste the full server-side code
   - `Sidebar.html` → paste the UI code
3. In **Code.gs**, ensure you have:
   ```javascript
   function onOpen() {
     DocumentApp.getUi()
       .createMenu('Color Glide')
       .addItem('Open panel', 'showSidebar')
       .addToUi();
   }

   function onInstall(e) { onOpen(e); }
