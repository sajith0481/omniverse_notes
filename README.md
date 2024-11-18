# omniverse_notes
Tracking Notes related to Omniverse installation and operation

Update snap-store:

https://askubuntu.com/questions/1411104/unable-to-update-snap-store-cannot-refresh-snap-store-snap-snap-store-ha

Install VSCode:

https://code.visualstudio.com/docs/setup/linux

Install Git:

https://git-scm.com/downloads/linux

Setup Git:

https://docs.github.com/en/get-started/getting-started-with-git/set-up-git

Disable Apparmor:

https://askubuntu.com/questions/1511854/how-to-permanently-disable-ubuntus-new-apparmor-user-namespace-creation-restric

Install Omniverse virtual workstation on Ubuntu:

https://docs.omniverse.nvidia.com/launcher/latest/it-managed-launcher/install_guide_linux.html

Install Isaac sim Workstation on Ubuntu:

https://docs.omniverse.nvidia.com/isaacsim/latest/installation/install_workstation.html

Install Isaac Sim container headless on AWS:

https://docs.omniverse.nvidia.com/isaacsim/latest/installation/install_advanced_cloud_setup_aws.html

Disable IOMMU Steps:

https://forums.developer.nvidia.com/t/isaac-sim-issue-with-iommu-on-bare-metal-despite-having-turned-it-off/278711

Install ROS2:

https://docs.ros.org/en/jazzy/Installation/Ubuntu-Install-Debs.html

Installing Pegasus Simulator:

https://pegasussimulator.github.io/PegasusSimulator/source/setup/installation.html

Install Cesium for Omniverse Developer Setup:

https://github.com/CesiumGS/cesium-omniverse/blob/v0.23.0/docs/developer-setup/README.md#linux

sudo apt install python3-full
sudo apt install pipx
pipx install conan==1.63.0
pipx ensurepath
pipx completions
echo $0
vim ~/.bashrc
sudo reboot
pipx install cmake-format --include-deps
pipx install black==23.1.0 flake8==7.1.1


Cloning the repo:

  151  cd ~/.ssh
  152  ls
  153  ls -la
  154  ssh-keygen -t ed25519 -C "sajith0481@gmail.com"
  155  ls -la
  156  eval "$(ssh-agent -s)"
  157  ssh-add ~/.ssh/id_ed25519
  158  cat ~/.ssh/id_ed25519.pub
  159  cd ~/Desktop/git/
  160  git clone git@github.com:CesiumGS/cesium-omniverse.git --recurse-submodules
