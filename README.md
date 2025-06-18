
# 🧠 Smart ROCF Scoring System

> An AI-powered full-stack web application for **automated cognitive assessment** using the Rey–Osterrieth Complex Figure (ROCF) test.

## 📌 Project Overview

The **Smart ROCF Scoring System** is designed to objectively and automatically evaluate user-drawn figures against a reference ROCF image using advanced computer vision techniques. This project was developed as part of our **Machine Learning and Data Mining** semester course.

Manual ROCF scoring is **subjective**, **time-consuming**, and requires **clinical expertise**. Our system eliminates these challenges with an intuitive frontend and intelligent backend for consistent, real-time scoring.

---

## 🚀 Live Features

- ✅ Upload a reference ROCF image
- ✅ Upload user-drawn sketches (sessions 1, 2, 3)
- ✅ Draw directly using your device (touchscreen or mouse) via an interactive canvas
- ✅ Automatically compute visual similarity scores using 5 advanced techniques
- ✅ View session-wise score breakdown in a clean UI
- ✅ Fully responsive frontend for desktop and tablet devices


---

## 🧠 Scoring Techniques Used

The backend calculates a final score using a **weighted average** of the following techniques:

| Metric                  | Description                                                                 |
|------------------------|-----------------------------------------------------------------------------|
| `cv2.matchShapes`      | Shape matching using contour descriptors                                    |
| `SSIM`                 | Structural similarity between binary masks                                  |
| `ORB Feature Matching` | Keypoint-based matching using ORB features                                  |
| `Hu Moments`           | Affine-invariant moment comparison                                          |
| `Area Similarity`      | Normalized difference in filled contour areas                               |

Each session's result includes individual metric scores and a computed final score (in percentage).

---

## 🛠️ Tech Stack

### 🔹 Frontend
- React.js
- Axios (HTTP client)
- React Router


### 🔹 Backend
- Flask (Python API)
- OpenCV, NumPy
- skimage.metrics (for SSIM)
- CORS support for frontend integration

---

## 🔧 Project Structure

```

Smart-ROCF-Scoring-System/
│
├── frontend/                   # React.js frontend
│   ├── src/
│   │   ├── pages/
│   │   ├── components/
│   │   └── App.js
│   └── public/
│
├── backend/                    # Flask backend
│   ├── app.py                  # API routes and logic
│   ├── scoring.py              # Image processing & scoring
│   ├── utils.py                # Preprocessing helpers
│   └── uploads/                # Stores uploaded images
│
└── README.md                   # This file

````

---

## 📦 Installation & Setup

### ✅ Prerequisites
- Python 3.9+
- Node.js 14+
- pip (Python package manager)
- Git

### 🔹 Backend (Flask API)

```bash
cd backend
pip install -r requirements.txt
python app.py
````

> Make sure the server is running on `http://localhost:5000`

### 🔹 Frontend (React)

```bash
cd frontend
npm install
npm start
```

> App will be accessible at `http://localhost:3000`

---


## 📚 Future Improvements

* 🧾 Add user authentication and database integration
* 🤖 Integrate ML models or deep learning for adaptive scoring
* 📊 Dashboard for clinicians with analytics and export options

---

## 📎 License

This project is open-source under the MIT License.

---

## 🔗 GitHub Repository

🔗 [https://github.com/Omer-443/RCOF-Automation/](https://github.com/omerfaisal/RCOF-Automation)

---

## 🙌 Acknowledgements

This project was completed as part of the **Computer Vision** course under our academic program. Special thanks to our instructors and peers for their valuable feedback and support!

---

## 📣 Feedback & Contributions

Pull requests, suggestions, and issues are welcome!
If you'd like to contribute or use this in research, feel free to reach out.


