# aports

alpine linux  nftables fullcone support

# repo

https://repo.tlle.eu.org

# credit
https://github.com/fullcone-nat-nftables

# setup repo and install glibc
```
echo 'https://repo.tlle.eu.org/alpine/v3.20/main' | sudo tee -a /etc/apk/repositories
wget https://repo.tlle.eu.org/alpine/v3.20/main/x86_64/ruaue-keys-1-r0.apk
doas sh -c '
apk add --allow-untrusted ./sevmonster-keys-1-r0.apk
apk update \
    && apk add gcompat \
    && rm /lib/ld-linux-x86-64.so.2 \
    && apk add --force-overwrite glibc \
    && apk add glibc-bin'
```
