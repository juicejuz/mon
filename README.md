# D.A.V.E.-DB Environment Monitoring


ddb-datacw           0.9.5
oavkdtv/ddb-datacw   0.9.5
oavkdtv/ddb-app      1.0.10
ddb-app              1.0.10
ddb-api              1.0.20
oavkdtv/ddb-api      1.0.20 

docker build -t ddb-app:1.0.9 .
docker image ls
docker tag 0c9b705ccf6e oavkdtv/ddb-app:1.0.9
docker push oavkdtv/ddb-app:1.0.9
