# Initial configurations
Define those variable in vars/secret.yml:
* username
* openvpn_file

Copy those files to the directory files:
* cna-windows-k9-installer-6-3-4-en.exe
* jre-8u311-windows-i586.exe

Install Ansible:
```bash
sudo pip install ansible
sudo pip install paramiko
```
# VPN configuration
Configure the VPN connection with the file **.ovpn** in the GUI. After the configuration, execute the command bellow to enable the VPN connection to resolve all the domains in the **inf.ufes.br**.
```bash
nmcli connection modify VPN_INTERFACE_NAME ipv4.dns-search 'inf.ufes.br'
```