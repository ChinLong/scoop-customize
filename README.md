## scoop-customize

The "customize" bucket for [Scoop](http://scoop.sh).


### How to use?


##### Firstly, make sure installed the [Scoop](http://scoop.sh/).


Set system environment ```SCOOP``` and ```SCOOP_GLOBAL```.(Suggested)

```bash
 set-executionpolicy remotesigned -scope currentuser
 [environment]::setEnvironmentVariable('SCOOP','D:\scoop\user','User')
 [environment]::setEnvironmentVariable('SCOOP_GLOBAL','D:\scoop\global','User')
 iex (new-object net.webclient).downloadstring('https://get.scoop.sh')
```


##### Then Add buckets.



add [scoop-extras](https://github.com/lukesampson/scoop-extras.git)

```bash
 scoop bucket add extras
```

and add this.

```bash
 scoop bucket add customize https://github.com/ChinLong/scoop-customize.git
```


##### Finally,install apps.


```bash

 scoop install sudo 
 scoop install 7zip 
 scoop install git 

 sudo scoop install oraclejdk scala python php nvm nodejs-lts -g
 sudo scoop install maven gradle sbt typesafe-activator -g

 scoop install coreutils curl openssh grep wget
 scoop install zeal shadowsocks ccleaner chromium jd-gui jetbrains-toolbox lingoes sublime-text heidisql
  
```