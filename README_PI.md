# Readme for installing on Raspberry Pi

## Getting Started

Install Git
```
apt install git
```

Install Go

```
wget https://golang.org/dl/go1.15.3.linux-armv6l.tar.gz
tar xvzf go1.15.3.linux-armv6l.tar.gz
mv go /usr/local/
echo '' >> ~/.profile
echo 'export GOPATH=$HOME/go' >> ~/.profile
echo 'export PATH=/usr/local/go/bin:$PATH:$GOPATH/bin' >> ~/.profile
source ~/.profile
```

Download Rice

```
go get github.com/GeertJohan/go.rice
go get github.com/GeertJohan/go.rice/rice
```

Download main sources

```
go get github.com/rob121/broadlinkgo
cd src/github.com/rob121/broadlinkgo/cmd
rice embed-go
go build -o broadlinkgo
```

