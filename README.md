# TASK3 "Water Quality & Potability Prediction: End-to-End Data Science Project"
Ushbu loyihada suv tarkibidagi 9 ta fizik-kimyoviy ko'rsatkich asosida suvning ichishga yaroqliligini bashorat qiluvchi Machine Learning modeli ishlab chiqilgan. 

Loyiha **Data Cleaning**, **Exploratory Data Analysis (EDA)** va **Predictive Modeling** bosqichlarini to'liq qamrab oladi.
##  Loyiha Maqsadi
Suv xavfsizligini laboratoriya tahlillarisiz, faqat kimyoviy ko'rsatkichlar orqali tezkor (real-time) aniqlash imkoniyatini yaratish.

##  Ishlatilgan Texnologiyalar
* Language: Python
* Libraries: Pandas, NumPy, Matplotlib, Seaborn
* ML Framework: Scikit-learn (Random Forest Classifier)
  
##  1. Data Cleaning (Option A)
Ma'lumotlar to'plami dastlab "iflos" holatda edi. Quyidagi ishlar amalga oshirildi:
* Missing Values:** `ph` (491), `Sulfate` (781) va `Trihalomethanes` (162) ustunlaridagi bo'shliqlar o'rtacha qiymat (`mean`) bilan to'ldirildi.
* Feature Selection:** Barcha 9 ta xususiyat model uchun muhim deb topildi.
  
##  2. Exploratory Data Analysis (Option B)
EDA jarayonida quyidagi asosiy xulosalar olindi:
* **Class Imbalance:** Datasetda yaroqsiz suvlar (61%) yaroqli suvlarga (39%) qaraganda ko'proq.
* **Correlation:** Xususiyatlar o'rtasida chiziqli bog'liqlik yo'q (Heatmap tahlili). Bu murakkabroq (non-linear) ML algoritmlarini qo'llash kerakligini ko'rsatdi.
##  3. Machine Learning Project (Option C)
Biz suvni klassifikatsiya qilish uchun **Random Forest Classifier** algoritmini tanladik.

### Model Natijalari:
* **Umumiy Aniqlik (Accuracy):** `67.84%`
* **Yaroqsiz suvni aniqlash (Recall for Class 0):** `86%` — Model xavfli suvni topishda juda samarali.
* **Yaroqli suvni aniqlash (Recall for Class 1):** `38%` — Bu modelning rivojlanish nuqtasi.

### Eng Muhim Faktorlar (Feature Importance):
Model qaror qabul qilishda quyidagi ko'rsatkichlarga eng ko'p tayanadi:
1. **Sulfate**
2. **ph**
3. **Hardness**

## 💡 Xulosalar va Kelajakdagi Rejalar
* **Xulosa:** Model suvning yaroqsizligini aniqlashda juda yaxshi natija ko'rsatdi. Bu inson salomatligi uchun muhim, chunki xavfli suvni "xavfsiz" deb yubormaslik ustuvor vazifadir.
* **Keyingi qadamlar:** Model aniqligini oshirish uchun *Hyperparameter Tuning* (GridSearchCV) o'tkazish va ko'proq ma'lumot to'plash.
