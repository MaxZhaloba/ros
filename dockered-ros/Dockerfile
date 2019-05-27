FROM ros
RUN apt-get -y update && \
    apt-get -y install software-properties-common && \
    add-apt-repository ppa:git-core/ppa && \
    apt-get -y upgrade && \
    apt-get -y install mc && \
    apt-get -y install terminator && \
    apt-get -y install git
#CMD bash
CMD /usr/bin/terminator -u