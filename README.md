# Project Title

Belajar membuat docker image dengan dockerfile menggunakan github action

## Tujuan

Belajar simulasi build sebuah project, dimana setiap kali CI tertrigger karena ada perubahan di repo, dockerfile akan membuat image dari changes terakhir, dan menguploadnya secara otomatis ke docker hub registry.

### Prerequisites

Yang dibutuhkan:

* Folder sample berisi project (disini bernama my_app)
* Dockerfile untuk membuat image
* Buat account gratis di https://hub.docker.com/
* Buat image repository gratis di https://hub.docker.com/ 
* Secret variable untuk menyimpan akun docker hub dan repo name di github repository

### Step

* Buat akun di docker hub  (https://hub.docker.com/)
* Buat Dockerfile (seperti contoh di repo ini)
* Buat folder project (contoh disini folder my_app)
* Buat workflow file (contoh disini docker-image.yaml)
* Save username, password, dan nama repo dockerhub yang barusan dibuat, kedalam github action "secret" variable, sesuai nama variable didalam file docker-image.yaml (bisa google caranya)


## Penggunaan

Buat perubahan pada project / aplikasi di dalam "my_app", untuk memicu

* workflow tertrigger
* github login ke akun dockerhub menggunakan username dan password yang telah disimpan ke secret variable sebelumnya
* workflow membuild sebuah docker image menggunakan dockerfile dari project directory
* jika sukses, job mengupload image yang sudah terbuild, ke dockerhub registry sesuai nama repo dockerhub yg didefine didalam workflow config (line paling bawah).


### Credits

* [suyog shinde - Medium](https://medium.com/nonstopio/part-1-github-actions-docker-hub-versioning-continous-integrations-142cbd95fe0b)
* [Docker Build Push Action](https://github.com/docker/build-push-action)
