# Goal

Goal is to install zookeeper for distributed service discovery in a single node with quorum member configuration. This installation process implements ZooKeeper quorum using ansible.

# Prerequisites

Java must be installed in the OS to run zookeeper. Since Ansible is used to complete this challenge so install Ansible in workstation and install java in the remote machine, You can also find Ansible java installation role [here] (https://github.com/shudarshon/scripts/tree/master/ansible/role-collection/roles).

# Procedure

Change `hosts` and `play.yml` file accordingly. Then run `ansible-playbook -i hosts play.yml`.

# Issue

If you find any issue then create it in the GitHub repo. For any suggestion, information or any help mail me at sdrsn.chaki@gmail.com. You can get me on my blog [here](www.shudarshon.com).
