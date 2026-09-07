This document serves regarding my struggle in the Parapay project.

Ketika memasuki tim terdapat kesulitan untuk keep up dengan kondisi pengembangan yang sekarang karena posisinya sudah 3/4 pengembangan sebelum tahap release/operasional dan terdapat minim dokumentasi mengenai aplikasi Parapay sendiri. 

Selain itu karena ini merupakan aplikasi revamp, tidak terdapat juga dokumentasi dari aplikasi sebelumnya. Sehingga, fitur yang sudah ada sebelumnya tidak terdokumentasi dengan baik membuat detail teknis dan detail constraint business atau cara dari penagihannya dicek secara manual oleh tim. Juga misal terdapat sedikit misalignment maka tim akan mengecek aplikasi lama secara manual dan tidak merefer ke dokumentasi aplikasi lama (karena tidak ada).

Sehingga banyak sekali business constraint yang tidak diketahui dan harus dikonfirmasi by chat ke Mentor. Sering kali constraint dari business yang diaplikasikan ke pengembangan tidak konsisten, sehingga habis cukup banyak waktu untuk berdiskusi dengan tim untuk menentukan bagaimana cosntraintnya akan ditangani.

Selain itu terdapat kendala juga, misal terdapat developer yang tidak masuk ke meet tersebut, sehingga nanti harus diadakan follow up hasil persetujuan by chat or by meeting dan tak jarang developer tersebut memiliki opini lain yang membuat pengembangan berubah arah lagi.

Dalam pengembangan fitur revisi terdapat banyak kendala dalam fitur nya karena fitur revisi memiliki banyak sekali constraint dari sisi business dan technical yang harus dicover. Misalnya pengembangan fitur revisi harus mengakomodasi 7 jenis payment yang ada, dan selain itu terdapat juga berbagai kondisi yang mungkin seperti satu payment untuk satu customer, satu payment untuk multi customer, dan payment tersebut juga dapat memiliki kondisi lain lagi, seperti underpayment, overpayment. dan lainnya. Sehingga dalam pengembangannya memerlukan beberapa kali iterasi hingga dapat berjalan dengan benar.

Selain itu karena pengembangan FE dan BE nya terpisah maka terkadang keperluan perubahan dari sisi BE harus dikonfirmasi terlebih dahulu ke mentor dan menunggu hingga fix, dan fitur FE di revisi baru dapat jalan.

Dalam pengembangannya saya tidak menggunakan AI secara penuh dengan memanfaatkan skills dan live documentationnya, sehingga tak jarang ketika terdapat bug dalam pengerjaan fiturnya dan memasukkan prompt yang diperlukan, maka fitur yang sebelumnya sudah terbuat secara tidak sadar terhapus oleh AI.

Dalam pengembangan fitur revisi juga karena perlu beberapa step untuk dapat mencapai titik revisi, maka pengembangan dan pengetesan tiap scenarionya memerlukan waktu yang cukup lama.
