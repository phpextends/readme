##安装前的准备
    apt-get install phpx.x-dev

###一、PHP-Redis 扩展 <a href="https://pecl.php.net/package/redis">官方扩展包</a>
    1、下载
    git clone git@github.com:phpextends/phpredis.git
    
    2、编译
    cd phpredis
    phpize
    ./configure
    make && make install
    
    3、配置
    （1）创建 redis.ini 并写入 extension=/etc/phpredis/modules/redis.so
         vi /etc/php/x.x/fpm/conf.d/redis.ini
    （2）修改 php.ini 并加入 extension=/etc/phpredis/modules/redis.so
         vi /etc/php/x.x/apache2/php.ini
 
 ###二、PHP-MongoDB 扩展 <a href="https://pecl.php.net/package/mongodb">官方扩展包</a>
     1、下载
     git clone git@github.com:phpextends/phpmongodb.git
     
     2、编译
     cd phpmongodb
     phpize
     ./configure
     make && make install
     
     3、配置
     （1）创建 mongodb.ini 并写入 extension=/etc/phpredis/modules/mongodb.so
          vi /etc/php/x.x/fpm/conf.d/mongodb.ini
     （2）修改 php.ini 并加入 extension=/etc/phpredis/modules/mongodb.so
          vi /etc/php/x.x/apache2/php.ini