# Common Issues and Resolutions

## SSL Certificate Failure

**Issue:**<br>
Certificate failed to issue. (e.g when using certbot)

**Cause:**<br>
DNS record had not fully propagated.

**Resolution:**<br>
Verified DNS configuration and waited for propagation before reissuing certificate.

**How to check and verify DNS has propogated:**<br>
Various console commmands if required but for simplicity and ease I used [WhatsMyDNS](https://whatsmydns.net/) & [DNSDumpster](https://dnsdumpster.com/)

---

## 502 Bad Gateway

**Issue:**<br>
Reverse proxy returned 502.

**Cause:**<br>
Backend container stopped responding.<br>

**Resolution:**
Checked container status using Docker.<br>
```docker ps -a | grep -v Exited | cut -c1-$COLUMNS```

Reviewed logs.<br>
```docker logs --since=Xh <container id>```

Restarted container.<br>
```docker start my_container```

Verified service availability.

---

## DNS resolution failure

**Problem:**<br>
Clients unable to access service via hostname.

**Cause:**<br>
Incorrect DNS record.

**Resolution:**<br>
Verified A record<br>
Checked propagation<br>
Flushed DNS cache<br>
Tested resolution

**Outcome:**<br>
Service accessible.

---

## Docker container repeatedly crashing

*Problem:**<br>
Service continuously restarting.

**Cause:**<br>
Incorrect environment variable.

**Resolution:**<br>
Reviewed container logs<br>
Corrected configuration<br>
Redeployed service

**Outcome:**<br>
Stable operation restored.

---

## WireGuard VPN connectivity issue

**Problem:**<br>
Unable to access internal services remotely.

**Cause:**<br>
Incorrect peer configuration.

**Resolution:**<br>
Reviewed WireGuard configuration<br>
Verified routes<br>
Tested DNS resolution through VPN

**Outcome:**<br>
Remote access restored.
