install Plymouth

copy sukuna folder to /usr/share/plymouth/themes

edit the file: (/etc/mkinitcpio.conf)
add plymouth in HOOKS

edit the file: (/etc/default/grub)
find GRUB_CMDLINE_LINUX_DEFAULT and replace it with this
GRUB_CMDLINE_LINUX_DEFAULT="quiet splash"

run these commands:
sudo mkinitcpio -p linux
sudo grub-mkconfig -o /boot/grub/grub.cfg

and then run this code and reboot:
sudo plymouth-set-default-theme -R sukuna
