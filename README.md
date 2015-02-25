docker_tls_gen
==============

Generates server and client TLS certs for use with Docker

You must have a CA cert and key in the same directory the script is run.

To generate the CA cert/key:

    openssl genrsa -aes256 -out CA.key 2048 
    openssl req -new -x509 -days 365 -key CA.key -sha256 -out CA.crt
    chmod -v 0400 CA.key 
    chmod -v 0444 CA.crt
