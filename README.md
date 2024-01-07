# openstack_centos8_packstack

sed -i 's/mirrorlist/#mirrorlist/g' /etc/yum.repos.d/CentOS-*

sed -i 's|#baseurl=http://mirror.centos.org|baseurl=http://vault.centos.org|g' /etc/yum.repos.d/CentOS-*


dnf update -y

dnf config-manager --enable powertools

yum  install centos-release-openstack-victoria.noarch

sed -i 's/mirrorlist/#mirrorlist/g' /etc/yum.repos.d/*

sed -i 's|#baseurl=http://mirror.centos.org|baseurl=http://vault.centos.org|g' /etc/yum.repos.d/*

dnf update -y

dnf install -y openstack-packstack

hostnamectl set-hostname myopenstack.example.com
hostname  myopenstack.example.com

ifconfig
vi /etc/hosts
172.31.18.252   myopenstack.example.com  myopenstack


dnf install network-scripts -y

$ sudo systemctl disable firewalld
$ sudo systemctl stop firewalld
$ sudo systemctl disable NetworkManager
$ sudo systemctl stop NetworkManager
$ sudo systemctl enable network
$ sudo systemctl start network


setenforce 0

packstack --gen-answer-file=my.txt

packstack --answer-file=my.txt






