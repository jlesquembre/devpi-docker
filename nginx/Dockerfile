# Version: 0.0.1
FROM base/archlinux
MAINTAINER José Luis Lafuente "jl@lafuente.me"
ENV REFRESHED_AT 2014-10-09

RUN [ "pacman", "-Syu", "--needed", "--noconfirm", "nginx" ]

ADD conf/global.conf /etc/nginx/conf.d/
ADD conf/nginx.conf /etc/nginx/

EXPOSE 80
EXPOSE 443

CMD [ "nginx" ]
