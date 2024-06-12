FROM centos:centos7
RUN yum update -y
RUN yum install epel-release -y
RUN yum install git python-setuptools -y
WORKDIR /
RUN git clone https://github.com/linkslice/CustomScriptBuilder.git
#ADD CustomScriptBuilder /
CMD ["./makepack.sh -a $AUTHOR -n $NAME -v $VERSION"]
