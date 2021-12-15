[//]: #@corifeus-header

[![NPM](https://nodei.co/npm/p3x-redis-ui.png?downloads=true&downloadRank=true)](https://www.npmjs.com/package/p3x-redis-ui/)

  

[![Donate for Corifeus / P3X](https://img.shields.io/badge/Donate-Corifeus-003087.svg)](https://paypal.me/patrikx3) [![Contact Corifeus / P3X](https://img.shields.io/badge/Contact-P3X-ff9900.svg)](https://www.patrikx3.com/en/front/contact) [![Corifeus @ Facebook](https://img.shields.io/badge/Facebook-Corifeus-3b5998.svg)](https://www.facebook.com/corifeus.software)  [![Build Status](https://github.com/patrikx3/redis-ui/workflows/build/badge.svg)](https://github.com/patrikx3/redis-ui/actions?query=workflow%3Abuild)
[![Uptime Robot ratio (30 days)](https://img.shields.io/uptimerobot/ratio/m780749701-41bcade28c1ea8154eda7cca.svg)](https://stats.uptimerobot.com/9ggnzcWrw)





# 📡 P3X Redis UI is a very functional handy database GUI and works in your pocket on the responsive web or as a desktop app v2021.10.260



**Bugs are evident™ - MATRIX️**
    



### NodeJS LTS is supported

### Built on NodeJs version

```txt
v16.13.1
```





# Description

                        
[//]: #@corifeus-header:end

`p3x-redis-ui` is a new Redis GUI which can serve as a backend server or as a desktop application.
  
Some of the features are coming below. 
  
The best use case for this Redis GUI, if you manage tons of JSON, as it includes JSONEditor and ACE. Check out the different options in the edit json button dialog. :)


<!--
👷 **The first full complete version was created in 20 days in September of 2018.** 
-->

<!--
## Donated-Ware features
  
**Until further notice, all donated-ware features are enabled for free. Please, test out your use case, how the JSON editor is helping you. Let us know!**

The `p3x-redis-ui+` version has additional features.   
The donation is $1/month. Please contact at [alabard@gmail.com](mailto:alabard@gmail.com) and can donate @ https://paypal.me/patrikx3  
  
The features that are only working in the donated-ware version:
* JSON editor
* Cluster
* AWS ElastiCache
* Gcloud memorystore
* Azure Redis

To check if your license is valid @  
https://server.patrikx3.com/api/patrikx3/redis-ui/status/your-license-key

#### New features
Users, that donated, have a big chance that requests for new features will be implemented.

##### Possible new features
* SSH tunnel
* Upload binary data
* Collapse/expand recursively on individual leafs

#### Plus function problems
Given, I do not have a full fledged server and to maintain the servers it costs money, it is possible, sometimes the server goes down. It is rare, but it will be back up probably in 5-10 minutes. If there is a problem that is longer, please contact me.

### Contributors license
Contributors get plus donate license for free for a year.    
Contributors, that created features that are working only in the donate-ware version get a license for life.  
  
-->  
  
## Warning 
It is not recommend to generate the configuration `JSON` via a text editor. The perfect solution is to generate the configuration in the GUI, then apply for example in Kubernetes.

## The online current version
https://p3x.redis.patrikx3.com  <!-- - this is the plus version -->

This Redis database every day in the morning European time CET restores some data, so you may do whatever you want to do.   
  
Besides, you could experience the test app to exit for 1 second, because it could auto update itself. It auto updates itself when the code from Git changes.

Third, it is a snapshot, it is possible, that the features are different from GitHub or NPM as the releases are usually monthly or as they happen. 


### Screenshots
[Screenshots readme](artifacts/readme/screenshots.md)

## Releases

### Snap

<!--
The main source installer is the `AppImage`, so, the themes are not implemented (the main menus). If you want the themes to be implemented (dark vs light), I suggest using the `AppImage` as it supports the themes natively. Besides, the auto self update function is not implemented in `Snap`, only in `AppImage` version.  
-->

[![LINK](https://snapcraft.io/static/images/badges/en/snap-store-black.svg)](https://snapcraft.io/p3x-redis-ui#cory-non-external)

### AppImage

https://github.com/patrikx3/redis-ui/releases  

#### To integrate into the menu
Execute:
```bash
sudo add-apt-repository ppa:appimagelauncher-team/stable
sudo apt-get update
sudo apt-get install appimagelauncher
```


#### After downloading the ```AppImage```, make it an executable.
```bash
mkdir -p $HOME/opt
mv ~/Downloads/p3x-redis-ui-a.b.c-x86_64.AppImage $HOME/opt/
chmod +x $HOME/opt/p3x-redis-ui-a.b.c-x86_64.AppImage
# Then you can run it
$HOME/opt/p3x-redis-ui-a.b.c-x86_64.AppImage &
```


<!--
It then actually integrates itself into the menus and it will auto update itself.
-->

### On ElectronJs  
(The GitHub versions are always instant, while the ElectronJs Apps releases are delayed.)  
https://electronjs.org/apps/p3x-redis-ui  

### CLI
 
Start up with a server or via a browser and NodeJs/NPM.
  
[Start up with a server readme](artifacts/readme/start-up-server.md)

[Some description about the config file readme](p3xrs.json)

### Docker 

https://hub.docker.com/r/patrikx3/p3x-redis-ui

#### Compose
https://github.com/patrikx3/redis-ui/blob/master/docker-compose.yml  
  
  

```bash
wget https://raw.githubusercontent.com/patrikx3/redis-ui/master/docker-compose.yml
# You might want to tune the settings folder in the docker-compose.yml.
# the /home/user/p3x-redis-ui-settings settings folder in yml should be set by yourself.
docker-compose up
```

#### Bare

```bash
# you can tune the settings folder
# in the -v first part is where you can set your own folder
mkdir -p ./p3x-redis-ui-settings
docker run -v $PWD/p3x-redis-ui-settings:/settings -h docker-p3x-redis-ui -p 7843:7843 -t -i patrikx3/p3x-redis-ui
```

The GUI will be @ http://localhost:7843

### Kubernetes

A complete example of deployment `p3x-redis-ui` in kubernetes using raw manifests
https://github.com/patrikx3/redis-ui/blob/master/k8s/manifests

```bash
kubectl apply -f namespace.yaml
# Do not forget to edit redis host and password configuration
kubectl apply -f configmap.yaml
kubectl apply -f deployment.yaml
kubectl apply -f service.yaml
kubectl apply -f ingress.yaml
```

Helm chart `p3x-redis-ui` deployment in kubernetes
https://github.com/patrikx3/redis-ui/blob/master/k8s/chart

```bash
helm template -f values.yaml release --namespace namespace . > generated.yaml
kubectl apply -f generated.yaml
```

## Features 

* The console history is kept indefinite in the local storage
* Redis 6 with TLS is enabled with this information:
  * https://spin.atomicobject.com/2021/08/05/configuring-redis-tls/
* You can override the server port via an environment variable `P3XRS_PORT`
* In the connections, you can enable read only mode, which means, the user will not be able to modify via gui and the console (only pub/sub monitor and select database is allowed) is disabled. 
* In a sub-directory, you can use Nginx/Ingress to rewrite your paths.
  * https://github.com/patrikx3/redis-ui/issues/43
* To show the menu in the desktop version, click ALT
* There is a new feature in the settings/tree setting, which limits the received keys, the minimum is 100, the maximum is 100k, so there is no more crash, because of that
* Since `v2020.4.189`, the tree can handle bigger key count, as of now, we are using deferred rendering for the tree - only rendering what is in the viewport, so it should be much faster versus rendering everything at once 
* Please, check out your Redis use case, if this program can cover your requirements
* Does not handle binary data
* **Does not work with sentinel**, but it will be developed at some point of time
* **Has cluster support**
  * Thanks so much for the awesome contribution by [@idetoile](https://github.com/idetoile) (now -> [@devthejo](https://github.com/devthejo)) of the cluster function.
* Able to monitor all channel messages on the console by using a checkbox.
* Works with multiple languages
* Works as a backend
* Works as a desktop via Electron
  * Linux
  * Windows
  * macOS
* Starts with no settings without config, or setup your own config
* Able to create, test, save, delete multiple connections or a readonly connections setup, for shared usage* 
* Online you are able to choose the tree separator, for example :, /, -, space etc... or even empty separator
* It is based on Redis-Commander and phpRedisAdmin
* You can select the database via console or the drop down.
   * The database select drop down shows if the checked database is empty or filled, so you can always know which is filled
* Save button to save the db
* Full statistics pages, can be useful
* This is just a New Kind on the Block in the Redis world, so, of course, there are advantages and disadvantages in the other Redis GUIs
* Dark - Dracula / light themes
* Search
  * Client side mode searching in keys - small key set
  * Server side mode searching in keys - large key set
  * Search mode
    * the search keys starts with a string key
    * the search keys includes a string in the key
* The app is responsive, it works on a phone/tablet as well
* There is a key sorting function, which has a penalty, because it sorts with natural-compare, which means it is more human display, then just raw characters, but up to 100k the keys is still ok. 
* For big key set to be usable paging should be a maximum 1000 keys / page, though for 250 is the sweetest spot


# TODO
[The to do readme](todo.md) 

# Change log
[The change log readme](change-log.md) 

# Contributors
[The contributors readme](contributors.md)

# Development

For file names do not use camelCase, but use kebab-case. Folder should be named as kebab-case as well. As you can see, all code filenames are using it like that, please do not change that.
Please apply the `.editorconfig` settings in your IDE.

It creates a package that allows you to compose `p3x-redis-ui-server` and `p3x-redis-ui-material` into one:

[Server on GitHub](https://github.com/patrikx3/redis-ui-server)  
[Client on GitHub](https://github.com/patrikx3/redis-ui-material)

If you develop on this app, you are required to test, that all JS you code write is working with Electron (as the embedded Electron NodeJs version is usually below the real NodeJs). Once the server and client is running as above, you clone this repo and test like this:
```bash
# terminal 1
git clone https://github.com/patrikx3/redis-ui-material.git
cd redis-ui-material
npm install
npm run dev

# terminal 2
git clone https://github.com/patrikx3/redis-ui-server.git
cd redis-ui-server
npm install
npm run dev

# if you are not working on Electron, at this point you can fire the browser
# @ http://localhost:8080/

# terminal 3 
git clone https://github.com/patrikx3/redis-ui.git
cd redis-ui
npm install
./scripts/start-local.sh
# or
.\scripts\start-local.cmd
```

### Development of the translations

By default, only English is created, but given all strings are from a `JS` file, it is very quick to spawn another language eg. German, French, Spanish etc ...

[English strings, for the web UI](https://github.com/patrikx3/redis-ui-material/blob/master/src/strings/en/strings.js)   
[English strings, for the Electron](https://github.com/patrikx3/redis-ui/blob/master/src/strings/en/index.js)

For a new language:
Add into `redis-ui-material/src/bundle.js`.

This solution is not using REST at all, but instead uses Socket.IO 🤣, which is weird, but I like it, it is supposed to be more responsive, as there is no big overhead in the HTTP protocol.

### Reference for Socket.IO speed
https://www.google.com/search?q=rest+vs+websocket+comparison+benchmarks


# URL links

[P3X Redis UI playground](https://www.patrikx3.com/en/front/playground/19/p3x-reds-ui#PG19)  
  
[Corifeus P3X Redis UI](https://corifeus.com/redis-ui/)  
  
[AlternativeTo Redis UI](https://alternativeto.net/software/p3x-redis-ui/)  

[NPM P3X Redis UI](https://www.npmjs.com/package/p3x-redis-ui)

[Snap Store](https://snapcraft.io/p3x-redis-ui)

[Github.IO Page](https://patrikx3.github.io/redis-ui/)

[//]: #@corifeus-footer

---

🙏 This is an open-source project. Star this repository, if you like it, or even donate to maintain the servers and the development. Thank you so much!

Possible, this server, rarely, is down, please, hang on for 15-30 minutes and the server will be back up.

All my domains ([patrikx3.com](https://patrikx3.com) and [corifeus.com](https://corifeus.com)) could have minor errors, since I am developing in my free time. However, it is usually stable.

**Note about versioning:** Versions are cut in Major.Minor.Patch schema. Major is always the current year. Minor is either 4 (January - June) or 10 (July - December). Patch is incremental by every build. If there is a breaking change, it should be noted in the readme.


---

[**P3X-REDIS-UI**](https://corifeus.com/redis-ui) Build v2021.10.260

[![Donate for Corifeus / P3X](https://img.shields.io/badge/Donate-Corifeus-003087.svg)](https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=QZVM4V6HVZJW6)  [![Contact Corifeus / P3X](https://img.shields.io/badge/Contact-P3X-ff9900.svg)](https://www.patrikx3.com/en/front/contact) [![Like Corifeus @ Facebook](https://img.shields.io/badge/LIKE-Corifeus-3b5998.svg)](https://www.facebook.com/corifeus.software)


## P3X Sponsor

[IntelliJ - The most intelligent Java IDE](https://www.jetbrains.com/?from=patrikx3)

[![JetBrains](https://cdn.corifeus.com/assets/svg/jetbrains-logo.svg)](https://www.jetbrains.com/?from=patrikx3)




[//]: #@corifeus-footer:end

