
Edit conf/config.py and sql/data.sql change at least:

CENTRAL_WALLET - DIGI address

COINDAEMON_TRUSTED_USER - DIGI rpc user

COINDAEMON_TRUSTED_PASSWORD - DIGI rpc password

DB_MYSQL_PASS to match password in sql/data.sql file.

On Debian:

apt-get install git mysql-server python python-twisted python-mysqldb python-pylibmc memchached python-pip python-simplejson

./update_submodules

pip install stratum

mysql -u root -p <sql/data.sql

twistd -ny launcher.tac
