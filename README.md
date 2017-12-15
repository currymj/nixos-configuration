# Nix Configuration

This is my nix configuration. It might work for you if you have an NVIDIA
graphics card, although you may have to tweak it.  Regardless I don't think
it's a particularly cool or complicated one, this repo is mainly for me to
track changes and easily copy it to new machines. Different machines may have
tweaks on different branches.

It can be tricky using git in root-owned directories (because probably your
username/email are associated with your user account, so sudo will complain).
Probably the simplest think to do is clone this into your home dir, and then
just

```
$ cd /etc/nixos/configuration.nix
$ sudo rm configuration.nix # back it up first!
$ sudo ln /home/YOUR_USERNAME/nixos-configuration/configuration.nix # or wherever you cloned it
```

This puts a hard link in the config directory. This probably isn't the best
scheme for a multi-user system but since I only use NixOS on workstations where
I have sudo rights, it works for me.
