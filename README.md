JMeter /all-student-name before optimized
![all-student-name.png](img%2Fall-student-name.png)
JMeter /highest-gpa before optimized
![highest-gpa.png](img%2Fhighest-gpa.png)
/all-student-name via command line
![stdnamejtl.png](img%2Fstdnamejtl.png)
/highest-gpa via command line
![gpajtl.png](img%2Fgpajtl.png)
/all-student optimized
![testplan1.png](img%2Ftestplan1.png)
/all-student-name optimized
![tesplan2.png](img%2Ftesplan2.png)
/highest-gpa refactored
![highest-gpa.png](img%2Fhighest-gpa.png)

Terdapat peningkatan performa yang signifikan pada *sample time* /all-student dan /all-student-name.
Untuk highest-gpa, menurut saya codenya sudah cukup optimized.

1. JMeter dapat menguji program dengan skenario *load* yang berbeda-beda, sehingga kita dapat mengetahui kemampuan program dalam mengatasi *load* tertentu . Di sisi lain, profiler menguji performa dari program hingga ke methodnya, sehingga kita dapat mengidentifikasi *code-code* yang perlu optimisasi.
2. Profiler memberikan informasi CPU time, Total time, hingga memory allocations dari setiap method yang dijalankan. Oleh karena itu, kita dapat mengidentifikasi dan mengoptimasi method-method yang memakan banyak resources atau CPU time.
3. Intellij Profiler menyediakan informasi-informasi yang membantu analisis dan identifikasi *bottlenecks* pada program. Contohnya, kita dapat melihat CPU Time, total time, dan memory allocations untuk method-method yang dijalankan. Data juga dapat disajikan secara visual menggunakan *flame graph*.
4. Profiler memberikan data yang cukup banyak, sehingga terkadang sulit untuk mengidentifikasi bagian-bagian yang menjadi *bottleneck* pada program. Pada tutorial ini, pengujian dilakukan untuk fungsionalitas satu fitur, sehingga saya dapat mengidentifikasi berdasarkan method-method yang dijalankan pada fitur tersebut.
5. Profiler Intellij memliki antarmuka dan visualisasi yang baik. Salah satu contohnya adalah terdapat keterangan cpu time pada source code di sebelah method yang dijalankan.
6. Performance test JMeter dan Profiler memiliki *scope* yang berbeda. Ada kemungkinan code yang dibuat sudah optimized setelah profiling tetapi saat performance test berjalan lebih lambat untuk load tertentu. Salah satu strategi untuk mengatasinya adalah dengan melakukan testing iteratif. Jika pada performance test JMeter menunjukkan response yang lambat pada skenario tertentu, maka kita dapat memfokuskan sesi profiling pada area tersebut.
7. Setelah menganalisis hasil performance testing dan profiling, tahap selanjutnya adalah mengimplementasikan algoritma yang lebih efisien. Untuk memastikan fungsionalitas aplikasi tetap terjaga, kita dapat mengimplementasikan functional test yang dapat dijalankan setelah melakukan perubahan pada code.
