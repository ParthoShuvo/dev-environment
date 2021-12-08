# ZSH configuration

## Setup

+ Open `./zshrc` file. **Run** `cd ./zshrc`

### PATH Environment

+ Add following PATH env
  
  ```bash
  # PATH Environment
  # NPM/NodeJS
  export NPM_PACKAGES="${HOME}/.npm-packages"
  export NODE_PATH=$NPM_PACKAGES/lib/node_modules:$NODE_PATH
  export PATH=$NPM_PACKAGES/bin:$PATH
  # Golang
  export GOROOT="/usr/local/go"
  export GOPATH="$HOME/go"
  export PATH="$PATH:$GOPATH/bin:$GOROOT/bin"
  export GOPROXY="http://proxy.golang.org,http://support7.ibfd.org:3000,direct"
  # export GOPRIVATE=""
  export GONOSUMDB="gitlab.ibfd.org/*" #Required to connect with athens-server
  #export GOPRIVATE="github.com/system-modules/*,ibfd.org/*,gitlab.ibfd.org/server/*"
  # JAVA 8
  export JAVA_HOME=/opt/jdk
  export PATH=${JAVA_HOME}/bin:${PATH}
  export JRE_HOME=/opt/jdk/jre
  export PATH=${JRE_HOME}/bin:${PATH}
  export M2_HOME=/opt/maven
  export PATH=${M2_HOME}/bin:${PATH}
  # python
  export PY_VIRTUAL_ENV="/home/shuvojit/.local/bin"
  export PATH=$PATH:$PY_VIRTUAL_ENV
  # aws eb cli
  export PATH="/home/shuvojit/.ebcli-virtual-env/executables:$PATH"
  # sls environments
  export SLS_DEBUG=*
  # aws-cli auto-complete
  autoload bashcompinit && bashcompinit
  autoload -Uz compinit && compinit
  compinit
  complete -C '/usr/local/bin/aws_completer' aws

  #AWS CLI
  export AWS_PROFILE=Shuvojit

  # AWS RDS
  export AWS_RDS_USERNAME=Nirvana
  export AWS_RDS_PASSWORD=hbosNizhas4%
  export AWS_SSH_LOCATION='103.217.111.148/32'

  # EB CLI
  alias update-eb-cli="python aws-elastic-beanstalk-cli-setup/scripts/ebcli_installer.py"
  export AWS_EB_PROFILE=Shuvojit
  ```

### Aliasing

+ Add following aliases at EOF

   ```bash
    #jetbrains agent
    alias JETBRAINS_AGENT="echo '-javaagent:/home/shuvojit/opt/jetbrains-agent/jetbrains-agent.jar'"
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
    alias cd-ibfd-kaz-go-modules="$HOME/Desktop/IBFD-KAZ/go-modules"
    alias cd-ibfd-kaz-driver="$HOME/Desktop/IBFD-KAZ/driver"
    alias cd-ibfd-kaz-driver-cvs="$HOME/Desktop/IBFD-KAZ/driver-cvs"
    alias cd-ibfd-kaz-doc="$HOME/Desktop/IBFD-KAZ/doc"
    alias cd-ibfd-kaz-db-local="$HOME/Desktop/IBFD-KAZ/docker-db"
    alias cd-ibfd-kaz-research="$HOME/Desktop/IBFD-KAZ/research"
    alias cd-home="cd $HOME"
    alias cd-learning="cd $HOME/Desktop/Learning"
    alias cd-interview-prep="cd $HOME/Desktop/Learning/interview-prep"
    alias ibfd-test-user="cat $HOME/Desktop/IBFD-KAZ/test-users.json"
    alias azure-test-user="cat $HOME/Desktop/IBFD-KAZ/azure-ad-test-users.json"
    # scripts
    alias update="sudo apt update"
    alias upgrade="sudo apt upgrade"
    alias killport='function _killp(){ lsof -nti:$1 | xargs kill -9 };_killp'
    alias autoremove="sudo apt autoremove -y"
    alias autoclean="sudo apt autoclean"
    # docker
    alias dokr-img-rm-unused="docker image prune -a"
    alias dokr-img-rm-dangling="docker image prune"
    alias dokr-img-rm-all='docker image rm ${docker image ls -q}" -f'
    alias dokr-img-list="docker image ls"
    alias dokr-info="docker info"
    alias dokr-container-rm-all='docker container rm $(docker container ls -aq) -f'
    # angular
    alias run-trp-prod-ssl="ng build --prod && mv dist/trp/assets/etc dist/trp/ && http-server dist/trp --port=4200 --proxy https://dev-research.ibfd.org --ssl --cert ssl/server.crt --key ssl/server.key"
    alias run-trp-prod="ng build --prod && mv dist/trp/assets/etc dist/trp/ && http-server dist/trp --port=4200 --proxy https://dev-research.ibfd.org"
    alias run-ng-build="ng build"
    alias run-ng-build-prod="ng build --prod"
    alias run-ng-lint="ng lint"
    alias run-ng-test="ng test"
    alias run-ng-test-headless="ng test --watch=false --browsers=ChromeHeadless"
    alias run-ng-proxy="ng serve --host=shuvojit.ibfd.org --port=8080 --proxy-config proxy-conf.json"
    alias run-ng-proxy-export="ng serve --host=0.0.0.0 --port=8080 --proxy-config proxy-conf.json"
    alias run-ng-lint-prod-test="ng lint && ng build --prod && ng test"
    alias run-packagr="npm run packagr"
    alias run-trp="ng serve --host=shuvojit.ibfd.org --port=4200 --proxy-config proxy-conf.json"
    alias run-ng="ng serve --host=shuvojit.ibfd.org --port=8080"
    alias run-nerui="ng serve --port=4200 --base-href=/nerui --proxy-config=proxy-conf.json"
    alias run-suds="ng serve --port=4200 --base-href=/suds --proxy-config=proxy-conf.json"
    alias run-suds-prod="ng build && mv dist/suds/assets/etc dist/suds/ && http-server dist/suds --port=4200 --proxy http://localhost:8080"
    # golang
    alias run-go-app="chmod a+x run.sh && ./run.sh local"
    alias run-go-app-dev="chmod a+x run.sh && ./run.sh dev"
    alias go-clean-cache="go clean -modcache"
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
