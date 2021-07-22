# Firewall blueprint
This package creates some common firewall rules that are managed with Config Controller. The firewall rules created include:

- allow ssh and https for management
- allow common ports between private IP ranges
- allow common ports from GCP load balancer ranges


Contents:
- ingress
    - allow-mgmt.yaml - creates a firewall rule that allows BIG-IP Mgmt traffic (ssh and BIG-IP's WEBUI)
    - allow-vip.yaml - creates a firewall rule that allow traffic to BIG-IP Virtual Services
    - allow-internal-common.yaml - creates a firewall rule that allows SSH, SSL, HTTP (8080), and ICMP traffic on all RFC1918 ranges
    - allow-gcp-lb.yaml - creates a firewall rule that allows traffic from GCP load balancer ranges for health check and proxy traffic on ports 80, 443, and 8080
- egress
    - allow-google-apis.yaml - creates a firewall rule that allows traffic to private.googleapis.com IP range
    - deny-all.yaml - creates a firewall rule that denys all egress traffic on TCP/UDP. It is recommended that if this rule is enabled, to also enable the "allow-google-apis" rule.

