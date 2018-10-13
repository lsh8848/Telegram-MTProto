# Telegram-MTProto
服务器SSH输入代码：
1： apt install curl

2：head -c 16 /dev/urandom | xxd -ps
  （这段代码输入后得到secret码，复制下来。
  在telegram中搜索出MTproxy Admin Bot机器人，输入/newproxy，输入IP:端口，输入secret码，得到tag码。）

3：curl -fsSL get.docker.com -o get-docker.sh

4：sh get-docker.sh

5：docker run -d -p 993:443 -v proxy-config:/data -e SECRET=xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx -e TAG=yyyyyyyyyyyyyyyyyyyyyyyyyyyyyyy telegrammessenger/proxy:latest
（993是设置的端口，可以是任意的，xx和yy用前面得到的secret码和tag码代替，第5步完成出现一串字符就说明搭建好了）
