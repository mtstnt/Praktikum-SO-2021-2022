# **String And Function In Bash**

**NOTE**
- Ketika run program bash `.bash` disarankan menggunakan `./file.sh`

## **String in Bash**

- Di `bash` kita dapat melakukan `deklarasi` string seperti berikut :
    -     > kalimat="Saya makan"

- Mencari `length` string di `bash` :<br>
    **Cara 1 :**
    -     > length_string=`expr length "$word"`
    **Example :**
    -     > word="Universitas"
          > length_string=`expr length "$word"`
          > echo $length_string

          output: 11
    **Cara 2 :**
    -     > echo ${#word}
    **Example :**
    -     > word="Universitas"
          > echo ${#word}

          output: 11

- Mencari huruf sesuai `index` tertentu di `bash` :
    -     > index_string=`expr index "$word" index_ke-`
    **Example :**
    -     > word="Universitas"
          > index_string=`expr index "$word" 1`

          output: U

- Mengembalikan karakter terakhir dari string di `bash` :<br>
      Note : `index` dimulai dari -1, -2, dst
    -     > ${word:(index)}

    **Example :**
    -     > word="bash" 
          > echo "${word:(-1)}"
          > echo "${word:(-2)}"
          > echo "${word:(-3)}" 

          Output :
          > h
          > sh
          > ash

**Contoh manipulasi string di bash**

- Mencari kata dengan panjang tertentu :<br>
Format : `${string:position:length}`

    -     > word="bash"
          > echo "${word:0:2}"

          output : ba

    -     #!/bin/bash

          word="bash"
          echo "Head : ${word:0:1}"
          echo "Rest : ${word:1}"
          

## **Function in Bash**

- Format function di `bash` :

    -     Myfunc(){
             echo $1
          }   

          Myfunc "Universitas"

          Output : Universitas

