* enalbe 3d acceleration in virtual box in settings

* install latest build tools
sudo apt-get update
sudo apt install linux-headers-$(uname -r) build-essential dkms

* install virtual box addon
 - On vritualbox, click "device" -> "install addon...". A device is mounted on Desktop folder
 - On Lubuntu terminal, go to the mounted folder and run ./VBoxLinuxAdditions.run

* enable share folder
 - On vritualbox, select "device" -> "shared folder" select a shared folder on your host and a name
 - On Lubuntu terminal, mount your shared folder with command line "sudo mount -t vboxsf -o uid=1000,gid=1000 <shared folder name> ~/share". Note that ~/share should be created first.