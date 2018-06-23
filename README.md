## scoop-customize

The "customize" bucket for [Scoop](http://scoop.sh).

---

### How to use?


##### Firstly, make sure installed the [Scoop](http://scoop.sh/).

Make sure you have PowerShell 3 or later installed. If you're on Windows 10 or Windows Server 2012 you should be all set, but Windows 7 and Windows Server 2008 might have older versions. Download [powershell3.0](https://www.microsoft.com/en-us/download/details.aspx?id=34595) or [powershell4.0](https://www.microsoft.com/en-us/download/details.aspx?id=40855).

```bash
 $psversiontable.psversion.major # should be >= 3
```

Set system environment ```SCOOP``` and ```SCOOP_GLOBAL```.(Suggested)

```bash
 set-executionpolicy remotesigned -scope currentuser
 [environment]::setEnvironmentVariable('SCOOP','D:\Scoop\User','User')
 [environment]::setEnvironmentVariable('SCOOP_GLOBAL','D:\Scoop\Global','Machine')
 iex (new-object net.webclient).downloadstring('https://get.scoop.sh')
```

##### Then Add buckets.

add [official buckets](https://github.com/lukesampson/scoop/blob/master/buckets.json)

```bash

 scoop install sudo 7zip git

 scoop bucket add extras
 scoop bucket add versions
 scoop bucket add nightlies
 scoop bucket add nirsoft
 scoop bucket add nerd-fonts
 scoop bucket add nonportable
 scoop bucket add java
```

add this bucket.

```bash
 scoop bucket add customize https://github.com/ChinLong/scoop-customize.git
```


##### Finally,install apps.


```bash

 scoop install sudo 7zip git

 sudo scoop install oraclejdk oraclejdk11 oraclejdk10 oraclejdk8 -g
 sudo scoop install kotlin scala groovy python php nvm nodejs-lts -g
 sudo scoop install springboot -g
 sudo scoop install maven gradle sbt -g
 sudo scoop install docker docker-compose docker-machine -g 
 
 scoop install vcredist
 scoop install coreutils curl openssh grep wget which sed tar telnet time
 scoop install notepadplusplus notepadplusplus-pm sublime-text vscode everything
 scoop install cmder heidisql jetbrains-toolbox jd-gui tortoisesvn zeal
 scoop install chromium ccleaner shadowsocks

#scoop install putty winscp
#scoop install aria2 qbittorrent transmission
#scoop install postgresql mariadb redis sqlite
#scoop install elasticsearch kibana logstash

 # make sure added customize bucket
 sudo scoop install typesafe-activator -g
 scoop install fscapture lingoes dns-jumper wnmp

```