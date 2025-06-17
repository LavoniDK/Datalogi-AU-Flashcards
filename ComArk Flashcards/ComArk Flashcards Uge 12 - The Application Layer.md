___
#flashcards/ComArk/12_Application-Layer

## Transport Layer Basics

What is the role of the IP address in networking?::It identifies the device to which a message is delivered.
<!--SR:!2025-07-18,32,270-->

What is a port number used for?::To identify the specific application/service on a device.
<!--SR:!2025-06-21,5,233-->

What is a socket in computer networking?::A combination of an IP address and a port number.
<!--SR:!2025-07-04,18,250-->

How does the transport layer deliver messages?::IP routes to the right device; port routes to the right app; TCP/UDP determines delivery method.
<!--SR:!2025-06-20,4,220-->

Give examples of standard port numbers for protocols. ?HTTP: 80 HTTPS: 443 FTP: 21 DNS: 53 SMTP: 25

## Domain Name System (DNS)

What does DNS do?::Translates human-readable domain names into IP addresses.
<!--SR:!2025-06-21,5,236-->

What are the two main types of DNS data?::Records (e.g., A, CNAME, MX) and Protocol info (UDP, TCP).
<!--SR:!2025-06-20,4,210-->

Why is DNS considered hierarchical?::It starts at root servers, then delegates to TLDs and further down to specific domains.
<!--SR:!2025-06-21,5,233-->

What is the role of root name servers in DNS?::To provide references to TLD name servers.
<!--SR:!2025-06-20,4,210-->

Under what conditions is TCP used in DNS?::When responses are too large or DNSSEC/zone transfers are used.
<!--SR:!2025-06-21,5,233-->

## HTTP Basics

What transport protocol does HTTP use?::TCP.
<!--SR:!2025-06-18,2,213-->

What port does HTTP operate over?::Port 80 (or 443 for HTTPS).
<!--SR:!2025-06-20,4,210-->

What is the purpose of persistent connections in HTTP/1.1?::To transfer multiple files over one connection, reducing latency.
<!--SR:!2025-06-29,13,230-->

## HTTP Methods

What are common HTTP methods and their purposes? ?GET – request resource POST – submit data PUT – create/replace resource DELETE – remove resource HEAD – get headers only

Why are HTTP methods considered abstract operations?::Because their behavior is defined by the server logic, not tied to file operations.
<!--SR:!2025-06-18,2,213-->

## Cookies

Why are cookies used in HTTP?::To simulate state in a stateless protocol.
<!--SR:!2025-06-21,5,233-->

How are cookies set and returned?::Set via `Set-Cookie` header; returned only to domains that set them.
<!--SR:!2025-06-18,2,216-->

What privacy concern can cookies raise?::Cross-site tracking across multiple domains.
<!--SR:!2025-06-18,2,213-->

## Security

Why is HTTP insecure?::Data is sent in plain text, vulnerable to MITM attacks.
<!--SR:!2025-06-21,5,233-->

Why is DNS insecure?::Queries are unencrypted, enabling tracking and spoofing.
<!--SR:!2025-07-06,20,250-->

How can we secure HTTP and DNS?::Use HTTPS and DNS over HTTPS (DoH).
<!--SR:!2025-06-28,12,230-->

## Application Layer and Protocols

What is the role of the Application Layer in the OSI model?::It provides network services directly to end-user applications.
<!--SR:!2025-06-18,2,213-->

## SMTP (Simple Mail Transfer Protocol)

What does SMTP do?::It sends emails between servers and from clients to servers.
<!--SR:!2025-06-21,5,233-->

What ports does SMTP use?::Typically 25, 587, or 465 (for secure transmission).
<!--SR:!2025-06-18,2,200-->

Why is SMTP called a push protocol?::Because it can send messages but cannot retrieve them.
<!--SR:!2025-06-18,2,216-->

## FTP (File Transfer Protocol)

What is FTP used for?::Transferring files between a client and a server.
<!--SR:!2025-06-21,5,236-->

What ports are used by FTP?::Port 21 for control, Port 20 for data.
<!--SR:!2025-06-18,2,200-->

Why is traditional FTP insecure?::It sends credentials and files in plaintext.
<!--SR:!2025-06-20,4,220-->

How can FTP be secured?::Using FTPS (SSL/TLS) or SFTP (over SSH).
<!--SR:!2025-06-18,2,213-->