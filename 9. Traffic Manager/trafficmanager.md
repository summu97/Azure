Lets say you have deployed web-servers in different locations like one in india and other in dubai then to route traffic in between these servers a traffic manager can be used.
Traffic Manager: DNS based traffic load-balancer. Just like Route53 in AWS.
--
* It is created as a policy not as load-balancer.
* Traffic manager works at global level.

Has 6 types of policies:
--
* Priority: To send max requests to high priority DNS endpoint.
* Weighted: When want to distribute traffic to endpoints weighted. Ex: 60%, 30% 10%
* Performance: Have endpoints in different locations & want your end user to use closest endpoint.
* Geographic: Indian users to India endpoint.
* Multi-value: Can have IPv4/IPv6 addresses as endpoint.
* Subnet: We can define a range of IP's to forward traffic to endpoint.


Real user measurement: end to end info of users who access the website.
--
