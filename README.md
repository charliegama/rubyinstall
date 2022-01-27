# rubyinstall

# Install Dependencies.

sudo apt-get update
sudo apt-get install git-core curl zlib1g-dev build-essential libssl-dev libreadline-dev libyaml-dev libsqlite3-dev sqlite3 libxml2-dev libxslt1-dev libcurl4-openssl-dev software-properties-common libffi-dev


# Key Public for Install RVM

gpg --keyserver keyserver.ubuntu.com --recv-key 409B6B1796C275462A1703113804BB82D39DC0E3 7D2BAF1CF37B13E2069D6956105BD0E739499BDB


# Install stable version ruby 

curl -sSL https://get.rvm.io | bash -s
source /etc/profile.d/rvm.sh

# Install  Version Ruby.
rvm install 2.6.6 
rvm use 2.6.6 --default


# Add RVM to PATH for scripting. Make sure this is the last PATH variable change.
export PATH="$PATH:$HOME/.rvm/bin"

# User Add ruby gem. 
sudo usermod -a -G rvm `user`

# verify version ruby 
ruby -v

