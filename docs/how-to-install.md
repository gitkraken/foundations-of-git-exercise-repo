---

title: How to Install GitKraken Client 
description: No Git tools are required for GitKraken Client, so once you’ve run the installer, you can open the app and get going.

---

There are three steps to success with GitKraken Client. That's it!

1. [Download](https://gitkraken.com/download) GitKraken Client
2. Install GitKraken Client
3. Use GitKraken Client

No Git tools are required for GitKraken Client, so once you’ve run the installer, you can open the app and get going.

It works directly with your repositories with no dependencies—you don’t even need to have Git installed on your system. GitKraken Client is built with NodeGit, a Git framework that is primarily developed and maintained by members of the GitKraken development team.

Below are platform-specific details on minimum requirements.

<div class='callout callout--basic'>
    <p>Looking for <em>GitKraken Enterprise</em> installation instructions? Then please start in with our <a href="/enterprise/system-requirements">Enterprise System Requirements</a> page. </p>
</div>

***
## Windows (.exe file)
* **System requirements:** Windows 10
* [Download (64-bit)](https://gitkraken.com/download/windows64)
* [Download (32-bit)](https://gitkraken.com/download/windows)

### Install Instructions
Double-click the downloaded executable file, and follow the installation instructions.

### Data Location
GitKraken Client data is stored with your home profile in `C:\Users\{user}\AppData\Roaming` in the `.gitkraken` folder.

***
## Mac OS (.dmg file)
* **System requirements:** Mac OS X 10.11+
* [Download](https://gitkraken.com/download/mac)

### Install Instructions
Double click the downloaded DMG file and when prompted, drag and drop the GitKraken icon to your Applications folder.

<img src="/img/documentation/how-to-install/mac-install.png" class="img-responsive center">

### Data Location
GitKraken Client data is stored in `/Users/{user}/.gitkraken` == `~/.gitkraken`.

***
## Linux (.deb, .rpm, and .tar.gz files)
* **.deb system requirements:** Ubuntu 18.04 LTS or later
* **.rpm system requirements:** RHEL 7+, CentOS 7+, or Fedora 34+

<div class='callout callout--warning'>
    <p>Note 📝 - GitKraken Client currently supports Ubuntu 18.04 LTS+, RHEL 7+, CentOS 7+, and Fedora 34+. While GitKraken Client may be able to be installed on other Linux distributions, we cannot guarantee that it will work as expected.</p>
</div>

### .deb
GitKraken Client has a simple package available for Debian based distributions.
```
wget https://release.gitkraken.com/linux/gitkraken-amd64.deb
sudo dpkg -i gitkraken-amd64.deb
```
Or [download the file](https://gitkraken.com/download/linux-deb).

### .tar
```
wget https://release.gitkraken.com/linux/gitkraken-amd64.tar.gz
sudo tar -xvzf gitkraken-amd64.tar.gz
```
Or [download the file](https://gitkraken.com/download/linux-gzip).

### .rpm
```
wget https://release.gitkraken.com/linux/gitkraken-amd64.rpm
sudo yum install ./gitkraken-amd64.rpm
```
Or [download the file](https://gitkraken.com/download/linux-rpm).

### Snap

Snap is an easy-to-install package for Linux distributions (supported versions above). Get it from the snap store or [Snapcraft.io](https://snapcraft.io/gitkraken).

### Data Location
GitKraken Client data is stored in `/home/{user}/.gitkraken` == `~/.gitkraken`.

## Run GitKraken Client

Upon installation, some Linux distros do not automatically create shortcuts to the app.

To run GitKraken Client manually, open the terminal and type `gitkraken` to start the app.

