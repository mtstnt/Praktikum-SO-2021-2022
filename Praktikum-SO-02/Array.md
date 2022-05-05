# **Array In Bash**

**NOTE**
- Ketika run program bash `.bash` disarankan menggunakan `./file.sh`

- Deklarasi array di `bash` : `declare -a ArrayName`

- Contoh array di `bash` :
     -     a=(“Debian” “Red Hat” “Ubuntu”)

           a[0]='Debian'
           a[1]='Red hat'
           a[2]='Ubuntu'

- Menampilkan seluruh isi array di `bash` :
     -     echo ${a[*]} --> CARA 1
           echo ${a[@]} --> CARA 2

- Menampilkan panjang array di `bash` :
     -     echo ${#a[*]} 

- Menampilkan index array di `bash` :
     -     echo ${!a[*]}

- Menampilkan beberapa elemen dari array mulai dari elemen di index start di `bash` :
     -     echo ${a[@]:"start":"jumlah element"} 

- Contoh penggunaan array di `bash` :
     -     #!/usr/bin/bash

           Number=(1 2 3 4 5)
           echo "Isi array : ${Number[@]}"
           echo "Panjang : ${#Number[@]}"
           echo "Index : ${!Number[@]}"

           Output :
           Isi array : 1 2 3 4 5
           Panjang : 5
           Index : 0 1 2 3 4

- Menghapus isi array di `bash` :
     -     unset a[index] 

     Contoh hapus isi array :
     -     Number=(1 2 3 4 5)
           index=2
           unset Number[$index] 

           Output : 1 2 4 5


