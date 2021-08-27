# ssh PortForwarding
https://help.ubuntu.com/community/SSH/OpenSSH/PortForwarding
ssh -g -f -N -L 
ssh -g -N -f -D 0.0.0.0:1081 10.8.0.2
proxychains4 -f /etc/proxychains_socks.conf 


# nfs
/xxxx  *(rw,insecure,sync,no_root_squash,no_subtree_check,all_squash,anonuid=0,anongid=0)

# jupyter
nohup jupyter-lab --allow-root&
~/.jupyter/jupyter_notebook_config.py
c.NotebookApp.ip = '*'
#c.NotebookApp.password = u'sha1:da92c1f689da:ee60442f8adf965e9663516fe55ecf29cec3f826'
c.NotebookApp.open_browser = False
c.NotebookApp.port = 18080
c.MappingKernelManager.root_dir = '/home/hua/.jupyter_run/root' 

# docker
sudo usermod -aG docker $USER
docker run -tid -v /usr:/usr -v /home/:/home -v /etc/localtime:/etc/localtime  -p 5024:22 -e POD_NODE_NAME=10.154.243.240  --privileged=true --name build_usr2 xxxx /bin/bash

# cachefilesd
https://blog.csdn.net/luckytanggu/article/details/78476634  
sudo aptitude  install cachefilesd  
cat /etc/cachefilesd.conf  --delete selinux 
/etc/default/cachefilesd  ---set run=yes  
systemctl restart cachefilesd 
mount -t nfs -o fsc 
