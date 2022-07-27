# Realtime-Project-2
Requirements:
   1. Jenkins server
   2. Ansible server
   3. Webapp server
   
 Now need to enable the ssh connection between three servers
   --> Enable ssh connection from vi /etc/ssh/sshd_config (Permit root login-yes, Passwordauthentication- yes)
   --> systemctl restrt sshd
   
  Enable passwordless authentication among all three servers
     -->ssh-keygen (This command is to generate sshkey)
     -->Now copy the key the destination server (ssh-copy-id root@private IPV4 address)
     ---> Once we added the key then we can login to the other server via ssh without entering the password ssh root@private IPV4 address)
     
   Then need to install publish over ssh plugin in Jenkins and add all the three servers under Manage Jenkins-->Configure system
    (Need to give hostname(public Ip address), Username(ubuntu) and password (password need to create if not crated- cmd# passwd ubuntu)
