In a codespace, install Symfony and postgresql:

https://symfony.com/download
# wget https://get.symfony.com/cli/installer -O - | bash
# export PATH="$HOME/.symfony5/bin:$PATH"

https://www.postgresql.org/download/linux/ubuntu/
# sudo sh -c 'echo "deb http://apt.postgresql.org/pub/repos/apt $(lsb_release -cs)-pgdg main" > /etc/apt/sources.list.d/pgdg.list'
# wget --quiet -O - https://www.postgresql.org/media/keys/ACCC4CF8.asc | sudo apt-key add -
# sudo apt-get update
# sudo apt-get -y install postgresql

https://xdebug.org/docs/install
# sudo apt-get install php-xdebugxdebug -v

configuration postgresql: https://stackoverflow.com/questions/32439167/psql-could-not-connect-to-server-connection-refused-error-when-connecting-to


# cd /workspaces/poug/ 
Créer un utilisateur pgsql
# symfony run psql

