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
 $env:SCOOP='D:\Scoop\User'
 $env:SCOOP_GLOBAL='D:\Scoop\Global'
 [environment]::setEnvironmentVariable('SCOOP', $env:SCOOP, 'User')
 [environment]::setEnvironmentVariable('SCOOP_GLOBAL', $env:SCOOP_GLOBAL, 'Machine')
 
 Invoke-Expression (New-Object System.Net.WebClient).DownloadString('https://get.scoop.sh') 
```

##### Then Add buckets.

add [official buckets](https://github.com/lukesampson/scoop/blob/master/buckets.json)

```bash

 scoop install sudo 7zip git

 scoop bucket add extras
 scoop bucket add versions
 scoop bucket add java
```

add this bucket.

```bash
 scoop bucket add customize https://github.com/ChinLong/scoop-customize.git
```


##### Finally,install apps.


```bash

 scoop install sudo 7zip git

 sudo scoop install openjdk oraclejdk8 -g
 sudo scoop install kotlin scala groovy python php nvm nodejs-lts -g
 sudo scoop install springboot -g
 sudo scoop install maven gradle sbt -g
 sudo scoop install docker docker-compose docker-machine -g 
 
 scoop install vcredist
 scoop install coreutils curl openssh grep wget which sed tar telnet time
 scoop install notepadplusplus notepadplusplus-pm sublime-text vscode everything
 scoop install cmder jetbrains-toolbox jd-gui tortoisesvn zeal
 scoop install chromium ccleaner shadowsocks

#scoop install aria2 qbittorrent transmission
#scoop install postgresql mysql mariadb redis sqlite heidisql
#scoop install elasticsearch kibana logstash

 scoop install fscapture lingoes dns-jumper wnmp

```