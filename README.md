[![Build Status](https://travis-ci.org/JDCnPlatform/jdcn.svg?branch=master)](https://travis-ci.org/JDCnPlatform/jdcn)
[![Author](https://img.shields.io/badge/author-@JDCnPlatform-blue.svg?style=flat)](http://github.com/JDCnPlatform) 
[![License](https://img.shields.io/badge/license-MIT-yellow.svg?style=flat)](http://jdcnplatform.mit-license.org)
[![Platform](https://img.shields.io/badge/platform-Linux-green.svg?style=flat)](https://github.com/JDCnPlatform/jdcn)
- - -

# JDCn

JDCn system is a decentralized application platform, which is designed to lower the threshold for developers, such as using JavaScript as develop language, supporting relational database to save transaction data, and making DAPP development be similar with traditional Web application. It is sure that these characteristics are very attractive to developers and SMEs. The ecosystem of the whole platform cannot be improved until developers make a huge progress on productivity. Also, JDCn platform is designed to be open for various fields, not limited to some particular parts such as finance, file storage, or copyright proof. It provides underlying and abstract API which can be combined freely to create different types of applications. In consensus mechanism, JDCn inherits and enhances DPOS algorithm, by which the possibility of forks and risk of duplicate payments would be significantly reduced. Furthermore, JDCn sidechain mode not only can mitigate the pressure of blockchain expansion, but also make DAPP more flexible and personal. JDCn system, as a proactive, low-cost and full stack solution, will surely be a next generation incubator of decentralized applications.

More infomation please visit


+ [official website](https://www.jdcn.io)
+ online wallet: [wallet.jdcn.io](https://wallet.jdcn.io/), [wallet.jdcn.cn](https://wallet.jdcn.cn/)

## System Dependency

- nodejs v6.3+
- npm 3.10+ (not cnpm)
- node-gyp v3.6.2+ (suggested)
- sqlite v3.8.2+
- g++
- libssl

## Installation for ubuntu 14.04.x or higher.

```
# Install dependency package
sudo apt-get install curl sqlite3 ntp wget git libssl-dev openssl make gcc g++ autoconf automake python build-essential -y
# libsodium for ubuntu 14.04
sudo apt-get install libtool -y
# libsodium for ubuntu 16.04
sudo apt-get install libtool libtool-bin -y

# Install nvm
curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.33.2/install.sh | bash
# This loads nvm
export NVM_DIR="$HOME/.nvm"
[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh" 
[ -s "$NVM_DIR/bash_completion" ] && \. "$NVM_DIR/bash_completion"  # This loads nvm bash_completion

# Install node and npm for current user.
nvm install v8
# check node version and it should be v8.x.x
node --version

# git clone sourece code
git clone https://github.com/JDCnPlatform/jdcn && cd jdcn && chmod u+x jdcnd

# Install node packages
npm install
```

## Web Wallet

```
cd public/

npm install bower -g
npm install browserify -g
npm install gulp  -g

npm install
# angular chose "angular#~1.5.3 which resolved to 1.5.11 and is required by ASCH"
bower install

npm run build
gulp build-test #This make the front-end files in public dir.
```

## Installation on docker.

[Please install Docker firstly](https://store.docker.com/search?offering=community&type=edition)

```
# pull jdcn code docker image
docker pull jdcnplatform/jdcn:v1.3.0
# run docker and jdcn
docker run -i -t --name jdcn1.3.0 -p 4096:4096 jdcnplatform/jdcn:v1.3.0 /bin/bash
root@e149b6732a48:/# cd /data/jdcn && ./jdcnd start
JDCn server started as daemon ...
```

## Run 

```
cd jdcn && node app.js
or
cd jdcn && ./jdcnd start
```
Then you can open ```http://localhost:4096``` in you browser.

## Usage

```
node app.js --help

  Usage: app [options]

  Options:

    -h, --help                 output usage information
    -V, --version              output the version number
    -c, --config <path>        Config file path
    -p, --port <port>          Listening port number
    -a, --address <ip>         Listening host name or ip
    -b, --blockchain <path>    Blockchain db path
    -g, --genesisblock <path>  Genesisblock path
    -x, --peers [peers...]     Peers list
    -l, --log <level>          Log level
    -d, --daemon               Run jdcn node as daemon
    --reindex                  Reindex blockchain
    --base <dir>               Base directory
```

## Default localnet genesis account

```
// This is the genesis account of localnet and one hundred million XAS in it.
{
  "keypair": {
    "publicKey": "8065a105c785a08757727fded3a06f8f312e73ad40f1f3502e0232ea42e67efd",
    "privateKey": "a64af28537545301f66579604628b55c7a7a102752bbd8f0b0d152f9754e78d58065a105c785a08757727fded3a06f8f312e73ad40f1f3502e0232ea42e67efd"
  },
  "address": "14762548536863074694",
  "secret": "someone manual strong movie roof episode eight spatial brown soldier soup motor" // password
}
```

## Releated projects

- [jdcn-docs](https://github.com/JDCnPlatform/jdcn/tree/master/docs)
- [jdcn-cli](https://github.com/JDCnPlatform/jdcn-cli)
- [jdcn-js](https://github.com/JDCnPlatform/jdcn-js)
- [jdcn-sandbox](https://github.com/JDCnPlatform/jdcn-sandbox-dist)
- [jdcn-explorer] website: [explorer.jdcn.io/](https://explorer.jdcn.io/)

## License

The MIT License (MIT)

Copyright (c) 2018 JDCn
Copyright (c) 2016-2018 JDCn
Copyright (c) 2015 Crypti

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

[jdcn-explorer]:https://explorer.jdcn.io/
