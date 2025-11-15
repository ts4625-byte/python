cat <<EOF | sudo tee /etc/apt/sources.list 
● deb http://archive.ubuntu.com/ubuntu noble main universe restricted multiverse 
● deb http://archive.ubuntu.com/ubuntu noble-updates main universe restricted multiverse 
● deb http://archive.ubuntu.com/ubuntu noble-security main universe restricted multiverse 
● EOF 
● sudo apt update 
● Install QEMU and related packages on Ubuntu 24.04 
● sudo apt install -y qemu-system-x86 qemu-utils libvirt-clients libvirt-daemon-system 
bridge- utils virtinst 
● Download Alpine Linux ISO (lightweight Linux distro) 
● wget https://dl-cdn.alpinelinux.org/alpine/v3.18/releases/x86_64/alpine-standard-3.18.0- 
x86_64.iso 
● Create a 2 GB virtual hard disk for Alpine VM 
● qemu-img create -f qcow2 alpine-vm.qcow2 2G 
● Launch the Alpine Linux VM with QEMU (headless mode) 
● qemu-system-x86_64 \ 
● -m 512M \ 
● -cdrom alpine-standard-3.18.0-x86_64.iso \ 
● -hda alpine-vm.qcow2 \ 
● -boot d \ 
● -net nic -net user \ 
● -nographic 
● Login at the Alpine Linux prompt 
● localhost login: root 
● Password:[pressEnter]
