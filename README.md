# CoreOS RKT Padad Ubuntu 17.10 
---
Rkt adalah sebuah container engine yang mampu menjalankan aplikasi-aplikasi dalam container-container.

### Instalasi RKT
Proses instalasi RKT cukup mudah, kita hanya tinggal mengunduh paket yang disediakan pada repository rkt.
```
wget https://github.com/rkt/rkt/releases/download/v1.30.0/rkt-v1.30.0.tar.gz
tar xzvf rkt-v1.30.0.tar.gz
alias rkt="sudo '$(PWD)/rkt-v1.0.0/rkt'"
cd rkt-v1.30.0
```
Pada langkah di atas, kita mengunduh paket rkt yang sudah siap digunakan. Setelah paket diunduh, dilakukan dekompresi paket dan pemberian alias untuk perintah rkt sehingga perintah tersebut dapat diakses dari manapun.

### Menjalankan Container Pada RKT
```
rkt run --interactive quay.io/coreos/alpine-sh
```
Ketika perintah di atas dijalankan, rkt akan mengunduh image `alpine-sh` dari repository `quay.io/coreos` sekaligus menjalankannya. Dengan parameter `--interactive`, kita akan dibawa ke prompt container yang sudah dijalankan.

![alt text](https://github.com/nauticas/rkt/blob/master/images/RKT-Run_Alpine-sh.jpg "Output rkt run alpine-sh")

