# 📚 photographic_memory.py

> For when right-click + save as just ain’t an option.

**photographic_memory.py** is a screenshot-based automation tool designed to capture ebook or online science paper pages that can't be downloaded directly. It lets you define a page region, takes sequential screenshots while flipping pages, and then (optionally) compiles them into a PDF file.

---

## 🛠️ Features
- Set-it-and-forget-it screenshot capture for ebook pages
- Auto-presses the right arrow key to advance through pages
- Saves each page as an image to a `shots/` folder
- Converts all images into a single PDF (very slow but works)
- Great for archiving materials behind JS-based readers

---

## ⚙️ How It Works
1. You specify the number of pages (`page_count`).
2. You set the coordinates of the screen region to capture.
3. The script screenshots the defined area, presses the right arrow key, and repeats.
4. Once complete, it compiles all `.png` images into a `.pdf` using `img2pdf`.

> 💡 Tip: It's often faster to manually combine the output images into a PDF using Adobe or another tool than to wait for the script’s PDF export.

---

## 🧠 Requirements
```bash
pip install pyautogui img2pdf
```

---

## 📂 Folder Structure
```
project/
├── shots/           # Where screenshots are saved
├── pdfs/            # Output directory for final PDF
└── photographic_memory.py
```

---

## 🧪 Usage
1. **Adjust coordinates:** Update the `region = (x, y, width, height)` to match your screen setup.
2. **Set your page count:** Update the `page_count` variable.
3. **Run it:** You’ll have 5 seconds to switch to your ebook reader.

```bash
python photographic_memory.py
```

---

## ⚠️ Warnings
- Screenshots are saved with numeric names (`0.png`, `1.png`, ...)
- Image-to-PDF process can be **very** slow with thousands of images
- The script assumes full control of your keyboard during execution (presses `right` repeatedly)
- Use ethically and responsibly

---

## Inspired by
My brain, hustle, and the phrase: *"Fine, I’ll do it myself."*

---

## 🧠 License
MIT – because im not the villain here.

---

**Made with fingers, frustration, and caffeine.** ☕🖥️
