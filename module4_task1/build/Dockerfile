# Container image that runs your code
FROM golang:1.15.8-buster

# WORKDIR /module4_task1

RUN rm -rf /usr/local/go
RUN apt update
RUN apt install git
RUN git clone https://github.com/Elizbeh/holbertonschool-validation.git
RUN mv holbertonschool-validation/* .
RUN rm -rf holbertonschool-validation
RUN apt install xz-utils
RUN apt install make -y

# RUN curl -sL https://deb.nodesource.com/setup_16.x | bash -
# RUN apt update
# RUN apt install nodejs -y
# RUN wget https://nodejs.org/dist/v16.19.0/node-v16.19.0-linux-x64.tar.xz
# RUN tar -xf node-v16.19.0-linux-x64.tar.xz
# RUN cd node-v16.19.0-linux-x64
# RUN cd node-v16.19.0-linux-x64 && cp -rp /module4_task1/node-v16.19.0-linux-x64/ /home/
# RUN ls -la /usr/bin/nodejs
# RUN cp -p /home/node-v16.19.0-linux-x64/bin/node /usr/bin/nodejs
# RUN apt install npm=8.19.3
# RUN apt install npm -y 
# RUN npm install -g npm@8.19.3
# RUN update-alternatives --install /usr/bin/npm npm /usr/bin/nodejs 1

RUN curl -fsSL https://deb.nodesource.com/setup_16.x | bash -
RUN apt install nodejs
RUN npm install -g markdownlint-cli

# RUN apt install hugo -y
# RUN curl -L https://github.com/gohugoio/hugo/releases/download/v0.109.0/hugo_extended_0.109.0_linux-amd64.deb -o hugo.deb
# RUN apt install ./hugo.deb
# RUN rm hugo.deb
RUN apt install zip -y
RUN apt install sudo -y

# Copies your code file from your action repository to the filesystem path `/` of the container
# COPY module4_task1 /

# Code file to execute when the docker container starts up (`entrypoint.sh`)
# ENTRYPOINT ["sh", "-c", "cd module4_task1"]
