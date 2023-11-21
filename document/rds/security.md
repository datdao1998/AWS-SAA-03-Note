## Encryption
You can use Secure Socket Layer / Transport Layer Security (SSL/TLS) connections to encrypt data in transit. 
* Amazon RDS creates an SSL certificate and installs the certificate on the DB instance when the instance is provisioned. 
* For MySQL, you launch the MySQL client using the --ssl_ca parameter to reference the public key to encrypt connections. 
* Using SSL, you can encrypt a PostgreSQL connection between your applications and your PostgreSQL DB instances. You can also force all connections to your PostgreSQL DB instance to use SSL.