# HTTP Evader: Automate Firewall and IDS Evasion Tests, Analyse Browser Behavior

While HTTP is defined in RFC2616 (HTTP/1.1) the specification does not address
every tiny detail. This makes browsers behave similar for the usual HTTP
traffic, but they differ in behavior regarding unusual or invalid traffic.

The same interpretation problems can be seen in security systems, e.g.
Intrusion Detection Systems (IDS), proxies or firewalls. Thus differences in the
interpretation of HTTP leave enough room for bypassing these security
systems.

This module contains predefined tests to generate dubious HTTP responses.
The distribution contains also a script `dubious_http.pl` which can be used
as an HTTP server to serve these dubious HTTP responses. This can also be used
to automatically test a firewall for possible evasion.
Alternativly it can be used to generate pcap-Files containing the dubious HTTP
traffic, which instead of life traffic can be fed for analysis into IDS
systems.

See http://noxxi.de/research/http-evader.html for on overview of the automatic
evasion tests and http://noxxi.de/research/semantic-gap.html for more details on
using interpretation differences between different browsers and security systems 
to bypass the latter.

## Quickstart Test Server

To start a test server at localhost port 8001 simply use:

```
perl dubious_http.pl -M server --no-garble-url 127.0.0.1:8001
```

Additional options are available, i.e. for https support and others.
Start the script with `--help` to get more information.
