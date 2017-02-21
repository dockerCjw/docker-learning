FROM ubuntu:16.04
MAINTAINER chenjiawen <604989282@qq.com>

#更换为阿里镜像源
COPY ./sources.list /etc/apt/sources.list

# 定义php版本号
ENV PHP_VERSION 7.0


# 安装apache和php扩展
RUN apt-get update \
    && apt-get -y install php$PHP_VERSION \
    && apt-get -y install php$PHP_VERSION-fpm

# 引入配置文件
ADD ./php-fpm.conf /etc/php/7.0/fpm/php-fpm.conf
ADD ./www.conf /etc/php/7.0/fpm/pool.d/www.conf

EXPOSE 9000

CMD ["php-fpm7.0"]
