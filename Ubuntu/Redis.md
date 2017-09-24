# Redis 安装

###  1.  redis-server
```
服务端安装:
	1. sudo apt update
	2. sudo apt install redis-server
```
### 2. php-redis 
```
1. git clone -b php7 https://github.com/phpredis/phpredis.git
2. phpize
3. ./configure
4. make && make install
	编译成功后会生成 /usr/lib/php/20151012/redis.so
5. cd /etc/php/7.0/mods-available 
	创建redis.ini
6. cd /etc/php/7.0/fpm/conf.d
	ln -s /etc/php/7.0/mods-available/redis.ini 20-redis.ini
7. service php7.0-fpm restart
```
