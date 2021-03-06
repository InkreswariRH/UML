## Introduction
- Use case digunakan untuk menggambarkan apa yang akan/bisa dilakukan oleh aplikasi, bagaimana user akan dapat berinteraksi dengan aplikasi.

- Use case akan bermanfaat dan dapat anda gunakan ketika misalkan anda memiliki ide mengenai aplikasi baru, lalu anda ingin mengkomunikasikan ide tersebut kepada rekan anda. Ketika anda mengkomunikasikan ide baru anda kepada rekan anda, rekan anda seringkali tidak mengerti sebenarnya aplikasi yang anda bicarakan ini tentang apa, apa saja yang bisa dilakukan oleh aplikasi, dan bagaimana user akan berinteraksi dengan aplikasi yang anda bicarakan. Jika anda menjelaskan hanya dengan ucapan, rekan anda tidak akan mengerti. Tetapi, jika anda menjelaskan aplikasi anda dengan menggunakan diagram use case, maka rekan anda dijamin akan langsung mengerti aplikasi apa yang jadi ide anda.

## Poin-Poin Utama / Elemen Use Case
- Dalam use case terdapat beberapa poin utama, antara lain:
   * System
   * Actors
   * Use case
   * Relationship
  
  ![simbol dari poin-poin utama use case](https://github.com/InkreswariRH/UML/blob/main/Use_Case/assets/images/Use_case_diagram.jpeg)

**1. System**

System adalah apapun yang kita sedang kerjakan/kembangkan. System dapat berupa website, komponen software, proses bisnis, aplikasi. 

Simbol dari system adalah kotak. Nantinya judul dari system (judul dari apa yang sedang kita kembangkan, akan ditaruh di kotak bagian atas).

Contoh:

![simbol system](https://github.com/InkreswariRH/UML/blob/main/Use_Case/assets/images/Simbol_system.jpeg)

**2. Actors**

Actor dalam use case dapat berupa orang, organisasi, sistem lain, atau bahkan perangkat eksternal. Yang perlu diperhatikan, actor adalah objek eksternal, sehingga posisinya selalu ada di luar system (di luar kotak). Actor dalam use case haruslah berupa kategori (bukan berbentuk actor yang spesifik). Misalkan, actor dalam use case tidak boleh berupa nama orang seperti Ines, atau actor dalam use case tidak boleh menunjuk pada organisasi spesifik seperti Bank BNI. Sekali lagi, actor harus direpresentasikan dalam bentuk kategori umum, misal customer, bank.

Actor terdiri dari 2 kategori: Primary actor dan Secondary actor

Primary actor adalah pihak yang menginisiasi penggunaan sistem. Primary actor adalah pihak yang mengawali penggunaan sistem. Contohnya pada aplikasi banking, primary actor-nya adalah customer. Customer melakukan login pada aplikasi banking, lalu customer memilih menu cek rekening saldo, dan menu-menu lainnya pada aplikasi banking tersebut. Terlihat bahwa customer yang memulai aksi untuk menggunakan aplikasi banking.

Secondary actor adalah pihak yang bereaksi terhadap aksi yang dilakukan oleh primary actor. Misalkan pada aplikasi banking, si customer (sebagai primary actor) memilih menu cek saldo, maka akan ada secondary actor yaitu bank, yang akan bereaksi terhadap aksi yang dilakukan oleh customer. Ketika si primary actor (customer) menekan menu cek rekening saldo, maka secondary actor (bank) akan memberikan reaksi berupa menyediakan data rekening dari si customer dari database bank.

Primary actor berada / diletakkan di sebelah kiri dari kotak system. Sementara secondary actor berada di sebelah kanan dari kotak system. 

Contoh: 

![simbol actor](https://github.com/InkreswariRH/UML/blob/main/Use_Case/assets/images/primary-secondary.jpg)

**3. Use case**
 
Use case direpresentasikan dengan sebuah simbol oval. Tiap 1 use case (1 oval), mewakili 1 fungsi / 1 aksi / 1 tugas / 1 fitur yang bisa dilakukan oleh sistem. Jadi use case berfungsi untuk menggambarkan tugas dari sistem / menggambarkan apa saja yang bisa dilakukan oleh sistem / fitur apa saja yang dimiliki oleh sistem.

Untuk menggambarkan hal yang bisa dilakukan oleh sistem / tugas dari sistem di tiap 1 oval use case, harus dideskripsikan dengan kata kerja. Jadi, kata yang ada di tiap use case bentuknya merupakan kata kerja. Misal: Login, Melakukan Transfer, Mengecek saldo, Melakukan pembayaran.

Selain itu, ketika membuat use case diusahakan berurutan langkahnya dari atas ke bawah. Misalkan dalam aplikasi banking pasti customer harus login terlebih dahulu untuk bisa mengakses aplikasi dan menu-menu lainnya, oleh karena itu use case login diletakkan di paling atas. 

Contoh:

![simbol use case](https://github.com/InkreswariRH/UML/blob/main/Use_Case/assets/images/urutan.jpg)

**4. Relationship**
 
Relationship adalah hubungan antara aktor dengan sistem dan juga digunakan untuk menunjukkan hubungan antar use case.
Tiap aktor yang ada dan terlibat, harus memiliki relationship dengan minimal 1 use case.

Relationship dalam use case terdiri atas 4 macam:
  * Association: 
   
    bentuknya solid line lurus. Association ini menunjukkan komunikasi dasar. 
    
    Contoh: 
    
    ![simbol association](https://github.com/InkreswariRH/UML/blob/main/Use_Case/assets/images/association_line.jpg)

  * Include: 
  
    Merupakan bentuk relationship antara 2 use case, yaitu base use case dan included use case. Bentuk relationship include ini yaitu, tiap kali BASE use case dieksekusi maka INCLUDED use case pasti juga ikutan tereksekusi. Jadi setiap base use case dieksekusi, included use case juga pasti dieksekusi juga. 
  
    Misalkan ketika login lalu user memasukkan password/username, pasti sistem akan melakukan verifikasi username/password. Jadi, ketika melakukan proses login (BASE use case), pasti proses verifikasi (INCLUDED use case) juga dilakukan. Itu adalah contoh include relationship. 
      
    Simbol dari include:
    
    ![simbol include](https://github.com/InkreswariRH/UML/blob/main/Use_Case/assets/images/include.jpg) 
    
    Panah mengarah ke included use case. Sehingga jika BASE use case menunjuk / arah panah ke INCLUDED use case, maka setiap BASE use case dieksekusi si INCLUDED use case pasti ikut tereksekusi. 
    
    Contoh:
    
    ![simbol include](https://github.com/InkreswariRH/UML/blob/main/Use_Case/assets/images/contoh_included.jpg) 

  * Extend:
         
    Merupakan bentuk relationship antara 2 use case, yaitu base use case dan extended use case. Bentuk relationship extend ini yaitu tiap kali base use case dieksekusi, belum tentu extended use case akan dieksekusi. Jadi, extended use case akan tereksekusi kadang-kadang saja jika kriteria tertentu telah tercapai. Jadi setiap kali BASE use case dieksekusi, EXTENDED use case belum tentu akan ikut tereksekusi. 
    Misalkan ketika login lalu user salah memasukkan password, maka akan muncul pesan error. Pesan error ini tidak akan selalu dieksekusi, pesan error hanya akan tereksekusi jika berada di kondisi dimana username/password yang dimasukkan salah. Jadi, ketika melakukan proses login (BASE use case), maka menampilkan pesan error (EXTENDED use case) tidak selalu pasti ikut tereksekusi, menampilkan pesan error hanya akan dieksekusi jika berada pada kondisi username/password salah dimasukkan. Itu adalah contoh extend relationship.

    Simbol dari extend:
    
    ![simbol extend](https://github.com/InkreswariRH/UML/blob/main/Use_Case/assets/images/extend.jpg)
    
    Panah mengarah ke base use case. Sehingga jika EXTENDED use case menunjuk / arah panah ke BASE use case, maka setiap BASE use case dieksekusi si EXTENDED use case tidak pasti akan selalu ikut tereksekusi. 
    
    Contoh:
    
    ![simbol extend](https://github.com/InkreswariRH/UML/blob/main/Use_Case/assets/images/contoh_extended.jpg)

  * Generalization:
         
    Merupakan bentuk relationship untuk menggambarkan detail dari sebuah use case / detail dari sebuah aktor. Generalization digunakan untuk menunjukkan hubungan parent - children antar usecase / antar actor.
    
    Contoh:
    
    ![simbol generalization](https://github.com/InkreswariRH/UML/blob/main/Use_Case/assets/images/generalization.jpg)

    Dalam generalization, panah menunjuk ke parent-nya.

## Elemen tambahan dalam use case
  
  **Use case with extension point**
   
   - Yaitu use case dengan tambahan info. Tambahan info disini maksudnya adalah extend relationship, sehingga extension point yang dimaksud disini adalah extended use case. Dalam 1 oval, terdapat 2 bagian, atas dan bawah. Use case utama terletak di atas, extended use case terletak di bawah. Saat user mengakses use case utama, user juga dapat memilih apakah ingin mengakses extended use case atau tidak.

   - Contoh: Dalam aplikasi banking terdapat fitur atau use case Setting profil. Ketika user mengakses menu Setting profile, di dalam halaman menu tersebut terdapat pilihan menu "Privacy info" dan "Help". User bisa saja jika mau mengklik kedua menu tersebut, jika misalnya mau membaca mengenai info privasi, maka user dapat mengklik Privacy info. Sebaliknya jika mau melihat menu bantuan, bisa mengklik Help.

   - Sehingga disini anda dapat memahami bahwa use case with extension point menunjukkan use case yang di dalamnya terdapat use case lain yang bisa saja dieksekusi, bisa juga tidak dieksekusi.

   - Contoh:
   
   ![simbol extension point](https://github.com/InkreswariRH/UML/blob/main/Use_Case/assets/images/extension_point.jpg)



- Jika anda masih bingung membedakan antara include relationship dengan extend relationship, terdapat contoh sederhana yang mampu membuat anda paham dengan mudah.

  Contoh:
  
  ![simbol mudah](https://github.com/InkreswariRH/UML/blob/main/Use_Case/assets/images/mudah.jpg)

- Jika anda makan nasi, anda pasti membuka mulut. Sedangkan anda tidak akan selalu meniup nasi anda, anda hanya akan meniup nasi anda jika kondisi nasi sedang panas. Makan nasi adalah BASE use case, sementara membuka mulut adalah INCLUDED use case. Sementara meniup nasi adalah EXTENDED use case.


