## scoop-customize

The "customize" bucket for [Scoop](http://scoop.sh).


### How to use?


##### Firstly, make sure installed the [Scoop](http://scoop.sh/).


Set system environment ```SCOOP``` and ```SCOOP_GLOBAL```.(Suggested)

```bash
 set-executionpolicy remotesigned -scope currentuser
 [environment]::setEnvironmentVariable('SCOOP','D:\Scoop\User','User')
 [environment]::setEnvironmentVariable('SCOOP_GLOBAL','D:\Scoop\Global','Machine')
 iex (new-object net.webclient).downloadstring('https://get.scoop.sh')
```


##### Then Add buckets.


add [scoop-extras](https://github.com/lukesampson/scoop-extras.git) and [versions](https://github.com/scoopinstaller/versions.git)

```bash
 scoop bucket add extras
 scoop bucket add versions
```

add this bucket.

```bash
 scoop bucket add customize https://github.com/ChinLong/scoop-customize.git
```


##### Finally,install apps.


```bash

 scoop install sudo 7zip git

 sudo scoop install oraclejdk scala python php nvm nodejs-lts -g
 sudo scoop install maven gradle sbt -g
 sudo scoop install docker docker-compose docker-machine -g 
 
 scoop install coreutils curl openssh grep wget
 scoop install chromium ccleaner shadowsocks notepadplusplus sublime-text lingoes
 scoop install heidisql jetbrains-toolbox jd-gui tortoisesvn zeal
 
 # make sure added customize bucket
 sudo scoop install typesafe-activator oraclejdk9 oraclejdk10 -g
 scoop install fscapture lingoes sublime-text

```