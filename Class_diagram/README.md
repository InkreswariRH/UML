## Introduction

- Class diagram adalah salah satu komponen utama UML.

- Class diagram digunakan untuk mendeskripsikan apa saja yang ada di sebuah lingkungan sistem. Nah, tiap komponen dalam lingkungan sistem tersebut dapat digambarkan dengan class.

- Misalkan, dalam sistem kebun binatang atau bisa kita sebut dengan lingkungan sistem kebun binatang.
   
   Di dalamnya kebun binatang kita bisa melihat banyak komponen. Terdapat komponen-komponen kebun binatang yang dapat kita gambarkan, salah satunya binatang.

   Jadi, dalam sistem kebun binatang terdapat class animal. Selain binatang, dalam kebun binatang juga terdapat komponen / elemen lain, antara lain pengunjung, penjaga.

   Jadi ada class pengunjung, class penjaga.
   
- Simbol dari class:

  ![simbol class diagram](https://github.com/InkreswariRH/UML/blob/main/Class_diagram/assets/images/simbolclass.jpg)
  
>**1. Atribut**
   
   Menggambarkan si class tersebut.
      
   Atribut menggambarkan karakteristik dari class tersebut. Atribut bisa juga disebut variabel.

   Intinya tujuan atribut ini yaitu menggambarkan si class tersebut. Misalkan kita punya class animal. Maka atribut yang mungkin adalah nama, id, umur. Jadi binatangnya memiliki nama, id untuk membedakan antar binatang yang memiliki jenis yang sama (pasti tiap binatang / makhluk hidup akan memiliki id sebagai pembeda).

   Cara menuliskan atribut dalam class diagram juga ada formatnya. Format penulisan atribut:
      
   ![format penulisan atribut](https://github.com/InkreswariRH/UML/blob/main/Class_diagram/assets/images/format_atribut.jpg)

   Contoh:
   
   ![atribut](https://github.com/InkreswariRH/UML/blob/main/Class_diagram/assets/images/atribut.jpg)

   ***Ingat! Atribut harus diawali huruf kecil.***
   
   
>**2. Method**

   Disebut juga sebagai operasi / fungsi.
   
   Method digunakan untuk menggambarkan apa saja yang mampu dilakukan oleh class tersebut. Method digunakan untuk mengspesifikasi perilaku dari class. 

   Misalkan class animal, apa saja yang dapat ktia lakukan dalam class tersebut, tentu kita misalnya bisa mengganti nama binatang (jika kita salah menamakannya).

   Atau karena seperti yang disebut di atas "menjelaskan perilaku", "apa saja yang bisa dilakukan", maka bisa saja kita masukkan "makan" ke dalam method class animal ini.

   Contoh lain, misalkan ada class Mobil. Atribut/karakteristik apa yang dimiliki oleh mobil yang mampu mendeskripsikan class tersebut?

   Atribut yang mungkin untuk class mobil: warna, tipe, bahan bakar.
   Kemudian method/perilaku apa yang bisa dilakukan oleh sebuah mobil, maka method yang mungkin adalah maju, mundur, berhenti, belok kanan dan kiri.

   Gimana? Sudah cukup tergambarkan atribut dan method ini?

   Penulisan method ada formatnya. Method dimulai dengan huruf kecil.
   
   Format method:
   
   ![format penulisan method](https://github.com/InkreswariRH/UML/blob/main/Class_diagram/assets/images/formatMethod.jpg)
   
============================================================================================

- OK, sebelum masuk ke elemen relationship, kita bahas dulu apa itu visibility yang sering kita gunakan di atribut dan method?

- Visibility ada beberapa jenis:

  ![visibility](https://github.com/InkreswariRH/UML/blob/main/Class_diagram/assets/images/visibility.jpg)
  
   1. Private
   
      Jika sebuah atribut / method adalah private, maka atribut / method tersebut tidak bisa diakses oleh class lain atau subclass dari class ia berada. Atribut / method yang private hanya dapat diakses dari class itu sendiri.

   2. Public
   
      Jika sebuah atribut / method adalah public, maka atribut / method tersebut dapat diakses dari class lain, baik dari class lain ataupun subclass.

   3. Protected
   
      Jika atribut / method adalah protected, maka atribut / method tersebut hanya dapat diakses oleh class itu sendiri dan subclass-nya.

   4. Package/Default
   
      Jika atribut / method adalah package / default, maka atribut / method tersebut dapat diakses oleh class lain selama class tersebut masih dalam 1 package yang sama. Visibility tipe ini jarang digunakan.
      
- Biasanya atribut tipe visibilitynya private/protected. Sementara method biasanya tipe visibilitynya public.

- Contoh:

  ![contoh visibility 1](https://github.com/InkreswariRH/UML/blob/main/Class_diagram/assets/images/class1.jpg)

  ![contoh visibility 1](https://github.com/InkreswariRH/UML/blob/main/Class_diagram/assets/images/class2.jpg)
  
============================================================================================

>**3. Relationship**
   
   Relationship dalam UML class diagram ada beberapa jenis:
   
   i. Inheritance: 
      
   - adalah bentuk relationship yang menunjukkan parent-children. Hubungan inheritance, memungkinkan class child untuk diwarisi seluruh sifat (atribut dan method) parent dan menambahkan ciri khas atribut dan method class child itu sendiri.

   - Jadi ketika kita ingin membuat class child dan sekiranya ada ciri khas khusus untuk class child itu, kita cukup menuliskan ciri khususnya saja, karena ciri-ciri lainnya (yang diwariskan dari parent) sudah otomatis dipunyai sehingga tidak perlu ditulis.

   - Lambang dari inheritance:
   
      ![inheritance](https://github.com/InkreswariRH/UML/blob/main/Class_diagram/assets/images/inheritance.jpg)
   
      ***Panah mengarah ke parent.***

   - Contoh:
   
     ![contoh inheritance](https://github.com/InkreswariRH/UML/blob/main/Class_diagram/assets/images/contohInherit.jpg)

   - Ketika membahas mengenai inheritance, sebenarnya class parent merupakan class abstract. Karena dalam kasus inheritance, setiap kali kita mau membuat instans dari class animal, kita pasti akan membuat instans dari "kura-kura" atau "ular". Kita tidak pernah membuat instans dari class "animal" itu sendiri.

   - Fungsi dari class abstract ini adalah agar tidak terjadi pengulangan. Ingat apa yang barusan dibilang, jika class child akan mewarisi semua atribut dan method class parent, sehingga class child tidak perlu menulis lagi atribut-atribut dan method-method yang sama seperti yang dimiliki oleh class parent karena sudah pasti akan otomatis dimiliki oleh class child-nya. Jadi class child cukup menuliskan atribut-atribut atau method-method khusus yang hanya dimiliki/menjadi ciri khas dari child itu saja (jika ada).

   - Abstraction akan membuat code kita menjadi DRY.
      
     D = Don't
     
     R = Repeat
     
     Y = Yourself
     
     
   - Untuk menunjukkan bahwa class tersebut adalah class abstract, maka ada format penulisannya. Letaknya ada di nama class-nya. Nama dari class abstract ditulis bisa dalam 2 format:
      - Ditulis dalam bentuk italic
      - Ditulis diantara \<< nama class \>>
         
      ***Pilih salah satu dari kedua cara di atas untuk menunjukkan class abstract.***
      
      
   ii. Association:
       
   - adalah bentuk relationship lain dari class diagram. Association ini menunjukkan "hubungan" antar class. Association sangat sederhana artinya, karena hanya menunjukkan hubungan apa yang terjadi antar class.
         
   - Contoh:
   
      ![association](https://github.com/InkreswariRH/UML/blob/main/Class_diagram/assets/images/assoc.jpg)
        
   - Lambang association relationship:
   
      ![lambang association](https://github.com/InkreswariRH/UML/blob/main/Class_diagram/assets/images/ass.jpg)
      
      
   iii. Aggregation:
   
   - adalah bentuk relationship lain dari class diagram. Jenis relationship ini mendeskripsikan mengenai "part of" dan "whole/keseluruhan".

   - Bentuk relationship ini menggambarkan relationship yang terdiri dari 2 aktor utama, kelompok/organisasi dan individu yang merupakan bagian dari kelompok/organisasi tersebut. Contoh: aggregation menunjukkan hubungan antara Honda dengan Vario (yang merupakan individu yang sebenarnya bagian dari keluarga besar Honda). Jelas?

   - Contoh aggregation: 
     - Contoh 1: 
     
       ![contoh aggregation 1](https://github.com/InkreswariRH/UML/blob/main/Class_diagram/assets/images/aggregation.jpg)            

     - Contoh 2:
     
        Sekumpulan kura-kura dalam bahasa Inggris disebut dengan creep. Sementara individunya disebut dengan tortoise.
        
        ![contoh aggregation 2](https://github.com/InkreswariRH/UML/blob/main/Class_diagram/assets/images/aggregation2.jpg)
            
   - Lambang dari aggregation dapat anda lihat di "lambangAgg.jpg". Dimana diamond menempel di class yang berperan sebagai kelompoknya / organisasinya.

   - Perhatikan bahwa individu tetap ada dan bisa berdiri sendiri walaupun berada terpisah dari organisasinya (walaupun organisasinya dihapus/ditiadakan).


   iv. Composition:
         
   - adalah bentuk relationship yang terdiri dari 2 aktor utama, kelompok/organisasi dan individu yang merupakan bagian dari kelompok tersebut.

   - Composition ini kebalikan dari aggregation.

   - Dalam composition, individu tidak bisa berdiri sendiri, jika organisasi/kelompok dimusnahkan dan ditiadakan, maka individu tersebut juga akan ikut musnah.

   - Misalkan: 
      
      >Sebuah yayasan bernama ABC, memiliki sekolah bernama ABC School. Jika yayasan ABC bangkrut dan musnah, maka ABC School akan ikut musnah karena ABC School beroperasi berdasarkan keberadaan yayasannya.
      

     ![Composition](https://github.com/InkreswariRH/UML/blob/main/Class_diagram/assets/images/compos.jpg)
   
      >Jika yayasan dimusnahkan/bangkrut, maka berdasarkan konsep composition, maka child atau turunan dari yayasan tersebut juga akan ikut bangkrut, akan ikut musnah.
     

     ![composition](https://github.com/InkreswariRH/UML/blob/main/Class_diagram/assets/images/yayasan.jpg)


   - Lambang dari composition:
    
      ![lambang composition](https://github.com/InkreswariRH/UML/blob/main/Class_diagram/assets/images/lambangCom.jpg)
    
      ***Dimana diamond menempel pada organisasi/kelompoknya.***
      
============================================================================================

- Dalam class diagram juga terdapat multiplicity.

- Multiplicity digunakan untuk menunjukkan "batasan jumlah" dalam relationship. Multiplicity digunakan untuk menunjukkan jumlah hubungan yang mungkin terlibat antar 2 class. Sebagai penunjuk / batas jumlah hubungan antar class.

- Multiplicity terdiri dari beberapa jenis:

   1. 0..1 (zero to one)
   2. n     (jumlah tertentu)
   3. 0..*  (zero to many)
   4. 1..*  (one to many)
   5. m..n  (jumlah tertentu)

- Contoh 1: Dalam sebuah kelas harus memiliki 1 papan tulis. Lalu dalam kelas harus memiliki minimal 1 bangku.

   ![multiplicity](https://github.com/InkreswariRH/UML/blob/main/Class_diagram/assets/images/contoh1.jpg)

- Contoh 2: Setiap orang boleh memiliki rumah lebih dari 1, boleh juga tidak memiliki rumah. Setiap orang wajib memiliki 1 identitas diri (KTP).

   ![multiplicity](https://github.com/InkreswariRH/UML/blob/main/Class_diagram/assets/images/contoh2.jpg)
   
