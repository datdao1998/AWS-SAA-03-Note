# Optimizing caching and availability
## Improve cache hit ratio
* Using Origin Shield
* Caching based on query string parameters
* Caching based on cookie values
* Caching based on request headers
* Remove Accept-Encoding header when compression is not needed
* Serving media content by using HTTP

## Optimizing high availability with CloudFront origin failover
* You can set up CloudFront with origin failover for scenarios that require high availability. To get started, you create an origin group with two origins: a primary and a secondary. If the primary origin is unavailable, or returns specific HTTP response status codes that indicate a failure, CloudFront automatically switches to the secondary origin.
* To set up origin failover, you must have a distribution with at least two origins. Next, you create an origin group for your distribution that includes two origins, setting one as the primary. Finally, you create or update a cache behavior to use the origin group.


# Configuring secure access and restricting access to content
Using field-level encryption to help protect sensitive data
* With Amazon CloudFront, you can enforce secure end-to-end connections to origin servers by using HTTPS. Field-level encryption adds an additional layer of security that lets you protect specific data throughout system processing so that only certain applications can see it.
* Field-level encryption allows you to enable your users to securely upload sensitive information to your web servers. The sensitive information provided by your users is encrypted at the edge, close to the user, and remains encrypted throughout your entire application stack. This encryption ensures that only applications that need the data—and have the credentials to decrypt it—are able to do so.





