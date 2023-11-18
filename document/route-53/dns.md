# Domain Name System (DNS) concepts
## Routing Policy
* **Simple routing policy** – Use to route internet traffic to a single resource that performs a given function for your domain, for example, a web server that serves content for the example.com website.
* **Failover routing policy** – Use when you want to configure active-passive failover.
* **Geolocation routing policy** – Use when you want to route internet traffic to your resources based on the location of your users.
* **Geoproximity routing policy** – Use when you want to route traffic based on the location of your resources and, optionally, shift traffic from resources in one location to resources in another.
* **Latency routing policy** – Use when you have resources in multiple locations and you want to route traffic to the resource that provides the best latency.
8 IP-based routing policy – Use when you want to route traffic based on the location of your users, and have the IP addresses that the traffic originates from.
* **Multivalue answer routing policy** – Use when you want Route 53 to respond to DNS queries with up to eight healthy records selected at random.
* **Weighted routing policy** – Use to route traffic to multiple resources in proportions that you specify.

# DNS Record
## A Record
You use an A record to route traffic to a resource, such as a web server, using an IPv4 address in dotted decimal notation.

## AAAA record type
You use an AAAA record to route traffic to a resource, such as a web server, using an IPv6 address in colon-separated hexadecimal format.

## CNAME record type
* A CNAME record maps DNS queries for the name of the current record, such as acme.example.com, to another domain (example.com or example.net) or subdomain (acme.example.com or zenith.example.org).
* Amazon Route 53 also supports alias records, which allow you to route queries to selected AWS resources, such as CloudFront distributions and Amazon S3 buckets.