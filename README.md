# Patient-Readmission-Risk-Prediction-with-Explainable-AI-XAI-
Predicting hospital readmission risk for diabetic patients using XGBoost, with model interpretability via SHAP and LIME.
Bu layihə, şəkərli diabetdən əziyyət çəkən xəstələrin xəstəxanadan çıxdıqdan sonra 30 gün ərzində geri qayıtma (readmission) riskini proqnozlaşdırmaq üçün hazırlanmışdır. Layihədə modelin qərarlarını şəffaf etmək üçün SHAP və LIME metodlarından istifadə olunub.
 # Layihənin Məqsədi
Xəstəxana resurslarını daha düzgün bölmək və yüksək riskli xəstələrə qabaqcadan müdaxilə etmək üçün XGBoost alqoritmi ilə proqnozlaşdırma modeli qurmaq.
# Texnologiyalar
Dil: Python
Model: XGBoost (Extreme Gradient Boosting)
İzahlı AI (XAI): SHAP, LIME
Data Processing: Pandas, NumPy
Vizualizasiya: Matplotlib, Seaborn
# Məlumat Dəsti (Dataset)
Layihədə 100,000-dən çox xəstə qeydini özündə birləşdirən "Diabetes 130-US hospitals" datası istifadə olunub.
Xüsusiyyətlər: Yaş, diaqnoz kodları (ICD-9), dərman dozaları, xəstəxanada qalma müddəti və keçmiş yatış sayı.
# Model Nəticələri
Modelin performansı yalnız dəqiqlik (Accuracy) deyil, həm də həssaslıq (Recall) üzərində balanslaşdırılıb:
Balanslı Recall (Class 1): ~0.59 (Yüksək riskli xəstələrin 60%-i uğurla aşkar edilir).
Metod: scale_pos_weight istifadə edilərək sinif bərabərsizliyi aradan qaldırılıb.
#  Modelin İzahı (Interpretability)
Layihədə "Qara qutu" (Black box) modellərin izahı üçün iki əsas metod tətbiq olunub:
SHAP (Global Explanation): Bütün data üzrə ən vacib faktorun number_inpatient (keçmiş yatış sayı) olduğu müəyyən edildi.
LIME (Local Explanation): Hər bir xəstə üçün fərdi risk faktorları (məsələn, konkret yaş və ya dərman təsiri) vizuallaşdırıldı.
