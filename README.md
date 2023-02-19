# Bank Marketing Campaign 

**Context**

Jenis produk keuangan yang digunakan masyarakat lebih bervariasi. Salah satu produk keuangan yang cukup dikenal masyarakat adalah term deposit. Mekanisme term deposit adalah nasabah menyimpan sejumlah uang di bank atau lembaga keuangan, dan uang tersebut hanya dapat ditarik setelah jangka waktu tertentu. Sebagai kompensasinya, nasabah akan diberikan bunga tetap sesuai dengan nominal uang yang disetorkan.

Namun demikian, sebagai badan usaha dengan produk keuangan dan nasabahnya masing-masing, bank tetap harus bersaing agar tidak kehilangan nasabah. Salah satu cara untuk mendapatkan pelanggan baru adalah dengan melakukan kampanye pemasaran.

**Target**

0 : Tidak melakukan deposit

1 : Melakukan deposit


**Problem Statement**

Biaya pemasaran bisa lebih besar jika perusahaan menargetkan nasabah tanpa melakukan skrining terlebih dahulu. Perusahaan ingin meningkatkan efisiensi pemasaran produk keuangan deposito dengan mengetahui nasabah mana yang tertarik berinvestasi dengan pendekatan deposito.

Dan jika biaya admin deposito diberikan secara gratis kepada semua calon/nasabah, maka biaya tersebut akan menjadi sia-sia jika calon/nasabah yang mendaftar tersebut memiliki jangka waktu deposit yang rendah dan dapat merugikan bank tersebut.

**Goals**

Maka berdasarkan permasalahan tersebut, bank ingin memiliki kemampuan untuk memprediksi kemungkinan seorang nasabah akan/ingin melakukan deposit di bank atau tidak, sehingga dapat memfokuskan pemasaran pada nasabah yang ingin melakukan deposit di bank tersebut.

Dan juga, perusahaan ingin mengetahui apa/faktor/variabel apa yang membuat seorang nasabah melakukan deposit atau tidak, sehingga mereka dapat membuat rencana yang lebih baik dalam mendekati nasabah potensial (nasabah yang ingin memiliki produk keuangan deposito).

**Analytic Approach**

Hal yang dilakukan adalah menganalisis data untuk menemukan pola yang membedakan nasabah yang mau berinvestasi dengan produk deposito dan yang tidak tertarik dengan produk deposito.

Kemudian akan dibuat model klasifikasi yang akan membantu bank untuk dapat memprediksi probabilitas seorang nasabah akan/ingin melakukan deposito di bank tersebut atau tidak.

**Metric Evaluation**

Type 1 error : False Positive  
Konsekuensi: sia-sianya biaya marketing, waktu dan sumber daya

Type 2 error : False Negative  
Konsekuensi: kehilangan calon nasabah potensial 

Berdasarkan konsekuensinya, maka sebisa mungkin yang akan kita lakukan adalah membuat model yang dapat mengurangi biaya pemasaran dari bank tersebut, tetapi tanpa menyebabkan berkurangnya kandidat nasabah potensial yang dibutuhkan bank. Jadi, akan dilakukan prediksi kelas *true positive*, dengan seminim mungkin prediksi *false positive*. Metric utama yang akan digunakan adalah roc_auc.

**Features**

**Profil Nasabah :**
-	umur
-	pekerjaan
-	balance
-	rumah
-	pinjaman

**Marketing data :**
- kontak: Jenis komunikasi kontak.
- bulan: Bulan kontak terakhir dalam setahun.
- kampanye: Jumlah kontak yang dilakukan selama kampanye ini dan untuk klien ini.
- *pdays*: Jumlah hari setelah klien dihubungi dari kampanye sebelumnya.
- *poutcome*: Hasil dari kampanye pemasaran sebelumnya.
- deposit: Apakah nasabah melakukan deposit atau tidak.

### Data Information

Header | Definition
---|--------- 
`Age`| Age of customer |
`Job` | Job of customer |
`Housing` | If costumer has housing loan |
`Loan` | Has Personal Loan |
`Balance` |Customer's individual balance |
`Contact` | Communication type |
`Month` |  Last contact month of year | 
`Campaign` | Number of contacts performed during this campaign and for this client |
`Pdays` | Number of days that passed by after the client was last contacted from a previous campaign |
`Poutcome` |outcome of the previous marketing campaign |
`Deposit` | has the client subscribed a term deposit |

Correlation between numerical data:


Model Classification



Metrics Evaluation



Model based on the analytics




Conclusion

Berdasarkan hasil classification report dari model Gradient Booster, dapat diambil konklusi berdasarkan recallnya bahwa bila seandainya nanti kita menggunakan model kita untuk memfilter/menyaring nasabah yang akan ditawarkan layanan deposit, maka model kita dapat mengurangi 87% nasabah yang tidak berminat dengan layanan deposito untuk tidak kita approach, dan model kita dapat mendapatkan 66% nasabah yang tertarik dari seluruh nasabah yang tertarik dengan layanan deposito.


