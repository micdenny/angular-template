FROM node:12-alpine

RUN apk update && \
    apk add git && \
    git config --global user.email "root@root.root" && \
    git config --global user.name "root" && \
    npm install -g @angular/cli@^10.0.0

RUN ng new --routing true --style scss --strict --interactive false ng-app

WORKDIR /ng-app

RUN ng add @angular/material --interactive false && \
    ng g module navigation --module app --interactive false && \
    ng generate @angular/material:navigation navigation --export --interactive false && \
    ng g module dashboard --module app --interactive false && \
    ng generate @angular/material:dashboard dashboard --export --interactive false && \
    sed -i 's+<!-- Add Content Here -->+<ng-content></ng-content>+g' ./src/app/navigation/navigation.component.html && \
    echo -e "<app-navigation>\n    <app-dashboard></app-dashboard>\n</app-navigation>" > ./src/app/app.component.html && \
    git add . && \
    git commit -m "Angular material design"

RUN ng build && \
    rm -rf dist

CMD [ "/bin/sh" ]