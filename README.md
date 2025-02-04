![Repo Build Status](https://img.shields.io/github/actions/workflow/status/zaggash/archlinux-aur/schedule-full_build_repo.yaml?label=REPO%20BUILD&logo=archlinux&logoColor=white&style=for-the-badge)
![Renovate](https://img.shields.io/github/actions/workflow/status/zaggash/archlinux-aur/schedule-renovate.yaml?label=renovate&logo=RenovateBot&logoColor=white&style=for-the-badge)


## My Archlinux repo
This is an unofficial repository for Arch Linux.  
Originaly intended to fit my needs and build custom or unavailable packages.

### How to use it
- Trust my public key:
```
pacman-key --init
curl -sL 'https://keybase.io/apinon/pgp_keys.asc?fingerprint=54231a262e8bf5501c6945d275bcc090ca185c57' | sudo pacman-key -a -
pacman-key --lsign-key 54231a262e8bf5501c6945d275bcc090ca185c57
```

- Edit `/etc/pacman.conf` with:
```
[archlinux-aur]
Server = https://github.com/zaggash/$repo/releases/download/$arch
SigLevel = Required
```

- Then update the DB:
```
pacman -Syy
```
