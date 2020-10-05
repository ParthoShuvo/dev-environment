# Current development environment details with tools & setups 

## Ubuntu 20.04 LTS
- #### oh-my-zsh
    - **Run below commands**
        1. `sudo apt install zsh`
        2. `sudo apt-get install powerline fonts-powerline`
        3. `git clone https://github.com/robbyrussell/oh-my-zsh.git ~/.oh-my-zsh`
        4. `cp ~/.oh-my-zsh/templates/zshrc.zsh-template ~/.zshrc`
        5. `chsh -s /bin/zsh`
        6. [More](https://dev.to/mskian/install-z-shell-oh-my-zsh-on-ubuntu-1804-lts-4cm4)
        7. *Nerd Fonts* follow [link](https://github.com/ryanoasis/nerd-fonts#option-6-ad-hoc-curl-download)
        
- #### Browser
    1. **Google Chrome - Latest**
    2. **Firefox - Latest**

- #### VPN 
    1. **Cisco any connect** 
        - *installation*
            1. unzip .tar.gz file
            1. `sudo apt install libpangox-1.0-0 libcanberra-gtk-module`
            2. `cd ${path-to-unzipped-folder}/vpn`
            3. `chmod +x vpn_install.sh`
            4. `sudo ./vpn_install.sh`

- #### VCS
    1. **Git-2.17.1 or latest** 
        - *install*  `sudo apt install git`
        - *config* 
            - *User name*  `git config --global user.name "${USER_NAME}"` 
            - *User email*  `git config --global user.name "${USER_EMAIL}"`
    2. **SSH Key**
        - *generate new* `ssh-keygen -t rsa -b 4096 -C "email@example.com"`
- #### IDE/Text-Editor
    1. **VS Code** 
        - *install* `sudo snap install code --classic`
        - *Extensions*
            1. Angular Essentials
            2. TSLint
            3. Live Server
            4. GitLens
            5. Bracket Pair Colorizer 2
            6. Docker
            7. XML Tools
            8. Emmet
            9. docs-markdown
            10. Go
        - *Themes*
            1. Winter is coming (Dark)
        - *Icons*
            1. VSCode Icons
        - *Keymap*
            1. Eclipse Keymap
        - *Watcher size of file changes in large workspace* [link](https://code.visualstudio.com/docs/setup/linux#_visual-studio-code-is-unable-to-watch-for-file-changes-in-this-large-workspace-error-enospc) 
    2. **gedit**
    3. **nano**
    4. **Datagrip 2016.3.4**
    5. **IntelliJ Idea 2017.1.6**
    6. **Sublime Text** 
        - *install* `sudo snap install sublime-text --classic`
        - *run in terminal* `subl $file`
- #### Language & Environments
    1. **Node.js**
        - *Run following commands*
            1. `curl -sL https://deb.nodesource.com/setup_12.x -o nodesource_setup.sh` > current: Node.js 12.16.2 stable
            2. `sudo bash nodesource_setup.sh`
            3. `sudo apt-get install -y nodejs`
            4. `nodejs -v`
            5. `npm -v`
            6. `sudo apt install build-essential`
    2. **angular-cli** 
        - *Run following commands*
            1. `sudo npm install -g @angular/cli`
            2. `ng version`
    3. **sdkman cli** - [install](https://sdkman.io/install)
    4. **JAVA 8** follow [link](https://www.fosstechnix.com/install-oracle-java-8-on-ubuntu/)
    5. **Maven 3** follow [link](https://www.vultr.com/docs/how-to-install-apache-maven-on-ubuntu-16-04)
    6. **Scala 2.13.1** `sdk install scala`
    8. **sbt (Scala build tool)** [follow](https://www.scala-sbt.org/download.html?_ga=2.179985249.491955621.1587575220-146846830.1587499294)
    7. **Go 1.13** 
        - *install* follow [link](https://linuxize.com/post/how-to-install-go-on-ubuntu-18-04/)
        - *VSCode Debugger* [launch.json](https://gist.github.com/ParthoShuvo/dec4add75cb67b88b38c7035e7ee0c79)
- #### Database
    1. **MySQL - 8** [link](https://www.digitalocean.com/community/tutorials/how-to-install-mysql-on-ubuntu-20-04-quickstart)
- #### Communication
    1. **Skype** `sudo snap install skype --classic`
    2. **Google Hangouts**
    3. **Slack** `sudo snap install slack --classic`
- #### Media
    1. **VLC** `sudo snap install vlc`
- #### Tools
    1. **curl** `sudo apt install curl`
    2. **Postman** `sudo snap install postman`
    3. **htop** `sudo snap install htop`
    4. **Docker**
        - *Run* `sudo snap install docker`
        - For without root permission follow [link](https://stackoverflow.com/questions/48957195/how-to-fix-docker-got-permission-denied-issue) 
- #### Document Reader
    1. **Foxit Reader** [link](http://ubuntuhandbook.org/index.php/2015/09/install-foxit-reader-in-ubuntu/)
- #### Miscellaneous
    1. **tlp**
        - `sudo add-apt-repository ppa:linrunner/tlp`
        - `sudo apt-get update`
        - `sudo apt-get install tlp tlp-rdw`
    2. **cpufreq indicator** `sudo apt-get install indicator-cpufreq`
    3. **gnome-tweak-tools**
        - `sudo apt install -y gnome-tweaks`
        - `sudo apt-get install gnome-tweak-tool`
    4. **qBittorrent 4.1.7**
        - `sudo add-apt-repository ppa:qbittorrent-team/qbittorrent-stable`
        - `sudo apt update && sudo apt install qbittorrent`
    5. **git hooks**
        - **Angular (pre-push)** [file](https://gist.github.com/ParthoShuvo/3a3ae1a949e1c13af2db03cc93a200fc)
    6. **inotify-tools** `sudo apt-get install inotify-tools`
    7. **youtube-dl** [follow](https://github.com/ytdl-org/youtube-dl)
        - *install* `sudo snap install youtube-dl`
        - */etc/youtubel-dl.conf* [file](https://gist.github.com/ParthoShuvo/d3954c9424b7e0f5ca5952a058d51517)
        - *[optional] watcher to move downloaded file to new location* [file](https://gist.github.com/ParthoShuvo/98a30413d2bdddeb80d1379747c49bac)
    8. **fast** - CLI internet speed test
        - *install* `sudo snap install fast`
- #### Scripts
    1. **Execute sudo without password**
        - open `sudo subl /etc/sudoers`
        - add line `shuvojit ALL=(ALL) NOPASSWD: ALL` at the EOF
        
            
