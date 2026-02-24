# Objective: installation of a reverse proxy to protect a Web server

Here is what you will learn:
- installation a reverse proxy with Caddy
- filtering URL so that not all unexpected traffic reaches the Web server
- filtering client IP addresses
- validation the protection of your Web server with tcpdump

# Why use a reverse proxy?

A reverse proxy is an intermediary server between a computer network and a server (most often a web server, but not exclusively). To do this, the reverse proxy creates two connections each time: one between itself and the web server, and another between itself and the remote equipment. Thus, during an attack targeting the web server, it is not the web server that is exposed, but rather the reverse proxy, which absorbs the attack instead.

A reverse proxy is useful for a web server because it improves:
- Security: HTTP requests don't go directly to the web server but are filtered by their URL beforehand. The reverse proxy can also block some IP addresses, just like a firewall.
- Performance: The web server isn't overloaded with unnecessary or malicious requests.

