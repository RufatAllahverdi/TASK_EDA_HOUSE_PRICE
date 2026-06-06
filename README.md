\# TASK\_EDA\_house\_price



Bu layihə Bakı şəhərində mənzil elanları datası üzərində aparılmış \*\*Exploratory Data Analysis (EDA)\*\* layihəsidir.  

Layihənin əsas məqsədi mənzil qiymətlərinə təsir edə biləcək faktorları araşdırmaq, məlumatları təmizləmək, statistik analiz aparmaq və nəticələri vizual şəkildə təqdim etməkdir.



\## Layihənin məqsədi



Bu EDA layihəsində mənzil qiymətləri ilə bağlı əsas dəyişənlər analiz edilmişdir:



\- Mənzilin ümumi qiyməti

\- Sahə ölçüsü

\- Otaq sayı

\- Bina növü

\- Təmir vəziyyəti

\- Çıxarışın olub-olmaması

\- İpoteka məlumatı

\- Mərtəbə məlumatları



Layihə real estate / house pricing datası üzərində ilkin data analizi aparmaq üçün hazırlanmışdır.



\## İstifadə olunan texnologiyalar



\- Python

\- Pandas

\- NumPy

\- Matplotlib

\- Seaborn

\- Jupyter Notebook



\## Dataset haqqında



Dataset mənzil elanları ilə bağlı məlumatlardan ibarətdir.



Əsas sütunlar:



\- `category`

\- `price`

\- `currency`

\- `price\_1m2`

\- `title`

\- `address`

\- `area`

\- `title\_deed`

\- `repair`

\- `mortgage`

\- `url`

\- `room\_number`

\- `current\_floor`

\- `total\_floor`



\## Görülən işlər



\### 1. Data Cleaning \& Preprocessing



Bu mərhələdə dataset analiz üçün uyğun formata gətirilmişdir.



Görülən əsas işlər:



\- `price` sütunundan `AZN`, boşluq və digər simvollar təmizləndi

\- `price\_1m2` sütunundan `AZN/m²` ifadəsi silindi

\- `area` sütunundan `m²` simvolu təmizləndi

\- `floor` sütunu iki ayrı sütuna bölündü:

&#x20; - `current\_floor`

&#x20; - `total\_floor`

\- Sütunların data tipləri uyğun formata çevrildi

\- Boş dəyərlər analiz edildi

\- `mortgage`, `repair` və digər sütunlardakı missing value-lar araşdırıldı



\### 2. Descriptive Statistics



Dataset üzərində əsas statistik göstəricilər hesablanmışdır.



Analiz olunan göstəricilər:



\- Mean

\- Median

\- Mode

\- Standard deviation

\- Variance

\- IQR

\- Frequency

\- Relative frequency

\- Pearson correlation



\### 3. Grouped Analysis



Kateqoriyaya görə mənzillər müqayisə edilmişdir:



\- Köhnə tikili

\- Yeni tikili



Müqayisə olunan göstəricilər:



\- Ortalama sahə

\- Otaq sayının medianı

\- Təmir və çıxarış məlumatlarının sayı və faizi



Analiz nəticəsində yeni tikililərin sahə baxımından daha böyük olduğu, lakin otaq sayının median olaraq oxşar qaldığı müşahidə edilmişdir.



\### 4. Outlier Analysis



`price` sütunu üzrə kənar dəyərlər araşdırılmışdır.



İstifadə olunan metodlar:



\- IQR metodu

\- Z-score yanaşması



Bu analiz vasitəsilə statistik baxımdan normal paylanmadan kənarda qalan mənzillər müəyyən edilmişdir.



\### 5. Correlation Analysis



Aşağıdakı dəyişənlər arasındakı əlaqələr analiz edilmişdir:



\- `price`

\- `area`

\- `room\_number`

\- `price\_1m2`

\- `current\_floor`

\- `total\_floor`



Pearson correlation coefficient vasitəsilə dəyişənlər arasındakı xətti əlaqə araşdırılmışdır.



\## Visualization



Layihədə Seaborn və Matplotlib kitabxanaları ilə vizuallaşdırmalar hazırlanmışdır.



Hazırlanan qrafiklər:



\- Price distribution histogram

\- KDE plot

\- Boxplot

\- Scatter plot

\- Heatmap

\- Barplot

\- Pairplot

\- Violinplot



Bu qrafiklər vasitəsilə qiymətlərin paylanması, outlier-lər, dəyişənlər arasındakı əlaqələr və kateqoriyalar üzrə fərqlər daha aydın şəkildə göstərilmişdir.



\## Əsas nəticələr



\- Dataset-də bəzi sütunlarda missing value-lar mövcuddur

\- `mortgage` sütununda çox sayda boş dəyər var və bu, çox güman ki, ipoteka məlumatının qeyd edilməməsi ilə bağlıdır

\- Yeni tikililərdə ortalama sahə köhnə tikililərə nisbətən daha yüksəkdir

\- Otaq sayının medianı bina növünə görə ciddi fərqlənmir

\- Qiymət dəyişəni sağa meylli paylanmaya malikdir

\- Sahə artdıqca ümumi qiymətin də artması müşahidə olunur

\- Bəzi mənzillər qiymət baxımından outlier hesab olunur



\## Project Structure



```text

TASK\_EDA\_house\_price/

│

├── TASK\_EDA\_house\_pricings.ipynb

├── README.md

└── data/

