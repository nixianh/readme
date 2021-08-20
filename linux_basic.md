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
