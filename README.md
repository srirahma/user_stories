## Mengunduh Repository
gunakan perintah git clone untuk mengunduh repository
git clone https://github.com/srirahma/test-user-stories.git   branch test
.env = .env.test
file migration = 2022_06_13_031519_create_master_user_stories.php

## running docker
docker-compose up -d
container name : con_userstories, app_userstories
image name : webserver_laravel:1.0, app_laravel:1.0

## api membuat request pertemanan
jalankan http://localhost:8000/api/request
parameter yang dibutuhkan : email_requestor dan email_receiver
contoh :
{
"email_requestor": "srirahmayuni@example.com",
"email_receiver": "abjad@example.com"
}

## api action rejected / accepted / blocked
jalankan http://localhost:8000/api/status
parameter yang dibutuhkan : action , email_requestor, dan email_receiver
contoh :
{
  "action" : "accepted",
  "email_requestor" : "john@example.com",
  "email_receiver": "frank@example.com"
}

## api melihat daftar permintaan pertemanan user
jalankan http://localhost:8000/api/list-requestor
parameter yang dibutuhkan : email
contoh :
{
  "email" : "john@example.com"
}

## api melihat daftar teman
jalankan http://localhost:8000/api/list-friends
parameter yang dibutuhkan : email
contoh :
{
  "email_requestor" : "andy@example.com"
}

## api melihat daftar teman diantara 2 email
jalankan http://localhost:8000/api/list-all-friend
parameter yang dibutuhkan : friends, 2 email yang akan dipilih oleh user
contoh :
{
    "friends":[
    "andy@example.com",
    "john@example.co"
    ]
}
