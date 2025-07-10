## Install git in rocky linux
**Follow this steps to install git in rocky linux:**

First we need to insatall build-essentail package as following step:
```bash
dnf group install "Development Tools" -y 
```
Then we need some necessary to install it:
```bash
dnf install zlib-devel openssl-devel libcurl-devel expat-devel gettext unzip cmake gcc -y
```
Now we need to download tarball of git and specefic version:
```bash
wget https://www.kernel.org/pub/software/scm/git/git-2.47.0.tar.gz
```
In this step extract git tarball az following way:
```bash
tar xvzf git-2.47.0.tar.gz 
```
Change to git directory:
```bash
cd git-2.47.0/
```
Use make command to compling and installing git from source code in speceifc path:
```bash
make prefix=/usr/local all
```
Now Executes the install target defined in the Makefile, which copies the compiled program files, libraries, and other necessary files to the system directories:
```bash
make install prefix=/usr/local
```
Check git version as following step:
```bash
git --version
```
Its show install git from source code with specefic version was successful.
