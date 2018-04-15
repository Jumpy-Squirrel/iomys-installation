# iomys-installation

Last done: April 2018

- Download Ubuntu 16.04.4 LTS server
- create VM (without easyinstall, 1 core, 1 GB, 20G disk)
- put install image in virtual DVD drive
- Start the VM
  + a single primary partition just for / (manual partitioning)
  + create user while installing
  + Add OpenSSH server
- Before reboot, remove the DVD image
- ssh in
  + ```sudo apt-get install ansible```
  + ```git clone https://github.com/Jumpy-Squirrel/iomys-installation.git```
  + ```cd iomys-installation```
  + ```sudo sh -c 'echo "localhost ansible_connection=local" >> /etc/ansible/hosts'```
  + ```sudo ansible-playbook iomys-installation.yml```

