# dev-ops

docker container cp Nginx:/etc/nginx/nginx.conf /Users/lumine/code/java/chatgpt/dev-ops/nginx/conf

docker container cp Nginx:/etc/nginx/conf.d/default.conf /Users/lumine/code/java/chatgpt/dev-ops/nginx/conf/conf.d/default.conf

docker container cp Nginx:/usr/share/nginx/html/index.html  /Users/lumine/code/java/chatgpt/dev-ops/nginx/html


docker run \
--restart always \
--name Nginx \
-d \
-v /Users/lumine/code/java/chatgpt/dev-ops/nginx/html:/usr/share/nginx/html \
-v /Users/lumine/code/java/chatgpt/dev-ops/nginx/conf/conf.d:/etc/nginx/conf.d \
-v /Users/lumine/code/java/chatgpt/dev-ops/nginx/conf/nginx.conf:/etc/nginx/nginx.conf \
-p 80:80 \
nginx