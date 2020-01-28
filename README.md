# System-Settings
Information regarding the apps and settings I use on my computers

#Install yakuake
sudo apt-get install yakuake

#Install Vim
sudo apt-get install vim

#Install git
sudo apt-get install git

#Show current git branch in terminal, execute the following steps
vim ~/.bashrc
#This opens the ~/.bashrc file, append the following to it.
      parse_git_branch() {
                            git branch 2> /dev/null | sed -e '/^[^*]/d' -e 's/* \(.*\)/(\1)/'
                          }
      export PS1="\u@\h \[\e[32m\]\w \[\e[91m\]\$(parse_git_branch)\[\e[00m\]$ "

#Save the above and execute the following command
source ~/.bashrc

#Install CopyQ - clipboard manager
sudo apt-get install copyq
