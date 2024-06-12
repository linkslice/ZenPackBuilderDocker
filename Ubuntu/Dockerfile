FROM ubuntu:22.04
RUN apt update
RUN apt install -y git python2.7 python-setuptools
RUN update-alternatives --install /usr/bin/python python /usr/bin/python2 2
WORKDIR /
RUN git clone https://github.com/linkslice/CustomScriptBuilder.git
#ADD CustomScriptBuilder /
CMD ["./makepack.sh -a $AUTHOR -n $NAME -v $VERSION"]
