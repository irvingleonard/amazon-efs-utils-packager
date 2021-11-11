FROM centos:7

RUN yum -y upgrade
RUN yum -y install git rpm-build make nfs-utils python3.6 botocore
RUN yum -y install https://github.com/irvingleonard/stunnel-packages/releases/download/el7_5.60-1/stunnel-5.60-1.el7.x86_64.rpm

WORKDIR /root
RUN git clone https://github.com/aws/efs-utils

WORKDIR /root/efs-utils
ENTRYPOINT ["make", "rpm"]
