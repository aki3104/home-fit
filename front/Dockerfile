FROM node:12.5.0-alpine

ENV HOME="/app/src" \
    LANG=C.UTF-8 \
    TZ=Asia/Tokyo 

WORKDIR ${HOME}

RUN apk update && \
    apk upgrade && \
    npm install -g npm && \
    npm install -g @vue/cli \ 
    vue add storybook

ENV HOST 0.0.0.0
EXPOSE 3000