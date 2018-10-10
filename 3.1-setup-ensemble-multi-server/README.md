# Goal

Goal is to install zookeeper for distributed service discovery in multiple node with quorum member configuration. This installation process implements ZooKeeper quorum using ansible.

# Prerequisites

Java must be installed in the OS to run zookeeper. Since Ansible is used to complete this challenge so install Ansible in workstation and install java in the remote machines, You can also find Ansible java installation role [here] (https://github.com/shudarshon/scripts/tree/master/ansible/role-collection/roles).


# Procedure

* If you not to choose manage infrastructure with terraform then Change `hosts` and `play.yml` file accordingly. Remember to change the variable label of ansible in var file (defaults/main.yml) of anisble role. Then run `ansible-playbook -i hosts play.yml`.

* If you choose terraform then simply use:
    * make init - only first time for installing necessary plugin
    * make plan - see the reosurces going to be changed by terraform
    * make apply - apply change
    * make destroy - remove infrastructure components and rollback

# Test

To check zookeeper status, use `cd /opt/zookeeper* && sudo -u zookeeper ./bin/zkServer.sh status` command in each servers. It should work on both ubuntu & centos.

# Issue

If you find any issue then create it in the GitHub repo. For any suggestion, information or any help mail me at sdrsn.chaki@gmail.com. You can get me on my blog [here](www.shudarshon.com).
