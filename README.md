# hr-employees

Employee Job Change Prediction

Bu layihədə işçilərin işlərini dəyişmək istəyib-istəmədiyini proqnozlaşdırmaq üçün verilənlər üzərində analiz və preprocessing mərhələləri həyata keçirilmişdir.

📁 Dataset Haqqında

Dataset işçilər haqqında müxtəlif məlumatları ehtiva edir:

Şəhər
Cins (gender)
Təhsil səviyyəsi və ixtisas
İş təcrübəsi (experience)
Şirkət tipi və ölçüsü (company_type, company_size)
Təlim saatları (training_hours)
Son iş dəyişmə məlumatı (last_new_job)

🎯 Target sütunu:

1 → İşini dəyişmək istəyir
0 → Hazırkı işində qalmaq istəyir
🔍 Data Analizi (EDA)

Aşağıdakı ilkin analizlər aparılmışdır:

Dataset strukturu (info, describe)
Null dəyərlərin yoxlanması
Data tiplərinin analizi
Kategorik və numeric sütunların ayrılması
Vizual analizlər (histogram, boxplot)
🧹 Data Preprocessing
1. Lazımsız sütunların silinməsi
enrollee_id, city sütunları çıxarıldı
2. Null dəyərlərin idarə olunması
Bəzi kategorik sütunlarda (gender, company_type, major_discipline) null dəyərlər "Unknown" ilə əvəz edildi
Numeric sütunlar uyğun metodlarla dolduruldu
3. Data tiplərinin düzəldilməsi
experience, last_new_job kimi sütunlarda olan >20, >4 kimi dəyərlər numerik formata çevrildi
4. Feature Engineering
company_size üçün xüsusi konvertasiya funksiyası tətbiq olundu
5. Encoding
Kategorik dəyişənlər pd.get_dummies() ilə one-hot encoding edildi
📈 Vizualizasiya
training_hours üçün histogram və boxplot
Outlier analizləri
Target ilə əlaqəli müqayisələr

Qeyd: Bəzi outlier-lər saxlanılmışdır ki, məlumat itkisi olmasın.

🤖 Model üçün Hazırlıq
Dataset X və y olaraq bölündü
train_test_split ilə train və test datasetlər yaradıldı
🛠️ İstifadə olunan texnologiyalar
Python 🐍
Pandas
NumPy
Seaborn
