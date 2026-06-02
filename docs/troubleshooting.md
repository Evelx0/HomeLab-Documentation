# Common Issues and Resolutions

## SSL Certificate Failure

Issue:
Certificate failed to issue. (e.g when using certbot)

Cause:
DNS record had not fully propagated.

Resolution:
Verified DNS configuration and waited for propagation before reissuing certificate.

How to check and verify DNS has propogated:
Various console commmands if required but for simplicity and ease I used [WhatsMyDNS](https://whatsmydns.net/) & [DNSDumpster](https://dnsdumpster.com/)

---

## 502 Bad Gateway

Issue:
Reverse proxy returned 502.

Cause:
Backend container stopped responding.
SSH via Termius

Resolution:
Checked container status using Docker.<br>
```docker ps -a | grep -v Exited | cut -c1-$COLUMNS```

Reviewed logs.<br>
```docker logs --since=Xh <container id>```

Restarted container.<br>
```docker start my_container```

Verified service availability.

---
