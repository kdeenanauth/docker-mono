FROM kdeenanauth/mono:1.0

MAINTAINER Kevin Deenanauth <kevin@deenanauth.com>

RUN mkdir -p /usr/src/app/source /usr/src/app/build
WORKDIR /usr/src/app/source

ONBUILD COPY . /usr/src/app/source
ONBUILD RUN nuget restore -NonInteractive
ONBUILD RUN xbuild /property:Configuration=Release /property:OutDir=/usr/src/app/build/
ONBUILD WORKDIR /usr/src/app/build