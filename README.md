# omniverse_notes
Tracking Notes related to Omniverse installation and operation

Install VSCode:

https://code.visualstudio.com/docs/setup/linux

Install Git:

https://git-scm.com/downloads/linux

Setup Git:

https://docs.github.com/en/get-started/getting-started-with-git/set-up-git

Disable IOMMU Steps:

Hi. You can leave SVM Mode enabled.
The IOMMU setting should be on a different page. Look for something similar below.
Advanced\AMD CBS\NBIO Common Options\IOMMU

After a reboot, you can verify that IOMMU is disabled if the two commands below do no print any outputs.

sudo dmesg | grep -e DMAR -e IOMMU

ls /sys/kernel/iommu_groups/

Hi. You might need help from the motherboard manufacturer to disable IOMMU for your specific hardware.

Another thing to try is to disable SVM mode like before.
Also try disable IOMMU in grub with similar commands below:

sudo bash -c 'echo GRUB_CMDLINE_LINUX="amd_iommu=off" >> /etc/default/grub'
sudo update-grub
sudo reboot
