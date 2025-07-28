# SympAI

SympAI is a Flask-based web application that helps users with:

- 🩺 Disease prediction  
- 🥗 Diet suggestions  
- 💊 Quick relief tips  
- 🏥 Finding nearby healthcare facilities  
- 🔐 User authentication and profile management  

---

## 🚀 Features

- **Disease Prediction:** Predict potential illnesses based on symptoms  
- **Diet Suggestions:** Smart dietary recommendations  
- **Quick Relief Tips:** Common remedies for quick relief  
- **Nearby Hospitals:** Find clinics/hospitals near your location  
- **User Auth:** Secure login, signup, and profile  
- **History (Coming Soon):** Track past queries  

---

## 🛠 Installation

### 1. Clone the repository:
```bash
git clone https://github.com/Sireesha-Budideti/sympai-2.git
cd sympai-2
```

### 2. Create a virtual environment and activate it:
```bash
python -m venv venv
venv\Scripts\activate   # On Windows
# OR
source venv/bin/activate  # On macOS/Linux
```

### 3. Install dependencies:
```bash
pip install -r requirements.txt
```

### 4. Set up the database:
```bash
flask db init
flask db migrate
flask db upgrade
```

### 5. Run the application:
```bash
python app.py
```

Then open your browser and visit:  
🌐 [http://127.0.0.1:5002](http://127.0.0.1:5002)

---

## 📡 API Endpoints

### 🔓 Public Endpoints
- `/` – Home page  
- `/diet-suggestion` – Get diet suggestions  
- `/quick-relief` – Quick remedies  
- `/care-near-you` – Find hospitals near you  

### 🔐 Authenticated Endpoints
- `/profile` – Manage your user profile  
- `/history` – View your past queries (under development)

### 🔁 POST Routes
- `/disease-prediction` – Accepts symptom input for diagnosis  
- `/get_hospitals` – Accepts `lat` and `lon` to return nearby hospitals

---

## 🗂 Project Structure

```
sympai/
├── app.py                  # Main Flask app
├── models.py               # Database models
├── forms.py                # Forms using Flask-WTF
├── prediction.py           # Disease prediction logic
├── requirements.txt        # Python dependencies
├── disease_health_tips.csv
├── Training_No_STDs.csv
│
├── templates/              # HTML templates
│   ├── base.html
│   ├── index.html
│   ├── login.html
│   ├── register.html
│   ├── profile.html
│   ├── prediction.html
│   ├── diet-suggestion.html
│   ├── quick_relief.html
│   ├── care_near_you.html
│
├── static/
│   ├── css/
│   │   ├── style.css
│   │   ├── care_near_you.css
│   │   ├── Diet.css
│   │   ├── prediction.css
│   │   ├── quick_relief.css
│   ├── js/
│   │   ├── script.js
│   │   ├── Dieat.js
│   │   ├── quick_relif.js
│   ├── images/
│       ├── bar_chart.png
│       ├── pie_chart.png
│       ├── oats.jpg
```

---

## ⚙ Configuration

- **SECRET_KEY**: Set your own secret key in `app.py` for security.
- **Database**: Change `SQLALCHEMY_DATABASE_URI` in `app.py` if you want to use a production DB.

---

## 🙋‍♀️ Maintainer

- [Sireesha Budideti](https://github.com/Sireesha-Budideti)

---

## 📄 License

This project is licensed under the [MIT License](LICENSE).
