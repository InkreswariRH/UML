## Introduction
- Sequence diagram menunjukkan bagaimana objek dari sistem atau class-class dalam source code berinteraksi antara satu dengan yang lain.

- Sequence diagram menunjukkan urutan aktivitas / kejadian.

- Sequence menunjukkan interaksi berdasarkan posisi-posisi objek / class (urutan posisi objek / class).

- Sequence diagram digunakan oleh para developer dan stakeholders untuk mengerti dan mendokumentasikan alur dari sistem yang sedang dibangun. Sequence juga dapat membantu mereka memahami requirement apa saja yang dibutuhkan oleh sistem.

## Poin-Poin Utama / Elemen Sequence

- Sequence diagram terdiri dari beberapa elemen utama:
   - Actor
   - Object
   - Message
   - Alternative frame
   - Activation box
   - Lifeline

- Dalam sequence, jika yang mau kita gambarkan adalah sistem, maka objek-objek dalam sequence adalah semua bagian-bagian dari sistem tersebut.

- Jika yang mau digambarkan dalam sequence adalah source code, maka objek-objek yang ada adalah class-class dalam source code tersebut.

![simbol dari poin-poin utama sequence](https://github.com/InkreswariRH/UML/blob/main/Sequence/assets/images/simbol_sequence.jpg)


**1. Aktor**
 
Aktor letaknya ada di sebelah kiri. Aktor adalah pihak yang ada di luar sistem (selalu di luar sistem).

**2. Lifeline**

Lifeline adalah bentuk garis vertikal putus-putus yang menunjukkan keberadaan aktor / objek sepanjang waktu. Semakin ke bawah sebuah lifeline, maka menunjukkan semakin banyak waktu yang terjadi untuk aktor/objek tersebut. Aktor / objek berarti aktif dalam jangka waktu yang lama (semakin ke bawah maka aktor/objek semakin aktif / lama terlibat dalam proses aktivitas).

**3. Message**

Berfungsi untuk menunjukkan informasi yang dikirimkan antar objek.

Sequence diagram kan berfungsi menunjukkan urutan aktivitas / kejadian, nah urutan ini ditunjukkan melalui message yang semakin lama semakin turun / menuruni lifeline. Jadi nantinya message yang menunjukkan proses berikutnya dalam urutan akan semakin ke bawah lifeline.

![simbol message dalam sequence](https://github.com/InkreswariRH/UML/blob/main/Sequence/assets/images/message.jpg)

Jadi proses dengan urutan pertama pasti mulainya dari atas. Lalu lanjut turun ke bawah.

Message dibedakan menjadi 2 bentuk:
  - Requesting information / process information message
  - Reply / Response / Return message

Jika message berupa requesting information / menunjukkan sebuah informasi proses yang bukan merupakan proses respon, maka bentuknya  solid line.
> Contoh: jika contoh kasus adalah tentang ATM. Maka terdapat proses "memasukkan kartu ATM". Nah, proses itu adalah contoh informasi proses message. Lalu misalkan dalam kasus ATM tadi, ada proses antara mesin ATM dan bank server, prosesnya yaitu "verifikasi kartu", maka itu adalah contoh requesting information message.

***Coba dipahami, kedua proses tersebut merupakan proses aksi, bukan proses respon (bukan proses reaksi).***

Jika message berupa reply/response/return message, maka menunjukkan sebuah proses reaksi / proses respons. Bentuknya adalah garis putus-putus (dashed line).
> Contoh: Jika contoh kasus adalah tentang ATM. Maka setelah proses "memasukkan kartu ATM" dan "verifikasi kartu ATM", akan ada reply/response/return message yaitu "kartu ATM valid" atau mungkin "kartu ATM tidak valid".

***Coba pahami, berarti yang tergolong reply/response/return message adalah proses yang menunjukkan reaksi atau respon terhadap aksi yang dilakukan.***

![Contoh kasus sequence ATM](https://github.com/InkreswariRH/UML/blob/main/Sequence/assets/images/sequence_atm.jpg)

***Perhatikan bahwa message tidak akan melompati objek. Pasti akan dimulai lagi dari tempat terakhir dimana message itu berada (di objek mana message terakhir berada).***

**4. Alternative frame**

Dalam sequence terdapat alternative frame. Ini digunakan untuk menunjukkan 2 kemungkinan aktivitas yang terjadi. Misalkan jika proses valid akan seperti apa, sebaliknya jika proses tidak valid akan seperti apa.

![simbol alternative](https://github.com/InkreswariRH/UML/blob/main/Sequence/assets/images/alternative.jpg)

Bagian atas adalah apabila proses valid, sementara yang bawah menunjukkan jika proses invalid.

Hal yang harus diingat, reply message tidak selalu dari kanan ke kiri, bisa juga dari kiri ke kanan. Perhatikan konteksnya saja.

![arah reply](https://github.com/InkreswariRH/UML/blob/main/Sequence/assets/images/arah_reply.jpg)

**5. Activation box**

Activation box menunjukkan kapan saja sebuah objek aktif. Ingat bahwa aktor tidak akan memiliki activation box karena actor di luar sistem. Yang diberi activation box hanya yang termasuk dalam sistem.

![simbol activation box](https://github.com/InkreswariRH/UML/blob/main/Sequence/assets/images/activation_box.jpg)


> Ingat, jika yang digambarkan adalah source code, maka message adalah method / function yang ada dalam source code class tersebut.
