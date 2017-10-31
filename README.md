## scoop-customize


The "customize" bucket for [Scoop](http://scoop.sh).


### How to use?

##### Firstly, make sure installed the [Scoop](http://scoop.sh/).

Set system environment ```SCOOP``` and ```SCOOP_GLOBAL```.(Suggested) 

##### Then Add buckets.

add [scoop-extras](https://github.com/lukesampson/scoop-extras.git)

```bash
 scoop bucket add extras
```
add this.

```bash
 scoop bucket add customize https://github.com/ChinLong/scoop-customize.git
```
##### Finally,install apps.

```bash

 scoop install sudo
 scoop install zeal shadowsocks ccleaner chromium jd-gui jetbrains-toolbox lingoes scoop sublime-text
  
 sudo scoop install coreutils 7zip curl openssh grep wget -g
 sudo scoop install oraclejdk scala python -g
 sudo scoop install git -g
 sudo scoop install gradle maven gradle sbt typesafe-activator -g
 sudo scoop install nvm nodejs -g
 sudo scoop install heidisql redis wnmp -g
 
```