# Airline-customer-value-analysis
Menggunakan Metode Unsuvervised Learning 
## Content
### Exploratory Data Analysis dan Preprocessing
* Berdasarkan missing values, dilakukan pengisian data pada feature AGE, SUM_YR_1, dan SUM_YR_2. Selain itu, dilakukan drop pada feature WORK_CITY, WORK_PROVINCE, * WORK_COUNTRY dan GENDER
* Dari hasil heatmap dan referensi ebook diketahui bahwa fitur penting berdasarkan sumber yang dibaca, dipilih menggunakan model LRFMC dimana fitur yang digunakan untuk model ini adalah: load_time, ffp_date, last_to_end, flight_count, seg_km_sum, avg_discount
* Fitur yang nilai korelasinya rendah dan dianggap tidak berhubungan dalam penyelesaian masalah akan di drop dari dataset: MEMBER_NO, AGE, GENDER, EXCHANGE_COUNT, SUM_YR_1, SUM_YR_2, POINT_NOTFLIGHT, AVG_INTERVAL, MAX_INTERVAL
* Pelanggan Loyal bisa dilihat dari pembagian flight count per tahun menjadi member
* Pelanggan lama bisa dilihat dari tanggal data diambil dikurang FFP join date
### Feature Engineering
Dari feature LAST_FLIGHT_DATE, FIRST_FLIGHT_DATE, dan FLIGHT COUNT, dilakukan perhitungan untuk menentukan rata-rata penerbangan per tahun dengan output pada feature Flight_Count/Year

* Dibuat feature Meeting_Time untuk menghitung jumlah bulan antara LOAD_TIME dan FPP_DATE
* Setelah feature engineering, drop feature yang tidak digunakan kembali, dan handling outlier, dilakukan standarisasi pada dataset sehingga data dapat siap untuk modelling

 ### Modeling
 Melakukan clustering menggunakan k-means dimana berdasarkan elbow method digunakan jumlah cluster yaitu sebanyak 4 cluster.
 
 ### Summary (Analysis Hasil Clustering)
Simpulkan secara singkat hasil pengerjaan teman-teman. Analysis karakteristik setiap cluster dan berikan insight Berdasarkan hasil pengerjaan, didapatkan beberapa kesimpulan sebagai berikut: a. Feature yang mempengaruhi dalam segmentasi pelanggan diantaranya yakni total jarak penerbangan, jarak waktu penerbangan terakhir ke pesanan penerbangan paling akhir, rata-rata diskon yang didapatkan pelanggan, durasi pelanggan menjadi member, dan rata-rata jumlah penerbangan per tahun.

  Berdasarkan cluster yang telah diidentifikasi (dapat dilihat di file) Adapun penjelasan terhadap ke-4 cluster yang terbentuk adalah sebagai berikut:
 Cluster 0 (middle value customer) ○ Member pada cluster 0 memiliki durasi 
membership selama 43 bulan yang memiliki 
jarak penerbangan sebesar 10.846 kilometer 
yang memiliki rata rata penerbangan diatas 8 
kali
● Cluster 1 (low value customer) ○ Member pada cluster 1 memiliki durasi 
membership selama 39 bulan yang memiliki 
jarak penerbangan sebesar 9.176 kilometer 
yang memiliki rata rata penerbangan diatas 6 
kali
● Cluster 2 (high value customer) ○ Member pada cluster 2 memiliki durasi 
membership selama 53 bulan yang memiliki 
jarak penerbangan sebesar 12.898 kilometer 
yang memiliki rata rata penerbangan diatas 9 
kal
