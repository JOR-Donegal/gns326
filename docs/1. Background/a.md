# Installation
The easiest way (IMHO) to use GNS3 is to build a UB2404 VM and install eveything on it nativly. You must have nested virtualization enabled for this to work. 

I used the script below on a UB2204 VM in Azure labs. 
Read through the script and see if you can follow what I did!

```
# Configure server to add a GUI
sudo apt update
sudo apt upgrade -y
sudo apt install xfce4
sudo apt install xrdp -y
sudo ufw allow 3389/tcp
sudo systemctl enable xrdp
sudo systemctl restart xrdp

# Add Chrome
sudo apt-get install fonts-liberation
sudo apt install xdg-utils -y
wget https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb
sudo dpkg -i google-chrome-stable_current_amd64.deb
rm google-chrome-stable_current_amd64.deb

# Add VSCode
wget https://code.visualstudio.com/sha/download?build=stable&os=linux-deb-x64
sudo apt install ./code_1.105.1-1760482543_amd64.deb

# Add GITHUB Desktop
wget -qO - https://mirror.mwt.me/shiftkey-desktop/gpgkey | gpg --dearmor | sudo tee /usr/share/keyrings/mwt-desktop.gpg > /dev/null
sudo sh -c 'echo "deb [arch=amd64 signed-by=/usr/share/keyrings/mwt-desktop.gpg] https://mirror.mwt.me/shiftkey-desktop/deb/ any main" > /etc/apt/sources.list.d/mwt-desktop.list'
sudo apt update
sudo apt install github-desktop -y

# Add Putty
sudo add-apt-repository universe
sudo apt update
sudo apt install -y putty

# Add GNS3
sudo add-apt-repository ppa:gns3/ppa
sudo apt update                                
sudo apt install gns3-gui gns3-server -y

# IOU support
sudo dpkg --add-architecture i386
sudo apt update
sudo apt install gns3-iou -y

# Add docker (remove defaults first)
sudo apt remove docker docker-engine docker.io
sudo snap remove docker
sudo apt-get install apt-transport-https ca-certificates curl software-properties-common -y
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
sudo add-apt-repository \
"deb [arch=amd64] https://download.docker.com/linux/ubuntu \
   $(. /etc/os-release && echo $VERSION_CODENAME) stable"
sudo apt update
sudo apt install docker-ce -y
sudo usermod -aG ubridge,libvirt,kvm,wireshark,docker $(whoami)
```