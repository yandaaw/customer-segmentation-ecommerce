# E-commerce Customer Segmentation
<p align="center">
  <img width="450" height="300" src="https://media.istockphoto.com/photos/marketing-segmentation-picture-id643956920?k=20&m=643956920&s=612x612&w=0&h=oJ2jfEW8Dp6XmT7PIwrcn4A0vCryKxf3T5C-QJjp1_Y=">
</p>

Ada berbagai macam penerapan unsupervised learning dalam industri diantaranya Customer segmentation. Dengan customer segmentation kita dapat mengetahui target atau cakupan dari produk barang atau jasa yang kita punya. Misalnya, suatu perusahaan telekomunikasi tertarik untuk mengelompokkan customer berdasarkan penggunaan SMS, dan internet. Perusahaan bisa saja menemukan pengelompokkan tertentu misalkan ada pelanggan yang sangat aktif dalam menggunakan internet tetapi jarang menggunakan SMS, ada juga yang jarang menggunakan internet tapi cukup sering menggunakan SMS atau bahkan ada yang aktif menggunakan keduanya. Dengan mengetahui informasi tersebut,  perusahaan dapat menentukan jenis produk yang paling sesuai untuk ditawarkan.

## **Overview**
Sebagai seorang data scientist di suatu e-commerce, penulis dimintai bantuan oleh tim marketing untuk membantu mereka dalam mengatur strategi pemasaran perusahaan. Mereka ingin mengetahui siapa pelanggan - pelanggan terbaik mereka, siapa yang berpotensial untuk menjadi pelanggan terbaik mereka dan siapa yang merupakan pelanggan-pelanggan yang kurang memberikan nilai kepada perusahaan.<br>

Salah satu cara yang bisa dilakukan untuk memahami pelanggan penulis adalah dengan melakukan segmentasi pelanggan. Segmentasi adalah proses pengelompokan pelanggan menjadi beberapa kelompok berdasarkan karakteristik mereka. Kita dapat menggunakan banyak variabel untuk membuat segmentasi pelanggan kita. Informasi seperti demografis pelanggan , geografis, psikografis, teknografis, dan perilaku sering digunakan sebagai pembeda untuk mensegmentasi pelanggan.<br>

Fokus pengerjaan project ini adalah melakukan segmentasi berdasarkan perilaku transaksi pelanggan. Hal ini menyesuaikan dengan dataset yang sudah di siapkan tim marketing yaitu data transaksi. Project ini akan menggunakan data Recency, Frequency dan Monetary yang sudah terbukti untuk merepresentasikan aktivitas transaksi pelanggan di berbagai industri.

## **Built With**
Project ini dibangun dengan menggunakan bahasa pemrograman Python dan sejumlah library python diantaranya:
- [pandas](https://pandas.pydata.org/)
- [numpy](https://numpy.org/)
- [seaborn](https://seaborn.pydata.org/)
- [matplotlib](https://matplotlib.org/)
- [Garbage Collector (gc)](https://docs.python.org/3/library/gc.html)
- [scikit-learn](https://scikit-learn.org/)
- [SciPy](https://scipy.org/)

## **Steps and Process**
Seperti telah dijelaskan sebelumnya pembuatan project ini berfokus pada melakukan segmentasi customer berdasarkan perilaku transaksi yang telah mereka lakukan. Kemudian untuk data analysis proses dan pembuatan model machine learning, penulis menggunakan 6-key steps sebagai panduan dalam pembuatan project ini. Yang mana proses-proses dibawah mengacu pada sifat iteratif dari proses pemecahan masalah berdasarkan alur kerangka kerja atau metodologi project data science seperti pada gambar dibawah.
1.  [Step 1](https://github.com/yandaaw/customer-segmentation-ecommerce/blob/main/cs1p_data_collection_wrangling.ipynb): Define problem statement / data requirements specification.
2.	[Step 2](https://github.com/yandaaw/customer-segmentation-ecommerce/blob/main/cs1p_data_collection_wrangling.ipynb): Data collection 
3.	[Step 3](https://github.com/yandaaw/customer-segmentation-ecommerce/blob/main/cs1p_data_collection_wrangling.ipynb): Data cleansing
4.	[Step 4](https://github.com/yandaaw/customer-segmentation-ecommerce/blob/main/cs1p_data_collection_wrangling.ipynb): Data preprocessing 
5.	[Step 5](https://github.com/yandaaw/customer-segmentation-ecommerce/blob/main/cs2p_exploratory_data_analysis.ipynb): Data analysis
6.	[Step 6](https://github.com/yandaaw/customer-segmentation-ecommerce/blob/main/cs3p_rfm_country_france.ipynb): Modeling, Evaluation, and Deployment 
7.	[Step 7](https://public.tableau.com/app/profile/sriyanda.afrida.wahyudi4721/viz/CustomerSegmentationDashboard_16520896677390/Dashboard1): Data communication (visualize and share the results)
![image](https://user-images.githubusercontent.com/73176284/161413233-cce4269a-bddb-4185-aa15-9eb88544d002.png)
<br>

## **Clustering**
Clustering merupakan suatu metode yang dapat digunakan untuk mendapatkan penggerombolan dalam data. Harapannya, data akan dikategorikan ke dalam sejumlah grup dimana data-data yang berada dalam grup yang sama memiliki kemiripan karakteristik. Sedangkan data memiliki grup berbeda akan sangat berbeda karakteristiknya. <br>

Metode clustering ada bermacam-macam. Metode yang akan digunakan pada project ini adalah K-Means. Dalam metode k-means kita memerlukan konsep jarak untuk mengetahui seberapa dekat suatu data poin dengan data poin lainnya. Salah satu konsep jarak yang dapat kita gunakan adalah jarak euclidean. Banyaknya cluster yang optimal dapat kita tentukan dengan metode elbow, silhouette atau bisa juga sudah ditentukan di awal berdasarkan domain knowledge.
![image](https://user-images.githubusercontent.com/73176284/167814538-914ec127-c316-4193-afc4-3fac51da65fe.png)
 
## **Conclusion EDA and Model**
<p align="center">
  <img width="450" height="300" src="https://user-images.githubusercontent.com/73176284/167811822-c68612f5-8c03-432c-bfad-a6f8b1e12162.png">
</p>

- Terdapat korelasi antara banyaknya Quantity dan Amount Spent dari suatu customer.
- United Kingdom, Germany, dan France merupakan negara dengan jumlah Customer terbanyak.
- Drusy Comer dari United Kindom merupakan Customer dengan jumlah pembelian terbanyak.
- Bulan November 2011 merupakan waktu dengan jumlah penjualan terbanyak.
- Hari kamis merupakan waktu dengan jumlah penjualan terbanyak.
- Jumbo bag adalah product dengan penjualan terbanyak.
- Negara France akan dipilih sebagai lokasi pemetaan untuk pembuatan rfm model - customer segmentation pada project ini karena pertimbangan banyaknya data dan point kesimpulan sebelumnya.   
- 70% Customer tersebar pada label Need Attention, kemudian 24% dari total Customer tersebar pada label Not Loyal, dan sisanya sebanyak 6% dari total Customer tersebar pada label Priority. 
- Kategory umur Generation X dan Millenials merupakan kategori umur dari Customer yang mendominasi sebaran label Need Attention dan Not Loyal. Sedangkan sebanyak 5% dari total seluruh presentase customer berlabel Priority berasal dari Generation x.
<br>

Untuk peninjauan hasil kesimpulan proses [**Exploratory Data Analysis**](https://github.com/yandaaw/customer-segmentation-ecommerce/blob/main/cs2p_exploratory_data_analysis.ipynb) dan pembuatan [**Model RFM**](https://github.com/yandaaw/customer-segmentation-ecommerce/blob/main/cs3p_rfm_country_france.ipynb) dapat dilihat pada setiap langkah-langkah pada bagian page **Steps and Process** diatas. Kemudian karakteristik hubungan label segmentasi dengan features data yang lain untuk setiap customer dapat dilihat pada [**dashboard**](https://public.tableau.com/app/profile/sriyanda.afrida.wahyudi4721/viz/CustomerSegmentationDashboard_16520896677390/Dashboard1) pada bagian page **Data Visualization** dibawah. 

## **Data Visualization**
Berikut merupakan visualisasi dalam bentuk dashboard untuk Customer Segmentation sebagai representasi proses data communication. [**Tableau**](https://public.tableau.com/en-us/s/) merupakan tools yang digunakan dalam pembuatan customer segmentation dashboard dibawah.
![image](https://user-images.githubusercontent.com/73176284/167811946-d777ed74-23c8-4b3a-b7ce-5277c2f07c9d.png)

Link dibawah merupakan beberapa dashboard yang telah dibuat dan berkaitan dengan project ini.
- [**Customer Profiling Dashboard**](https://public.tableau.com/app/profile/sriyanda.afrida.wahyudi4721/viz/CustomerProfilingDashboard_16520824416280/Dashboard1)
- [**Customer Segmentation Dashboard**](https://public.tableau.com/app/profile/sriyanda.afrida.wahyudi4721/viz/CustomerSegmentationDashboard_16520896677390/Dashboard1)
- [**Product Analysis Dashboard**](https://public.tableau.com/app/profile/sriyanda.afrida.wahyudi4721/viz/ProductAnalysisDashboard_16521079878290/Dashboard1)
