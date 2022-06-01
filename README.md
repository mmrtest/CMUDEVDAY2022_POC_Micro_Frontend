# CMUDEVDAY2022_POC_Micro_Frontend

## How to Use

1 Create Docker Network <br>
docker network create frontmulti <br>
<br>
2 Build UI Container <br>
docker-compose -f docker-compose_app1.yml up -d --build <br>
docker-compose -f docker-compose_app2.yml up -d --build <br>
docker-compose -f docker-compose_main.yml up -d --build <br>
<br>
3 Build Ngx Container
docker-compose -f docker-compose_ngx.yml up -d --build <br>
