# Lessons Learned

## Documentation matters more than memory.<br>
I've learned that documenting changes, ports, DNS records and deployment configurations saves significant troubleshooting time later.

## Logs usually tell you what's wrong.<br>
Most problems were solved by reviewing:<br>
<br>
- Docker logs
- Nginx logs
- Application logs

before making configuration changes.

## DNS causes more issues than expected.<br>
Many accessibility issues were ultimately related to DNS records, propagation delays or caching.

## Security should be considered from the beginning.
Reducing exposed services and using VPN access significantly improves security compared with exposing everything publicly.

## AI accelerates implementation but not understanding.
AI tools can generate configurations and code quickly, but successful deployment still requires validation, testing and troubleshooting by the operator.

## Docker Networking

Initially I had some difficulties understanding container networking and service communication.

Through troubleshooting I learned and gained exposure to:

- Docker bridge networking
- Port mappings
- Service discovery
- Container isolation

## SSL Certificates

Improved understanding on the relationship between:

- DNS
- Domain ownership
- Certificate issuance
- HTTPS encryption
