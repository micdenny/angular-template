FROM node:12-alpine

RUN apk update && \
    apk add git && \
    git config --global user.email "root@root.root" && \
    git config --global user.name "root" && \
    npm install -g @angular/cli@^9.0.0

RUN ng new --routing true --style scss --strict --interactive false ng-app

WORKDIR /ng-app

RUN ng build && \
    rm -rf dist && \
    rm -f $HOME/.gitconfig

CMD [ "/bin/sh" ]