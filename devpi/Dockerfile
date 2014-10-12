# Version: 0.0.1
FROM base/archlinux
MAINTAINER José Luis Lafuente "jl@lafuente.me"
ENV REFRESHED_AT 2014-10-09

RUN [ "pacman", "-Syu", "--needed", "--noconfirm", "python", "python-pip", "sqlite" ]
RUN pip install -U devpi-server devpi-web

ENTRYPOINT [ "devpi-server" ]
CMD [ "--port", "4040", "--host", "0.0.0.0"]
