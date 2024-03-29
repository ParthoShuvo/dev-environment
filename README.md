## Ubuntu 20.04 LTS

- ### Ansible
  
  - [What is ansible][9]
  - To install follow [this][8]

- ### Homebrew

- Run `/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"`. For [more][15]

- ### oh-my-zsh

  - **Run below commands**
        1. `sudo apt install zsh`
        2. `sudo apt-get install powerline fonts-powerline`
        3. `git clone https://github.com/robbyrussell/oh-my-zsh.git ~/.oh-my-zsh`
        4. `cp ~/.oh-my-zsh/templates/zshrc.zsh-template ~/.zshrc`
        5. `chsh -s /bin/zsh`
        6. Try following steps to install [PowerLevel10k][10] theme
            - `git clone https://github.com/romkatv/powerlevel10k.git $ZSH_CUSTOM/themes/powerlevel10k`
            - Set the theme `ZSH_THEME="powerlevel10k/powerlevel10k"` in .zshrc file
            - Install following [fonts][11]
            - Run `p10k configure`
        7. Try following to change gnome terminal
            - Follow <https://github.com/Gogh-Co/Gogh> to install
            - Apply Gotham theme
        8. _More_
            - <https://dev.to/mskian/install-z-shell-oh-my-zsh-on-ubuntu-1804-lts-4cm4>
            - <https://www.freecodecamp.org/news/jazz-up-your-zsh-terminal-in-seven-steps-a-visual-guide-e81a8fd59a38/>
        9.  *Nerd Fonts* follow [link](https://github.com/ryanoasis/nerd-fonts#option-6-ad-hoc-curl-download)
        10. ___Current ZSH Setup___
           1. [Config][2]
           2. [Current zshrc file][3]
        11. Install plugins
            - git
            - git-flow: `brew install git-flow`
            - brew
            - npm
            - node
            - history
            - docker
            - kubectl: [follow][12]
            - kubectx: [follow][13]
            - zsh-syntax-highlighting
            - zsh-autosuggestions: follow [this][13]
            - minikube: [follow][14]

- ### Browser

    1. **Google Chrome - Latest**
    2. **Firefox - Latest**

- ### VPN

    1. [**Cisco any connect**][1]
        - *installation*
            1. unzip .tar.gz file
            2. `sudo apt install libpangox-1.0-0 libcanberra-gtk-module`
            3. `cd ${path-to-unzipped-folder}/vpn`
            4. `chmod +x vpn_install.sh`
            5. `sudo ./vpn_install.sh`

- ### VCS

    1. **Git-2.17.1 or latest**
        - *install*  `sudo apt install git`
        - *config*
            - *User name*  `git config --global user.name "${USER_NAME}"`
            - *User email*  `git config --global user.name "${USER_EMAIL}"`
    2. **SSH Key**
        - *generate new* `ssh-keygen -t rsa -b 4096 -C "email@example.com"`
    3. **GitKraken**
        - *install* follow [this][5]
        - *patcher* follow [this][6]

- ### IDE/Text-Editor

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
        - [*Extension installation script*][4]
           - _**Make sure**_ you have the ``code`` command line installed
           - Make executable: `chmod +x ./my_vscode_extensions.sh`
           - Run script: `./my_vscode_extensions.sh`
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

- ### Language & Environments

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
    7. **sbt (Scala build tool)** [follow](https://www.scala-sbt.org/download.html?_ga=2.179985249.491955621.1587575220-146846830.1587499294)
    8. **Go 1.13**
        - *install* follow [link](https://linuxize.com/post/how-to-install-go-on-ubuntu-18-04/)
        - *VSCode Debugger* [launch.json](https://gist.github.com/ParthoShuvo/dec4add75cb67b88b38c7035e7ee0c79)
    9. **Python3**
       - **install**

            ```bash
            sudo apt install python3 python3-pip -y
            ```

       - **create virtual env** [_follow_](https://www.digitalocean.com/community/tutorials/how-to-install-python-3-and-set-up-a-programming-environment-on-an-ubuntu-20-04-server)
    10. [**PHP-7 and Composer**][7]

- ### Database

    1. **MySQL - 8**
        - **install** [link](https://www.digitalocean.com/community/tutorials/how-to-install-mysql-on-ubuntu-20-04-quickstart)
        - **workbench** [link](https://dev.mysql.com/downloads/workbench/)

- ### Communication

    1. **Skype** `sudo snap install skype --classic`
    2. **Google Hangouts**
    3. **Slack** `sudo snap install slack --classic`

- ### Media

    1. **VLC** `sudo snap install vlc`

- ### Tools

    1. **curl** `sudo apt install curl`
    2. **Postman** `sudo snap install postman`
    3. **htop** `sudo snap install htop`
    4. **Docker**
        - *Run* `sudo snap install docker`
        - For without root permission follow [link](https://stackoverflow.com/questions/48957195/how-to-fix-docker-got-permission-denied-issue)

- ### Document Reader

    1. **Foxit Reader** [link](http://ubuntuhandbook.org/index.php/2015/09/install-foxit-reader-in-ubuntu/)

- ### Miscellaneous

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

- ### Microsoft Office -2013

  - **install playonlinux**

    ```bash
    sudo apt install playonlinux
    ```

  - **install winbind**

    ```bash
    sudo apt install winbind -y
    ```

  - **download microsoft windows-2013** [_from_](https://drive.google.com/file/d/1v2TdcR99TcjZyIUbKgeP-qvsUxZjRvQj/view?usp=sharing)
  - **follow [_this_](https://www.youtube.com/watch?v=Vf8zr096mYQ&ab_channel=DistroTester)**

- ### Scripts

    1. **Execute sudo without password**
        - open `sudo subl /etc/sudoers`
        - add line `shuvojit ALL=(ALL) NOPASSWD: ALL` at the EOF

- ### VM

    1. [**VMware Player**](https://itsfoss.com/install-vmware-player-ubuntu-1310/)

[16]: https://github.com/ahmetb/kubectx
[15]: https://brew.sh/
[14]: https://minikube.sigs.k8s.io/docs/commands/completion/#:~:text=minikube%20shell%20completion%20for%20the%20given%20shell
[13]: https://github.com/zsh-users/zsh-autosuggestions/blob/master/INSTALL.md
[12]: https://kubernetes.io/docs/tasks/tools/included/optional-kubectl-configs-zsh/
[11]: https://github.com/romkatv/powerlevel10k#:~:text=download%20these%20four%20ttf%20files
[10]: https://github.com/romkatv/powerlevel10k#fonts
[9]: https://www.youtube.com/watch?v=1id6ERvfozo&ab_channel=TechWorldwithNana
[8]: https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html#installing-ansible-on-ubuntu
[7]: https://www.digitalocean.com/community/tutorials/how-to-install-and-use-composer-on-ubuntu-20-04
[6]: https://github.com/5cr1pt/GitCracken
[5]: https://gist.github.com/ParthoShuvo/f5e716989103c7db1b8c7a38fc3b243e
[1]: https://drive.google.com/file/d/1sRXrfgyVo2qbxCgmAup3GDtXMxQyBK_D/view?usp=sharing
[2]: https://github.com/ParthoShuvo/dev-environment/blob/master/zsh
[3]: https://github.com/ParthoShuvo/dev-environment/blob/master/zsh/zshrc
[4]: https://github.com/ParthoShuvo/dev-environment/blob/master/my_vscode_extensions.sh
