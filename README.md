Show Server Certificate Details
-------------------------------

A simple way to show the full certificate details for a server

### Usage

```
➜ show-server-cert www.google.com 443
depth=3 C = US, O = Equifax, OU = Equifax Secure Certificate Authority
verify return:1
depth=2 C = US, O = GeoTrust Inc., CN = GeoTrust Global CA
verify return:1
depth=1 C = US, O = Google Inc, CN = Google Internet Authority G2
verify return:1
depth=0 C = US, ST = California, L = Mountain View, O = Google Inc, CN = www.google.com
verify return:1
DONE
Certificate:
    Data:
        Version: 3 (0x2)
        Serial Number: 4951787825404708995 (0x44b848caa05a0883)
    Signature Algorithm: sha256WithRSAEncryption
        Issuer: C=US, O=Google Inc, CN=Google Internet Authority G2
        Validity
            Not Before: Nov 10 15:31:38 2016 GMT
            Not After : Feb  2 15:30:00 2017 GMT
        Subject: C=US, ST=California, L=Mountain View, O=Google Inc, CN=www.google.com
        Subject Public Key Info:
            Public Key Algorithm: rsaEncryption
                Public-Key: (2048 bit)
                Modulus:
                    00:97:a4:10:ac:bc:d8:d2:32:af:6c:7f:cb:fc:46:
                    2b:8c:5e:e1:0a:47:bd:82:3f:0c:f3:42:a8:cb:ea:
...
```

### Installation

This requires openssl. You can install this on a recent version of ubuntu with the following:

```bash
sudo apt-get install openssl
```

If you have [antigen](https://github.com/zsh-users/antigen) then just run the following:

```bash
antigen-bundle matthewfranglen/show-server-cert
```

Otherwise just clone this repo and add the `show-server-cert` command to the $PATH.
