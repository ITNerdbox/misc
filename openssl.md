## Supporting SSLv2 and SSLv3

For security testing purposes it may come in handy to manually check whether a server is configured with SSLv2 and/or SSLv3. 
As the latest versions of OpenSSL do no longer support them, an older version of OpenSSL can be compiled with these protocols.

```bash
wget https://openssl.org/source/openssl-1.0.2k.tar.gz
tar -xvf openssl-1.0.2k.tar.gz
cd openssl-1.0.2k/
./config enable-ssl2 enable-ssl3 no-shared
make depend
make
```
Once done compiling, the openssl binary can be found in ```apps/```. Rename the binary to ```openssl23``` and copy it to ```/usr/bin```.
