# tarballs-for-wsl
This repo contains:
- a Debian Trixie root-fs tarball, so you can run the DietPi installer script by yourself
- a root-fs tarball already converted to DietPi.

`/etc/wls.conf` contains

```
[boot]
systemd=true

[network]
#generateResolvConf=false

[automount]
enabled=false
```

They can be installed via PowerShell:
`wsl --import <Distro-Name> <Installaion-Path> <Archive-Path>`

e.g. `wsl --import DietPi M:\WSL M:\Downloads\root-fs.tar.xz`


On first run of the DietPi VM, the first-login installation should be triggered. 
A message will appear, that the first run setup is already running in another window, not sure where this come from. I just killed the process and run `dietpi-software` again to trigger the setup.

After that you can comment out `#generateResolvConf=false` in `/etc/wsl.conf` and set your own DNS nameserver, if you like.
