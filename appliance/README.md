# Building the appliance

## Making VM

* Download atomic iso from http://www.projectatomic.io
* If needed, update fedora version (and the other settings) in the ks.cfg
* Run build.sh to make kickstart iso

* Create a VM with 1GB ram, 1 CPU, 20GB drive
* Attach two CD drives to that VM and put atomic image and ks.iso in them
* Boot with ks=cdrom:/ks.cfg option

## Deploying MDG onto the VM

* Prepare banners by calling `ansible-playbook -i inventory appliance.yml -k`
* Do MDG install using ansible.