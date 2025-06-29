I know, a lot of you must have faced the problem with Stremio installation in Ubuntu 24.04 LTS.
After going through it elaborately, I now know why it happens.
The main reason is, Ubuntu 24.04 does not uses (and does not identifies) ```libmpv1```
The way around is to simply create another .deb file from the original stremio deb, and change the dependencies. To do so, just run the script.

```
chmod +x ./install_stremio.sh
./install_stremio.sh
```

Also, you can run the following ```wget``` command:
```
wget -O - https://raw.githubusercontent.com/Kabir5296/Stremio-Ubuntu24.04-Fix/refs/heads/main/install_stremio.sh | bash
```