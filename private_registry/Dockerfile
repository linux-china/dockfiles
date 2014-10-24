FROM registry:0.8.1
MAINTAINER linux_china linux_china@hotmail.com

#RUN apt-get -y install libmysqlclient-dev
#RUN pip install mysql-python

ADD ./config_sample.yml /dockerregistry/config/config_sample.yml

ENV SEARCH_BACKEND sqlalchemy
#ENV SQLALCHEMY_INDEX_DATABASE mysql://root:mysecretpassword@192.168.1.22:3306/docker_registry
ENV SQLALCHEMY_INDEX_DATABASE sqlite:////opt/sqlitedb/reg.db
ENV STORAGE_PATH /opt/registry

ENV MIRROR_SOURCE https://registry-1.docker.io
ENV MIRROR_SOURCE_INDEX https://index.docker.io

CMD exec docker-registry