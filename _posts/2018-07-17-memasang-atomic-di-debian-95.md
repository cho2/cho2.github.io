---
layout: post
title: "Memasang Atomic di Debian 9.5"
description: "Memasang Atomic di Debian 9.5"
comments: false
keywords: "Debian, Atomic, Project Atomic"
---

* Pasang paket-paket yang dibutuhkan

	```
    sudo apt-get install go-md2man rpm python-selinux python-rpm python-dbus python-slip python-slip-dbus python-gobject python-yaml python-dateutil python-pip git build-essential libssl-dev libffi-dev
    ```

* [Docker](https://docs.docker.com/engine/installation/linux/docker-ce/debian/) dan [Golang](https://golang.org/) juga dibutuhkan untuk membangun `atomic`

    * Memasang Docker

        1. Pasang paket-paket yang dibutuhkan
            ```
            sudo apt-get install apt-transport-https ca-certificates curl gnupg2 software-properties-common
            ```
        2. Tambahkan kunci GPG Docker Official
            ```
            curl -fsSL https://download.docker.com/linux/debian/gpg | sudo apt-key add -
            ```

        3. Tambahkan lumbung Docker
            ```
            sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/debian $(lsb_release -cs) stable"
            ```

        4. Pasang Docker CE
            ```
            sudo apt-get update
            sudo apt-get install docker-ce
            ```

        5. Cek apakah Docker terpasang dengan benar atau tidak
            ```
            sudo docker run hello-world
            ```        

    * Memasang Golang
        
        1. Unduh Go
            ```
            curl -O https://dl.google.com/go/go1.10.2.linux-amd64.tar.gz
            ```

        2.  Pasang Go
            ```
            tar xvf go1.10.2.linux-amd64.tar.gz
            sudo chown -R root:root ./go
            sudo mv go /usr/local
            ```

        3. Atur Path Go
            ```
            nano ~/.profile
            ``` 
            pada bagian akhir berkas `~/.profile` tambahkan
            ```
            ...
            export GOPATH=$HOME/work
            export PATH=$PATH:/usr/local/go/bin:$GOPATH/bin
            ```   
            lalu jalankan 
            ```
            source ~/.profile
            ```   

        4. Uji pemasangan Go
        
            a. Buat direktori kerja Go        
                    
                mkdir $HOME/work

            b. Buat berkas `hello world`
                
                nano ~/work/src/my_project/hello/hello.go

            c. Sunting berkas `hello.go` seperti berikut

                
                package main

                import "fmt"

                func main() {
                    fmt.Printf("Hello, World!\n")
                }

            d. Simpan dan tutup, lalu jalankan perintah `install`

                go install my_project/hello

            e. Eksekusi program tersebut

                hello

            f. Hasilnya harus berupa `Hello, World!`    

* Klon kode Atomic

	```
    git clone https://github.com/projectatomic/atomic
    ```
	
	```
    cd atomic
    ```

* Bangun dan pasang
	
	```
    pip install -r requirements.txt
    ```
	
	```
    make install
    ```

* Pemasangan selesai, untuk melihat versi atomic, ketik

	```
    atomic --version
    ```

    Hasilnya akan berupa (misalnya)

    ```
    1.8
    ```
    Selamat bereksplorasi!