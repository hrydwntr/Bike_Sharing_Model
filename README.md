Business Problem Understanding
Context

Capital Bikeshare adalah sebuah sistem peminjaman sepeda yang terdapat di Amerika Serikat. Sistem peminjaman sepeda ini adalah generasi baru dari rental sepeda tradisional dimana seluruh proses keanggotaan, penyewaan, dan pengembalian telah diotomasi. Melalui sistem ini, pengguna mampu secara mudah menyewa sepeda dari satu lokasi tertentu dan mengembalikkannya di lokasi yang lain. Saat ini, terdapat sekitar lebih dari 500 program bike-sharing di seluruh dunia dengan lebih dari 500.000 sepeda. Capital Bikeshare sendiri memiliki lebih dari 600 stasiun dan sekitar 5.000 sepeda Capital Bikeshare yang tersebar di wilayah Washington. Dewasa ini, minat terhadap sistem ini cukup besar dikarenakan peran penting terhadap isu lalu lintas, lingkungan, dan kesehatan.

Terlepas dari menariknya pengaplikasian sistem peminjaman sepeda di dunia nyata, karakteristik data yang dihasilkan oleh sistem ini membuat hal tersebut menarik untuk diteliti. Berbanding terbalik dengan sarana transport lain seperti bus atau subway, durasi perjalanan, posisi keberangkatan dan kedatangan terekam secara jelas di sistem ini. Fitur ini menjadikan sistem peminjaman sepeda menjadi sebuah virtual sensor network yang bisa digunakan untuk merasakan mobilitas di dalam kota. Oleh sebab itu, diharapkan banyak kejadian penting di dalam kota dapat dideteksi melalui pemantauan data ini.

Problem Statement

Salah satu dari banyak tantangan dalam sistem peminjaman ini ialah untuk menyediakan jumlah unit sepeda yang cukup di setiap kondisi dan situasi. Jika tidak, maka kita bisa gagal dalam memenuhi tuntutan dari pengguna sistem peminjaman sepeda tersebut dan bahkan bisa berujung kepada hilangnya kepercayaan pelanggan. Namun apabila jumlah ketersediaan sepeda terlalu banyak, hal itu bisa menyebabkan banyaknya unit sepeda yang tidak terpakai, dalam kata lain, tidak efisien. Dimana hal tersebut bisa berimbas kepada membengkaknya biaya manajemen, logistik, serta perawatan untuk tiap unit sepeda. Seperti yang dilansir Wikipedia, setiap satu unit sepeda berharga $1000 dan biaya operasi tahunan setiap sepedanya adalah $1860.

Goals

Berdasarkan permasalahan tersebut, Capital Bikeshare tentu perlu memiliki 'tool' yang baik guna memprediksi serta membantu tiap stakeholder yang terkait (baik klien maupun Capital Bikeshare itu sendiri) untuk dapat menentukan jumlah unit sepeda yang tersedia dengan tepat di setiap kondisi dan situasi. Adanya perbedaan situasi dan kondisi seperti cuaca, musim, kelembaban, suhu, dapat menambah keakuratan prediksi jumlah unit sepeda yang perlu disediakan. Dimana hal tersebut tidak hanya mendatangkan profit namun juga menjaga efisiensi operational cost dari sisi Capital Bikeshare dan jika dari sisi pengguna (klien) tentunya hal tersebut sangat membantu dalam memenuhi tuntutan kebutuhan pelanggan.

Analytic Approach

kita akan melakukan analisa terhadap data untuk dapat menemukan pola dari fitur-fitur yang ada, yang membedakan satu kondisi dengan yang lainnya, serta bagaimana tiap fitur tersebut mempengaruhi jumlah unit sepeda yang perlu tersedia. Selanjutnya, kita akan membangun suatu model regresi yang akan membantu dalam menentukan jumlah unit sepeda yang perlu disediakan oleh Capital Bikeshare, yang mana akan berguna untuk menjaga efisiensi operational cost.

Metric Evaluation

Evaluasi metrik yang akan digunakan adalah MAE, MAPE, dan R-squared. Dimana MAE adalah rataan nilai absolut dari error, sedangkan MAPE adalah rataan persentase error yang dihasilkan oleh model regresi. Semakin kecil nilai MAE dan MAPE yang dihasilkan, berarti model semakin akurat dalam memprediksi jumlah unit sepeda dengan limitasi fitur yang digunakan. Selain itu, kita juga akan menggunakan nilai R-squared jika model yang nanti terpilih sebagai final model adalah model linear. Nilai R-squared digunakan untuk mengetahui seberapa baik model dapat merepresentasikan varians keseluruhan data, seberapa besar pengaruh variabel independen terhadap variabel dependen. Semakin mendekati 1, maka semakin fit pula modelnya terhadap data observasi. Namun, metrik ini tidak valid untuk model non-linear.

Data Understanding
Dataset merupakan data peminjaman sepeda di sistem Capital Bikeshare dalam rentang tahun 2011-2012.
Setiap baris data merepresentasikan informasi terkait waktu peminjaman, cuaca, dan musim yang sesuai.
