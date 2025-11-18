# EgoBlur Model Weights

This repository contains the **pre-trained EgoBlur model weights** in `.jit` format for:
- **Face anonymization**  
- **License plate anonymization**

These weights are intended to be used for **privacy-preserving blurred output** in videos or images.  
The models do **not identify people**, they only detect regions that must be anonymized.

---

## 📌 Models Included

```

egoblur_face/        → Face blur model (egoblur_face.jit)
egoblur_lp/          → License plate blur model (egoblur_lp.jit)

````

Both files are stored using **Git LFS** because they are larger than 100MB.

---

## 🚀 How to Use (Python Example)

```python
import os
import urllib.request

def download_if_missing(filepath, url):
    if not os.path.exists(filepath):
        print(f"Downloading {filepath}...")
        urllib.request.urlretrieve(url, filepath)

# Paths where your app will store weights
face_path = "weights/egoblur_face.jit"
lp_path   = "weights/egoblur_lp.jit"

# Download links (Raw GitHub URLs)
download_if_missing(
    face_path,
    "https://raw.githubusercontent.com/ganeshmohane-aisolo/egoblur-model-weights/main/egoblur_face/egoblur_face.jit"
)

download_if_missing(
    lp_path,
    "https://raw.githubusercontent.com/ganeshmohane-aisolo/egoblur-model-weights/main/egoblur_lp/egoblur_lp.jit"
)
````

Now you can load the `.jit` model in your application.

---

## 🔐 Privacy & Policy Compliance

These models are used **only for anonymization** (blurring sensitive regions).

✔ The models **do not identify** a person
✔ They **do not extract personal attributes**
✔ They **only detect bounding boxes** for faces and license plates
✔ Purpose: **Privacy protection**, compliant with standard anonymization practices

These weights should be used only for **privacy-preserving processing**, not surveillance or identification.

---

## 🔗 Reference: Meta Project Aria

EgoBlur anonymization originates from **Project Aria** by Meta Reality Labs.
For technical details:
[https://projectaria.com](https://projectaria.com)

This repository only provides **weights** for anonymization models — no copyrighted code from Project Aria is included.

---

## 📄 License

These weights are provided for **research and privacy-preserving applications**.
Check Project Aria's licensing terms if using their datasets or code.


## 📬 Contact

For issues or questions, open a GitHub Issue in this repository.

```
