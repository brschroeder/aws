# Amazon Web Services

## Getting Started

need access key id on local machine

Log into the EC2 instance using SSH as user centos. The argument to the "-i" option is the /location/filename of your private key (i.e. the *.pem file you downloaded from the AWS Console).

```{bash}
ssh -i brett-20160630.pem centos@ec2-54-149-104-27.us-west-2.compute.amazonaws.com
```
You should not be prompted for any password since the private key in the *.pem file is effectively your password - if you look at ~/.ssh/authorized_keys, you will notice that this file has already been pre-populated with the public key that corresponds to the private key in your *.pem file.

### Updating and installing software

Now it is just like any other real machine. Switch to the root user as follows

```bash
sudo su - 
```



then yum repolist to list of repositories configured. Need to add EPEL repository as follows (need to install wget first since it is not in default install)

yum install wget
wget http://dl.fedoraproject.org/pub/epel/7/x86_64/e/epel-release-7-7.noarch.rpm
rpm -ivh epel-release-7-7.noarch.rpm
yum update
yum install R

install aws bundle if not using amazon linux (as root)
wget https://s3.amazonaws.com/aws-cli/awscli-bundle.zip
unzip awscli-bundle.zip



need to run "aws configure" before using any aws cli tool

for yr in 2005 2006; do aws s3 cp $yr.csv.bz2 s3://brs-analytics/airline/$yr.csv.bz2; done
