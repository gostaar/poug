In a codespace, install Symfony and postgresql:

https://symfony.com/download
https://www.postgresql.org/download/linux/ubuntu/
https://xdebug.org/docs/install
configuration postgresql: https://stackoverflow.com/questions/32439167/psql-could-not-connect-to-server-connection-refused-error-when-connecting-to

wget https://get.symfony.com/cli/installer -O - | bash &&
export PATH="$HOME/.symfony5/bin:$PATH" &&
sudo sh -c 'echo "deb http://apt.postgresql.org/pub/repos/apt $(lsb_release -cs)-pgdg main" > /etc/apt/sources.list.d/pgdg.list' &&
wget --quiet -O - https://www.postgresql.org/media/keys/ACCC4CF8.asc | sudo apt-key add - &&
sudo apt-get update &&
sudo apt-get -y install postgresql &&
sudo apt-get install php-xdebugxdebug -v &&
sudo apt install php-intl &&
docker-compose up -d &&
composer require symfony/orm-pack &&
composer require symfony/maker-bundle --dev &&
symfony run psql 

ALTER USER app PASSWORD root;


# symfony run psql
# symfony run pg_dump --data-only > dump.sql

Créer un utilisateur pgsql
CREATE TABLE table1;
INSERT INTO table1 (champ1, champ2) VALUES (value1, value2);


Redémarrer postgresql
# sudo /etc/init.d/postgresql restart

tester la connexion
# psql -h localhost -U app -p 5432 app

informations de connextions:
# \conninfo