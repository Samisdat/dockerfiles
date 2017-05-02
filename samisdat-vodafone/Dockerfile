FROM ruby:2.2.7
MAINTAINER Samisdat bastian.pertz@vodafone.com

RUN git config --global --add oh-my-zsh.hide-dirty 1

RUN gem install libv8 --version 3.11.8.0 
RUN gem install rubocop 
RUN gem install bundle 
RUN gem install jslint 
RUN gem install scss-lint --version 0.32.0
RUN gem install middleman
RUN gem install middleman-svg-fallback
RUN gem install middleman-imageoptim
RUN gem install middleman-webp
RUN gem install rails-erb-lint
RUN gem install pre-commit
RUN gem install minitest
RUN gem install foreman
RUN gem install tilt -v '1.4.1'

# install node
RUN curl -sL https://deb.nodesource.com/setup_7.x | bash -
RUN apt-get install -y nodejs

# install same node packages
RUN npm install -g grunt-cli
RUN npm install -g eslint
RUN npm install -g handlebars 
RUN npm install -g typescript

# install git
RUN apt-get install -y git-core
RUN apt-get install -y git-flow

## install oh-my-zsh
RUN apt-get install -y zsh
RUN curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh | bash -

# install tig from source while the one from package is not working
RUN mkdir /root/tig
RUN git clone https://github.com/jonas/tig.git /root/tig
RUN apt-get install -y build-essential
RUN apt-get install -y ncurses-dev
WORKDIR /root/tig
RUN make
RUN make install
RUN ln -s /root/bin/tig /bin/tig
RUN apt-get remove -y build-essential
RUN apt-get remove -y ncurses-dev
RUN rm -rf /root/tig

