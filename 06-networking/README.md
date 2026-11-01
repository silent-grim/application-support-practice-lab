# Module 06 — Networking & Connectivity

**Status:** Theory Completed — Practical Lab Pending

## 1. Learning Objectives

Understand the fundamentals of network communication and develop the ability to investigate connectivity issues affecting applications and web portals.

Topics covered:

- TCP/IP networking model
- OSI model and network encapsulation
- IP addressing and private IP ranges
- DNS resolution
- Default gateway and routing
- TCP vs UDP
- Common network ports and protocols
- TCP connection establishment
- TLS and HTTPS communication
- HTTP request-response lifecycle
- HTTP methods and status codes
- Application gateway and upstream connectivity

## 2. Networking Fundamentals

### TCP/IP Model

Studied the five-layer TCP/IP model:

1. Application
2. Transport
3. Internet
4. Data Link
5. Physical

Covered the relationship between the TCP/IP and OSI models, along with encapsulation and decapsulation during network communication.

### IP Addressing and Routing

Topics covered:

- IPv4 addressing
- Private and public IP addresses
- Subnet mask
- Default gateway
- Routing fundamentals
- Local network vs external network communication

### DNS

**Domain Name System (DNS)** translates hostnames into IP addresses.

Investigation concepts:

- DNS resolution
- DNS server responses
- Successful resolution vs unsuccessful resolution
- DNS-related application access failures

### TCP and UDP

**TCP:**
- Connection-oriented communication
- Three-way handshake
- Reliable and ordered delivery
- Acknowledgements and retransmissions

**UDP:**
- Connectionless communication
- No built-in delivery guarantee
- No TCP-style handshake

### Common Network Ports

| Port | Protocol / Service |
|---|---|
| 22 | SSH |
| 53 | DNS |
| 80 | HTTP |
| 443 | HTTPS |
| 3306 | MySQL |
| 3389 | RDP |
| 5432 | PostgreSQL |

## 3. TLS, HTTPS and HTTP

### TLS Fundamentals

Covered:

- Encryption
- Data integrity
- Server authentication
- Digital certificates
- Certificate validation
- Simplified TLS handshake

### HTTP and HTTPS

Studied the HTTP request-response model.

HTTP methods:

- GET
- POST
- PUT
- PATCH
- DELETE

HTTP status code categories:

- 1xx — Informational
- 2xx — Success
- 3xx — Redirection
- 4xx — Client or request errors
- 5xx — Server-side or gateway errors

Important status codes:

| Status | Meaning |
|---|---|
| 200 | OK |
| 201 | Created |
| 301 | Moved Permanently |
| 302 | Found |
| 400 | Bad Request |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |
| 429 | Too Many Requests |
| 500 | Internal Server Error |
| 502 | Bad Gateway |
| 503 | Service Unavailable |
| 504 | Gateway Timeout |

## 4. Windows Troubleshooting Command Reference

### IP Configuration

| Command | Purpose |
|---|---|
| `ipconfig` | Display basic IP configuration |
| `ipconfig /all` | Display detailed network configuration |
| `ipconfig /release` | Release DHCP-assigned IPv4 configuration |
| `ipconfig /renew` | Request a new DHCP configuration |
| `ipconfig /flushdns` | Clear the local DNS resolver cache |

### DNS Investigation

| Command | Purpose |
|---|---|
| `nslookup google.com` | Query DNS for a hostname |
| `nslookup -type=A google.com` | Query IPv4 address records |
| `nslookup -type=AAAA google.com` | Query IPv6 address records |
| `Resolve-DnsName google.com` | Resolve DNS using PowerShell |

### Connectivity and Routing

| Command | Purpose |
|---|---|
| `ping google.com` | Test ICMP reachability |
| `tracert google.com` | Display the route towards a destination |
| `route print` | Display the local routing table |
| `arp -a` | Display the ARP cache |

### TCP Port Testing

| Command | Purpose |
|---|---|
| `Test-NetConnection google.com -Port 443` | Test TCP connectivity to port 443 |
| `Test-NetConnection google.com -Port 80` | Test TCP connectivity to port 80 |

Important output:

`TcpTestSucceeded : True`

Indicates that a TCP connection to the specified destination port succeeded. It does not confirm that TLS, HTTP or the application itself is functioning correctly.

### HTTP and TLS Investigation

| Command | Purpose |
|---|---|
| `curl.exe -I https://google.com` | Inspect HTTP response headers using HEAD |
| `curl.exe -v https://google.com` | Display verbose connection, TLS and HTTP information |
| `curl.exe -Iv https://google.com` | Inspect verbose connection details using HEAD |

### Service and Port Investigation

| Command | Purpose |
|---|---|
| `Get-Service` | List Windows services |
| `Get-Service -Name "ServiceName"` | Check a specific service |
| `Get-NetTCPConnection` | Display TCP connection information |
| `netstat -ano` | Display active connections and listening ports |
| `netstat -ano \| findstr :8000` | Filter connections involving port 8000 |

## 5. Troubleshooting Methodology

A structured approach to investigating application connectivity:

1. Identify the affected users and application.
2. Check local IP configuration.
3. Verify DNS resolution.
4. Investigate network reachability and routing.
5. Test the required TCP port.
6. Verify TLS and certificate validation.
7. Inspect the HTTP response.
8. Investigate application and upstream dependencies.
9. Collect evidence and correlate logs.
10. Verify recovery after corrective action.

### Important Distinctions

**DNS success does not guarantee TCP connectivity.**

A hostname may resolve correctly while the destination port remains inaccessible.

**Ping failure does not automatically mean a server is down.**

ICMP traffic may be blocked while TCP connectivity remains available.

**TCP success does not guarantee application health.**

The TCP connection may succeed while TLS validation, HTTP requests or backend processing fail.

**HTTP 502 does not automatically identify the root cause.**

Investigate the gateway, upstream application, connectivity and relevant backend logs.

## 6. Practical Troubleshooting Scenarios

### Scenario 1 — DNS Resolution

A user cannot access an application through its hostname.

Investigation:
- Check local network configuration.
- Query DNS using `nslookup`.
- Examine the returned IP address or DNS error.
- Compare results with the expected hostname resolution.

### Scenario 2 — ICMP Failure with TCP Success

Ping requests time out, but `Test-NetConnection` to port 443 succeeds.

Finding:

ICMP failure alone does not establish that the destination is unavailable. Continue investigating TLS and HTTP.

### Scenario 3 — HTTP 502 Bad Gateway

The application hostname resolves, TCP 443 succeeds, TLS validation passes, but the HTTP response is 502.

Investigation:
- Examine gateway logs.
- Identify the configured upstream.
- Check upstream application availability.
- Correlate gateway and application logs.
- Investigate recent configuration changes or deployments.

### Scenario 4 — Upstream Connection Refused

Gateway logs indicate that a connection to the application on port 8000 was refused.

Investigation:
- Check whether the application service is running.
- Verify that it is listening on port 8000.
- Check the listening interface and upstream configuration.
- Investigate recent deployments, configuration changes and service failures.

## 7. Practical Lab — Pending

The following exercises remain to be performed on Windows:

- [ ] Inspect local IP configuration using `ipconfig`.
- [ ] Examine detailed network settings using `ipconfig /all`.
- [ ] Perform DNS queries using `nslookup`.
- [ ] Test ICMP reachability using `ping`.
- [ ] Inspect routing using `tracert` and `route print`.
- [ ] Test TCP connectivity using `Test-NetConnection`.
- [ ] Inspect HTTP and TLS responses using `curl.exe`.
- [ ] Investigate Windows services and listening ports.
- [ ] Document command outputs and investigation findings.

## 8. Learning Outcomes

- Understand the basic flow of network communication.
- Differentiate DNS resolution, routing, TCP connectivity, TLS validation and HTTP responses.
- Interpret common connectivity and application errors.
- Identify when an issue requires investigation at the gateway, network or application layer.
- Apply a structured troubleshooting approach before escalating an incident.

## 9. Completion Criteria

This module will be marked completed after the practical Windows exercises have been performed, results interpreted and findings documented.

---

**Note:** This is a simulated learning and practice module. It does not represent production infrastructure administration experience.
