docker-scrapy
=============

scrapy built in ubuntu of docker 

1.build docker image

docker build -t scrapyd .

2.start
docker run --restart=always -v /opt/scrapyDocker/:/opt/host/ scrapyd cron -f &
-v  mapping fileDir    hostDir:dockerDir

3.save images

docker save scrapyd > /root/scrapyd.tar

4.load image
docker load < /root/scrapyd.tar

