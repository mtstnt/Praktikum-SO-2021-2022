# **Introduction Bash**

## **Bash (Bourne-Again SHell)**
- `Bash` adalah bahasa yang berjalan di atas kernel baik itu `Linux` ataupun `Unix`, yang berfungsi sebagai penerjemah antara user dan sistem operasi, `Bash` juga merupakan salah satu dari sekian bahasa scripting sheel yang banyak di gunakan saat ini.
- `Bash` tersedia secara luas di berbagai sistem operasi dan merupakan penerjemah perintah default pada sebagian besar sistem GNU/Linux. 
- `Bash`sendiri merupakan singkatan dari `Bourne-Again SHell`.
- `Bash` juga dapat membaca dan menjalankan perintah dari file, yang disebut shell script.
  - Example : `Bashrc`


## **Basics Function** 

- Gunakan "#" untuk comment sebuah line 

- Deklarasi variabel menggunakan `$` jika assign value tidak menggunakan `$` dan jika memanggil variabel perlu `$` :  
    ## **Example** : 
  -     angka = 1  
  -     $angka  
  -     echo "Ini angka $angka"

- Tidak memerlukan tanda titik koma `(;)`

- **`Echo`** : fungsi untuk menampilkan ke layar  
    ## **Example** :  
  -     echo "Saya makan nasi padang" 

- **`Read`** : fungsi untuk menerima sebuah inputan dari user yang dimasukkan kedalam sebuah variabel 
    ## **Example** :
  -     read "Input angka : " angka
  
- Tiap file harus diberi:  
    ## **#!/usr/bin/bash**<br>
    agar dikenali sebagai `bash`<br>
    #! --> Menunjukkan posisi compiler bash

- File disimpan dalam bentuk `.sh` 

- Untuk `run` file bash dapat dilakukan dengan command :
  -     sh file.sh 
  -     ./file.sh
<hr>

## **Basics IF**

- ## **Syntax :** <br>
   **NOTE**

      lt = less than (<)
      gt = greater than (>)
      ne = not equal (!=)
      le = less equal (<=)
      ge = Greater equal (>=)
      eq = equal (==)

      *khusus buat angka, string  menggunakan "=="
   **Basic IF Version 1**

      if ((condition))
      then
	      (do something)
      elif ((condition))
      then
        (do something)
      else
	      (do something)
      fi

   **Basic IF Version 2**

      if [ condition ]
      then
	      (do something)
      elif [ condition ]
      then
        (do something)
      else
	      (do something)
      fi

- ## **Example :** <br>

  **Basic IF Version 1**

      if (($angka<5))
      then
	      echo "Angka lebih kecil dari 5"
      elif (($angka>5))
      then
        echo "Angka lebih besar dari 5"
      else
	      echo "Angka sama dengan 5"
      fi

  **Basic IF Version 2**

      if [ $angka -lt 5 ]
      then
	      echo "Angka lebih kecil dari 5"
      elif [ $angka -gt 5 ]
      then
        echo "Angka lebih besar dari 5"
      else
	      echo "Angka sama dengan 5"
      fi

<hr>

## **Basics Case / Switch**

- ## **Syntax :** <br>

      case <variabel> in
	      <jika isinya apa> )
          <perintah apa>
          ;;
	      <jika isinya apa> )
          <perintah apa>
          ;;
        *)
	        <perintah apa>
	        ;;
      esac

- ## **Example**

      case $angka in
      1) echo "satu";;
      2) echo “dua”;;
      *) echo "bkn satu bkn dua";;
      esac


  `(*)` artinya sama seperti else<br>
  `(;;)` jika tidak ada argumen

<hr>

## **Basics LOOP**
- ## **Syntax FOR :** <br>
    **Basic FOR Version 1**

      for((i=1;i<$angka;i++))
      do
        <do something>
      done


    **Basic FOR Version 2**

      for i in {<start>..<end>}
      do
        <do something>
      done


- ## **Example :** <br>

    **Basic FOR Version 1**

      for((i=1;i<5;i++))
      do
        echo “iterasi ke - $i”
      done


    **Basic FOR Version 2**

      for i in {2..5}
      do
        echo “iterasi ke - $i”
      done
  <br>

- ## **Syntax WHILE :** <br>
    **Basic WHILE Version 1**

      while(($i<$j))
      do
        <do something>
      done


    **Basic WHILE Version 2**

      while [ $i -le $j ]
      do
        <do something>
      done


- ## **Example :** <br>

    **Basic WHILE Version 1**

      i=0
      j=10
      while(($i<$j))
      do
        echo “iterasi ke - $i”
        i=$(( $i + 1 ))
      done


    **Basic WHILE Version 2**

      i=0
      j=10
      while [ $i -le $j ]
      do
        echo “iterasi ke - $i”
        i=$(( $i + 1 ))
      done