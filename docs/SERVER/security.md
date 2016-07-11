# Security

**Table of Contents**

[TOC]

## Overview

Securing your services & applications over HTTPS (SSL) is highly important to make sure your content is private between client & server.

## Credentials over HTTP vs. SSL

Typical applications will initially request a token from the server for authentication. To do such request, the application needs to send a combination of Username/Password to the server. Users only wants to share their credentials with the server and no one else. Unauthorized intruders have the ability to intercept network traffic between servers and clients. Here are examples of data being intercepted by a [man in the middle](#man-in-the-middle) attack.

### Credentials over HTTP

Performing a POST with Basic Authorization over an un-secure connection we can easily intercept the client's username (JohnSmith) & password (12345678).

```http
Hypertext Transfer Protocol
  POST /token HTTP/1.1
  HOST: localhost:8080
  Connection: keep-alive
  Content-Length: 269
  Content-Type: multipart/form-data
  Authorization: Basic Sm9oblNtaXRoOjEyMzQ1Njc4
    Credentials: JohnSmith:12345678
```

### Credentials over SSL

When we performed the same POST with Basic Authorization we were enable to intercept any content from the HTTP headers. The only data visible from the intercepted packet is encrypted.

```http
Secure Sockets Layer
  TLSv1.2 Record Layer: Application Data Protocol: http
  Content Type: Application Data (23)
  Version: TLS 1.2 (0x0303)
  Length: 620
  Encrypted Application Data: 09b24c93d51714a77fb77687c761ca1d3c1a75d9a680dc6...
```

## Man in the Middle (MITM) Attacks

This term is commonly used in the cyber security community and can be described as a malicious/spying attack on your network. In this type of attack, someone is "listening" to the traffic between the browser and the server. The most common MITM happens at Internet cafes, by listening to the WiFi.

## Extended Validation Certificates

- https://blogs.technet.microsoft.com/askds/2009/08/14/extended-validation-support-for-websites-using-internal-certificates/

## TLS 1.2

Content
