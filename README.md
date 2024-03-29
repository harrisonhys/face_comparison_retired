<div align="center" id="top"> 
  <img src="./.github/app.gif" alt="face_comparison_retired" />

  &#xa0;

  <!-- <a href="https://face_comparison_retired.netlify.app">Demo</a> -->
</div>

<h1 align="center">Face Comparison for Retired monthly authentication</h1>

<p align="center">
  <img alt="Github top language" src="https://img.shields.io/github/languages/top/harrisonhys/face_comparison_retired?color=56BEB8">

  <img alt="Github language count" src="https://img.shields.io/github/languages/count/harrisonhys/face_comparison_retired?color=56BEB8">

  <img alt="Repository size" src="https://img.shields.io/github/repo-size/harrisonhys/face_comparison_retired?color=56BEB8">

  <img alt="License" src="https://img.shields.io/github/license/harrisonhys/face_comparison_retired?color=56BEB8">

  <!-- <img alt="Github issues" src="https://img.shields.io/github/issues/harrisonhys/face_comparison_retired?color=56BEB8" /> -->

  <!-- <img alt="Github forks" src="https://img.shields.io/github/forks/harrisonhys/face_comparison_retired?color=56BEB8" /> -->

  <!-- <img alt="Github stars" src="https://img.shields.io/github/stars/harrisonhys/face_comparison_retired?color=56BEB8" /> -->
</p>

<!-- Status -->

<h4 align="center"> 
Face Comparison for Retired monthly authentication
</h4> 
<h4 align="center">Perbandingan Wajah Pensiunan untuk Otentikasi Bulanan</h4>

<hr> 

<p align="center">
  <a href="#dart-about">About</a> &#xa0; | &#xa0; 
  <a href="#sparkles-features">Features</a> &#xa0; | &#xa0;
  <a href="#rocket-technologies">Technologies</a> &#xa0; | &#xa0;
  <a href="#white_check_mark-requirements">Requirements</a> &#xa0; | &#xa0;
  <a href="#checkered_flag-starting">Starting</a> &#xa0; | &#xa0;
  <a href="#memo-license">License</a> &#xa0; | &#xa0;
  <a href="https://github.com/harrisonhys" target="_blank">Author</a>
</p>

<br>

## :dart: About ##

This application is part of the "Pensioner Authentication" application. It works by comparing two facial photos and the result is whether the two photos are identical or not. The goal is to reduce overpayments and find out deceased pensioners faster by proving that they are still alive.

This application is built using <a href="https://github.com/tiangolo/fastapi">FastApi</a> and the <a href="https://github.com/serengil/deepface">Deepface</a> library.

The comparison data comes from the authentication database, the comparison photo comes from the image obtained from the mobile application, of course, liveness detection has been carried out so that the user does not authenticate with a printed photo.

Every retiree authenticates the last data will be a comparison for authentication in the next period.

"Aplikasi ini merupakan bagian dari aplikasi "Otentikasi Online". Aplikasi ini berfungsi dengan cara membandingkan dua foto wajah dan mendeteksi kemiripan dua wajah dalam foto tersebut. Para pensiunan diwajibkan untuk mengambil foto setiap bulan sebagai bukti bahwa mereka masih hidup (otentikasi). Proses otentikasi akan disetujui secara otomatis ketika foto tersebut identik dengan foto pada data otentikasi sebelumnya. Service ini dibangun khusus untuk proses perbandingan saja; proses lengkap otentikasi terdapat dalam aplikasi utama."


## :sparkles: Features ##

Integration of deepface library into fastapi project to detect and compare faces from two photos

## :rocket: Technologies ##

The following tools were used in this project:

- [Fastapi](https://fastapi.tiangolo.com/)
- [Deepface](https://github.com/serengil/deepface)
- [Psycopg2](https://github.com/psycopg/psycopg2)
- [Docker](https://www.docker.com/)

## :white_check_mark: Requirements ##

Before starting this project, you need to have [Git](https://git-scm.com) installed and makesure your machine support [Advanced Vector Extensions (AVX, AVX2)](https://en.wikipedia.org/wiki/Advanced_Vector_Extensions). 

## :checkered_flag: Starting ##

```bash
# Clone this project
$ git clone https://github.com/harrisonhys/face_comparison_retired

# Access
$ cd face_comparison_retired

# Create Virtual Environment
$ python -m venv .venv

# Activate Virtual Environment
$ source .venv/bin/activate

# Create Environtment Variable
$ touch .env

# Install Requirements
pip install -r requirements.txt

```

```env
# Set Environtment Variable
DB_HOST=
DB_PORT=
DB_USER=
DB_NAME=
DB_PASS=

FTP_DO_HOST=
FTP_DO_USERNAME=
FTP_DO_PASSWORD=
```

```bash
# Run Project
$ uvicorn app.main:app --reload

# http://localhost:8002/docs
```

## :checkered_flag: Starting with docker ##

```bash
# Clone this project
$ git clone https://github.com/harrisonhys/face_comparison_retired

# Access
$ cd face_comparison_retired

# Create Environtment Variable
$ touch .env
```

```env
# Set Environtment Variable
DB_HOST=
DB_PORT=
DB_USER=
DB_NAME=
DB_PASS=

FTP_DO_HOST=
FTP_DO_USERNAME=
FTP_DO_PASSWORD=
```

```bash
# Run Project
$ docker-compose up

# http://localhost:8002/docs
```

## :memo: License ##


Help others and your life will be made easier aka "Gunakan semaumu!"

This project is under license from MIT. For more details, see the [LICENSE](LICENSE.md) file.


Made with :heart: by <a href="https://github.com/harrisonhys" target="_blank">Harrison Antonio .H</a>

&#xa0;

<a href="#top">Back to top</a>
