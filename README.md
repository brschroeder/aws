# Amazon Web Services

## Getting Started

need access key id on local machine

### Updating and installing software

Do sudo su - to gain root access, then yum repolist to list of repositories configured. Need to add EPEL repository as follows (need to install wget first since it is not in default install)

yum install wget
wget http://dl.fedoraproject.org/pub/epel/7/x86_64/e/epel-release-7-7.noarch.rpm
rpm -ivh epel-release-7-7.noarch.rpm




install aws bundle if not using amazon linux

need to run "aws configure" before using any aws cli tool

for yr in 2005 2006; do aws s3 cp $yr.csv.bz2 s3://brs-analytics/airline/$yr.csv.bz2; done
