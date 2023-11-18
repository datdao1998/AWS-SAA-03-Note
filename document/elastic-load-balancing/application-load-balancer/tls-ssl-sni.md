## TLS
TLS is a protocol for securely transmitting data like passwords, cookies, and credit card numbers. 

It enables privacy, authentication, and integrity of the data being transmitted. 
* TLS uses certificate based authentication where certificates are like ID cards for your websites. 
* You trust the person that signed and issued the certificate, the certificate authority (CA), so you trust that the data in the certificate is correct. 

## SNI
With SNI support we’re making it easy to use more than one certificate with the same ALB. 

The most common reason you might want to use multiple certificates is to handle different domains with the same load balancer.