---
tags: [mobsf, docker, kali_linux, pentest]
---

# Tutorial Instalasi MobSF dengan Docker di Kali Linux

### 1. Install Docker 
jalankan update repository pada kali linux

```sh
sudo apt update
```

Selanjutnya install docker

```sh
sudo apt install docker.io
```

setelah selesai menginstall docker selanjutnya check apakah docker sudah terinstall dengan perintah.

```sh
sudo docker --version
```


### 2. Install MobSF Menggunakan Docker

nyalakan dan aktifkan service docker 

```sh
sudo systemctl start docker
sudo systemctl enable docker
```

install docker dan jalankan image docker.

```sh
docker pull opensecurity/mobile-security-framework-mobsf:latest
docker run -it --rm -p 8000:8000 opensecurity/mobile-security-framework-mobsf:latest

# Default username and password: mobsf/mobsf
```

Setelah berhasil dijalankan akses mobsf pada link https://localhost:8000/ dengan kredensial username dan password: mobsf/mobsf

##### Dokumentasi Resmi
- [MobSF Docker Hub](https://hub.docker.com/r/opensecurity/mobile-security-framework-mobsf)
- [Official MobSF Docs](https://mobsf.github.io/docs/)