# Ansible Role: build Bitcoin Core and Run in Ubuntu 20.04 
Build Bitcoin Core and Run in Ubuntu servers.

This role install Bitcoin Full Node on Ubuntu 20.04 and dependencies. You will likely need to do some additional configuration work before starting this role, such as changing variables, describing the ettings that will be used for you.

# Minimum Hardware Requirements
****2 core
2GB RAM
500GB of free disk space

# Dependencies
For Ubuntu to 20.04  Bitcoin PPA has not released libdb-4.8 for Focal Fossa (Ubuntu 20.04) yet. This playbook install libdb-4.8 from the source code.
This playbook installs the following dependenciesansible :
     build-essential
     libtool
     autotools-dev
     automake
     pkg-config
     bsdmainutils
     python3
     libevent-dev
     libboost-dev
     libsqlite3-dev
     sed
     g++
     make

# Role Variables
Before starting, you need to change the value of the following variables:
```
bitcoin_rpcuser: username
bitcoin_rpcpassword: password
bitcoin_rpcbind: "127.0.0.1"
```

# Example Playbook
```
- hosts: server
  roles:
    - ansible-bitcoin
```

