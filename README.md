# ocr-data

A multilingual OCR (Optical Character Recognition) dataset repository.

This dataset is specifically designed for **fine-grained word-level OCR tasks**, providing **precise word-level bounding box annotations** for each image.

Each word is annotated with **pixel-accurate localization**, enabling tasks such as text detection, text recognition, and end-to-end OCR.

This repository currently provides an **Arabic OCR dataset**. Datasets for **English, German, Italian, and Spanish** will be released soon.

![OCR Sample](sample/showpages.png)

---

## 📦 Available Datasets

The technical specifications of each dataset are listed in the table below.

| Language | Dataset Version | Public Download Link | Pages Count | Unique Words | Fonts Count | Full Dataset Link |
|----------|-----------------|----------------------|--------------|--------------|--------------|-------------------|
| Arabic   | v1.0            | [Gdrive](https://drive.google.com/file/d/1Si0wTQ9sDm5744f_gFWEo2cFNzYcgi9i/view?usp=drive_link)            | TBD          | TBD          | TBD          | To obtain this dataset, please contact us at: deepcolab01[at]gmail.com [not free]               |


---


## 📁 Dataset Structure

The dataset is organized into three main directories at the root level:

```
ocr-data/
├── images/
├── labels/
├── texts/
```

---

### 📷 images/

- Contains OCR images in **PNG** format.
- Each image has a corresponding **JSON annotation file** with the same base filename.
- The JSON file precisely defines the location of each word in the image.

### 🏷 labels/

- Contains **JSON annotation files** corresponding to the images.
- Each JSON file shares the same base filename as its related image.
- These files define **word-level annotations** with exact bounding box coordinates.
- The annotation structure is identical to the JSON format described in the `images/` section.

JSON Annotation Format (per image)

```python
import json
with open(path_image_label, 'r', encoding='utf-8') as f:
    data = json.load(f)
```

```json
{
  "0": {
    "word": "كلمة",
    "location": {
      "x": 3927,
      "y": 481,
      "w": 397,
      "h": 170
    }
  },
  "1": {
    "word": "عربية",
    "location": {
      "x": 3544,
      "y": 481,
      "w": 355,
      "h": 170
    }
  }
}
```

- `word`: The recognized word in the image.
- `location`: Bounding box of the word:
  - `x`, `y`: Top-left corner coordinates
  - `w`, `h`: Width and height of the bounding box

---


### 📝 texts/

- Contains **TXT** files.
- Each text file corresponds to an image.
- Stores the **continuous (full) text** related to the image content.


---

## 🚀 Roadmap

- [x] Arabic OCR Dataset
- [ ] English OCR Dataset
- [ ] German OCR Dataset
- [ ] Italian OCR Dataset
- [ ] Spanish OCR Dataset

---

## 📜 License

Please check the `LICENSE` file for usage terms and conditions.

---

## 🤝 Contributing

Contributions, issues, and feature requests are welcome. Feel free to open an issue or submit a pull request.

---

## 📬 Contact

For access requests or questions, please open an issue in this repository.

