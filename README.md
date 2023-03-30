# sysfore-Test
Installing Git on CentOS 7
Follow these steps to install the latest Git version on your CentOS 7 system:

The first step is to enable the Wandisco GIT repository. To do that, open your text editor and create a new YUM repository configuration file named wandisco-git.repo in the /etc/yum.repos.d/ directory:

sudo nano /etc/yum.repos.d/wandisco-git.repo
Copy
/etc/yum.repos.d/wandisco-git.repo
[wandisco-git]
name=Wandisco GIT Repository
baseurl=http://opensource.wandisco.com/centos/7/git/$basearch/
enabled=1
gpgcheck=1
gpgkey=http://opensource.wandisco.com/RPM-GPG-KEY-WANdisco
Copy
Import the repository GPG keys with:

sudo rpm --import http://opensource.wandisco.com/RPM-GPG-KEY-WANdisco
Copy
Once the repository is added, install the latest version of Git by running the following command:

sudo yum install git
Copy
To verify the installation type the command below which will print the Git version:

git --version
Copy
The output will look something like below, meaning that Git version 2.18.0 has been successfully installed on your CentOS system.

git version 2.18.0
