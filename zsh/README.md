## ZSH configuration


### Setup
+ Open `./zshrc` file. **Run** `cd ./zshrc`

### PATH Environment
+ Add following PATH env
  
  ```bash
  # PATH Environment
  # Golang
  export GOROOT="/usr/local/go"
  export GOPATH="$HOME/go"
  export PATH="$PATH:$GOPATH/bin:$GOROOT/bin"
  # JAVA 8
  export JAVA_HOME=/opt/jdk
  export JRE_HOME=/opt/jdk/jre
  export M2_HOME=/opt/maven
  export PATH=${M2_HOME}/bin:${PATH}
  # python
  export PY_VIRTUAL_ENV="/home/shuvojit/.local/bin"
  export PATH=$PATH:$PY_VIRTUAL_ENV
  # sls environments
  export SLS_DEBUG=*
  ```

### Aliasing
+ Add following aliases at EOF
   ```bash
    # aliasing
    # file
    alias edit-zsh="subl ~/.zshrc"
    alias edit-profile="subl ~/.zshrc"
    alias source-zsh="source ~/.zshrc"
    alias source-profile="source ~/.zshrc"
    alias edit-sudoers="sudo subl /etc/sudoers"
    alias edit-hosts="sudo subl /etc/hosts"
    alias edit-git-exclude="subl .git/info/exclude"
    # Directory
    alias cd-ibfd-kaz="$HOME/Desktop/IBFD-KAZ"
    alias cd-ibfd-kaz-client="$HOME/Desktop/IBFD-KAZ/client"
    alias cd-ibfd-kaz-server="$HOME/Desktop/IBFD-KAZ/server"
    alias cd-ibfd-kaz-driver="$HOME/Desktop/IBFD-KAZ/driver"
    alias cd-ibfd-kaz-driver-cvs="$HOME/Desktop/IBFD-KAZ/driver-cvs"
    alias cd-ibfd-kaz-doc="$HOME/Desktop/IBFD-KAZ/doc"
    alias cd-ibfd-kaz-db-local="$HOME/Desktop/IBFD-KAZ/docker-db"
    alias cd-home="cd $HOME"
    alias cd-learning="cd $HOME/Desktop/Learning"
    alias ibfd-test-user="cat $HOME/Desktop/IBFD-KAZ/test-users.json"
    alias azure-test-user="cat $HOME/Desktop/IBFD-KAZ/azure-ad-test-users.json"
    # scripts
    alias update="sudo apt update"
    alias upgrade="sudo apt upgrade"
    # angular
    alias run-ng-build="ng build"
    alias run-ng-build-prod="ng build --prod"
    alias run-ng-lint="ng lint"
    alias run-ng-test="ng test"
    alias run-ng-test-headless="ng test --watch=false --browsers=ChromeHeadless"
    alias run-ng-proxy="ng serve --host=shuvojit.ibfd.org --port=4200 --proxy-config proxy-conf.json"
    alias run-ng-proxy-export="ng serve --host=0.0.0.0 --port=4200 --proxy-config proxy-conf.json"
    alias run-ng-lint-prod-test="ng lint && ng build --prod && ng test"
    alias run-packagr="npm run packagr"
    alias run-trp="ng serve --host=shuvojit.ibfd.org --port=8080 --proxy-config proxy-conf.json"
    alias run-ng="ng serve --host=shuvojit.ibfd.org --port=4200"
    # golang
    alias run-go-app="chmod +x run.sh && ./run.sh local"
    alias run-go-app-dev="chmod +x run.sh && ./run.sh dev"
    # git
    alias gbr="git branch"
    alias gps="git push"
    alias gpsm="git push origin master"
    alias gpl="git pull"
    alias gplm="git pull origin master"
    alias gplmain="git pull origin main"
    alias gcm="git commit -m"
    alias gcam="git commit -a -m"
    alias gst="git status"
    alias gdf="git diff"
    alias gad="git add"
    alias gch="git checkout"
    alias gchm="git checkout master"
    alias gchmain="git checkout main"
    alias gcb="git checkout -b"
    alias glog="git log --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset' --abbrev-commit"
    alias git-ibfd-config="git config user.email shuvojit.saha@kaz.com.bd && git config user.name 'Shuvojit Saha'"
    alias git-self-config="git config user.email shuvojitsahashuvo@gmail.com && git config user.name 'ParthoShuvo'"
    alias git-global-config="git config --global user.email shuvojit.saha@kaz.com.bd && git config --global user.name 'Shuvojit Saha'"
    alias sping="ping -c 5 www.stackoverflow.com"
    alias gping="ping -c 5 www.google.com"
    #THIS MUST BE AT THE END OF THE FILE FOR SDKMAN TO WORK!!!
    export SDKMAN_DIR="/home/shuvojit/.sdkman"
    [[ -s "/home/shuvojit/.sdkman/bin/sdkman-init.sh" ]] && source "/home/shuvojit/.sdkman/bin/sdkman-init.sh"
    # intellji
    alias datagrip="sudo /usr/local/bin/datagrip &"
    # chrome
    alias chrome-cors='google-chrome --args --user-data-dir="/tmp/chrome_dev_test" --disable-web-security &'
   ```