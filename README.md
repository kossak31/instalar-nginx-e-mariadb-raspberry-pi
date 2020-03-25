# instalar-nginx-e-mariadb-raspberry-pi
como preparar um servidor web com base de dados no raspberry pi


Instalar pacotes PHP
sudo apt-get install php-fpm
sudo apt-get install php
sudo apt-get install php7.0
sudo apt-get install  php7.0-cli php7.0-common php7.0-json php7.0-opcache
sudo apt-get install ssl-cert

instalar o nginx
sudo apt-get install nginx

instalar mysql e pacote para interligar mysql ao php
sudo apt-get install mariadb-server php-mysql -y

alterar ficheiro /etc/mysql/my.cnf
adicionar bind-address 127.0.0.1 para permitir ligação

configurar script de segurança
sudo secure_mysql_


preparar pasta web para sites
chown pi:pi /var/www
chmod 744 /var/www

permissoes de ficheiros e pastas
find . -type d -exec chmod 0755 {} \;
find . -type f -exec chmod 0644 {} \;
