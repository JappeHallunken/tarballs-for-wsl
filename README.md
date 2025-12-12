# tarballs-for-wsl
A Debian Trixie root-fs tarball and another converted to DietPi for WSL

`/etc/wls.conf` contains

```
[boot]
systemd=true

[network]
generateResolvConf=false

[automount]
enabled=false
```

They can be installed via PowerShell:
`wsl --import <Distro-Name> <Installaion-Path> <Archive-Path>`

e.g. `wsl --import DietPi M:\WSL M:\Downloads\root-fs.tar.xz`


On first run of the DietPi VM, the first-login installation should be triggered.
