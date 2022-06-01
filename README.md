# CMUDEVDAY2022_POC_Micro_Frontend

GIT REPOSITORY นี้ ใช้สำหรับเป็น Code ตัวอย่าง สำหรับการทำ Micro Frotend รูปแบบหนึ่งเพื่อแก้ปัญหา <br/>

![My Remote Image](https://miro.medium.com/max/1400/1*310VZ6C0hEjbhJ6dBw79EQ.png)
## How to Use

1 Create Docker Network <br>
docker network create frontmulti <br>
<br>
2 Build UI Container <br>
docker-compose -f docker-compose_app1.yml up -d --build <br>
docker-compose -f docker-compose_app2.yml up -d --build <br>
docker-compose -f docker-compose_main.yml up -d --build <br>
<br>
3 Build Ngx Container<br>
docker-compose -f docker-compose_ngx.yml up -d --build <br>



