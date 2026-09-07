This document serves regarding my App technical document

Project Folder: /home/malik/Work/Parapay
If there are any ambiguous statement do extra check on the project folder.

Parapay (FATL's) is an application to collect and manage payment of invoices for company's Account Receivable (AR) with the following features:
create a collection of invoices that will be billed to customer by FAR (collector)
manage multi-payment of the collection and residual
collect and deposit customer's payment
revise and edit payment in a collection

Parapay terintegrasi dengan SAP untuk mengambil invoice dan memasukkannya ke Parapay untuk diselesaikan dan kemudian akan dikembalikan lagi ke dalam SAP sebagai kontrol utama dari Invoice. 

SAP (System Applications and Products in Data Processing) adalah platform ERP (Enterprise Resource Planning) yang digunakan untuk mengelola berbagai proses bisnis di perusahaan.

Struktur receivable
Terdapat beberapa plan yang mengelola receivable antara Paranova atau Parama
1. PT Paranova Global Optima (Paranova)Fokus Utama: Perusahaan yang berfokus pada produk-produk health and wellness (kesehatan dan kebugaran) secara holistik. [1] (https://www.dompetdhuafa.org/dompet-dhuafa-salurkan-mushaf-al-quran-di-5-lokasi/)Brand yang Dinaungi: Menaungi brand bernama Beyondly, yang memproduksi produk perawatan kulit (skincare), nutrisi, dan minyak esensial (essential oil) yang tersertifikasi halal. [1] (https://id.wikipedia.org/wiki/Beyondly)Model Bisnis: Selain menjual produk, Paranova melalui Beyondly juga fokus menciptakan peluang usaha mandiri (penghasilan tambahan) bagi perempuan lewat program reseller atau penjualan langsung. [1] (https://chanelmuslim.com/info/beyondly-ciptakan-peluang-usaha-bagi-perempuan-untuk-tingkatkan-kemampuan-finansial-di-tengah-iklim-ekonomi-yang-menantang), [2] (https://money.kompas.com/read/2022/12/20/212000826/cara-mendapatkan-tambahan-penghasilan-lewat-beyondly)2. PT Parama Global Inspira (Parama)Fokus Utama: Bergerak di bidang logistik dan distribusi (distribution armlength).Peran Operasional: Menjadi distributor tunggal dan pihak yang bertanggung jawab menyalurkan produk-produk manufaktur milik PT Paragon Technology and Innovation (seperti Wardah) ke berbagai toko, ritel, dan pusat distribusi di seluruh wilayah Indonesia dan Malaysia.Keahlian: Manajemen gudang (warehouse), rantai pasok (supply chain), manajemen pengiriman, dan pemenuhan pesanan (e-commerce enabler). [1] (https://id.linkedin.com/company/pt-parama-global-inspira), [2] (https://glints.com/id/opportunities/jobs/mt-parama/fbf98b77-2278-4bf2-a465-63292d6a8aa6), [3] (https://www.instagram.com/p/CedKFfhhKXa/), [4] (https://kfmap.asia/warehouse/pt-parama-global-inspira-dc-bali-24921), [5] (https://www.youtube.com/watch?v=9F9Kp-lUsk4&t=19)

Setiap plant memiliki daerahnya masing masing, misalnya terdapat Bogor, Kendari, Ambon, dsb. 

Setiap plant memiliki beberapa role, Admin AR (mengurus sisi Invoice), FAR (mengurus penagihan piutang pada lapangan), nanti cek lagi buat nambah

Setiap plant memiliki beberapa area dan data customer di tiap plant akan dimapping ke satu area dan satu FAR. 

Setiap customer memiliki beberapa invoices yang dapat ditagih secara periodis. 

Setiap kali ingin melakukan penagihan, dari sisi Admin AR harus membuat sebuah collection. Collection merupakan kumpulan invoices dari satu atau lebih customer yang akan ditagih dalam satu kali jalan.

Setelah collection dikirimkan dari Admin AR, FAR dapat mengecek list invoicenya dan dapat menolak atau menerima Collection tersebut. Jika menolak maka dari Admin AR dapat menghapus collection atau menyesuaikan invoicenya. 
Jika menerima maka FAR dapat menagihkan invoices yang ada dalam collection tersebut. 

Dalam menu collection FAR dapat membuat Gagal Tagih per Customer dengan alasan tertentu sehingga dapat menagih ulang lagi nanti. Jika FAR memulai menu penagihan maka dari FAR dapat memasukkan payment (Cash, Transfer, Giro, Potong Tagihan, Tukar Faktur, Retur). 

Setiap Payment dapat untuk satu atau lebih invoices dalam collection tersebut.

Invoice dapat teralokasi secara penuh, parsial, atau jika tidak memiliki alokasi dari payment manapun akan menjadi gagal tagih pada akhir payment.

Setelah payment selesai, FAR dapat mensubmit paymentnya, dan payment tersebut akan muncul di menu Admin AR. 
Admin AR dapat menolak paymentnya dan membuat FAR merevisi ulang paymentnya, kasus yang umum terjadi adalah nominal yang tidak sesuai ataupun tanggal pembayaran yang tidak sesuai. Jika sesuai maka FAR dapat menyetujui paymentnya dan dapat menambahkan debit/credit untuk payment jika terdapat kekurangan atau kelebihan sedikit dari payment.
