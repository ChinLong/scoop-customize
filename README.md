## scoop-customize

The "customize" bucket for [Scoop](http://scoop.sh).

---

### How to use?


##### Firstly, make sure installed the [Scoop](http://scoop.sh/).

Make sure you have PowerShell 5(or later) and .NET Framework 4.5 (or later) installed. 
If you do not have, please download. 
Download lastest [PowerShell](https://docs.microsoft.com/en-us/powershell/) and [.NET Framework](https://dotnet.microsoft.com/download).

```bash
 $psversiontable.psversion.major # should be >= 5.0
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
 scoop install sudo
 sudo scoop install 7zip openssh git --global
 scoop bucket add extras
 scoop bucket add versions
 scoop bucket add java
 scoop bucket add nonportable
 scoop bucket add nirsoft
 scoop bucket add php
```

add this bucket.

```bash
 scoop bucket add customize https://github.com/ChinLong/scoop-customize.git
```


##### Finally,install apps.

```bash
 sudo scoop install openjdk oraclejdk8 -g
 sudo scoop install kotlin scala groovy python php nvm nodejs-lts -g
 sudo scoop install maven gradle sbt ant -g
#sudo scoop install docker docker-compose docker-machine -g 
 
 scoop install vcredist
 scoop install coreutils curl openssh grep wget which sed tar telnet time less touch
 scoop install notepadplusplus notepadplusplus-pm sublime-text vscode everything
 scoop install cmder jetbrains-toolbox jd-gui tortoisesvn zeal
 scoop install chromium ccleaner shadowsocks

#scoop install aria2 qbittorrent transmission
#scoop install postgresql mysql mariadb redis sqlite heidisql
#scoop install elasticsearch kibana logstash

 scoop install fscapture lingoes dns-jumper wnmp

```