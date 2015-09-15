# odin
Parrallels Odin Plesk

## Plesk/named/patch_remove_local_bind

On plesk 12.5.30 some named configuration files are local binding on chroot.  
Great for security, but on Proxmox such bind block backups.  
So I cp required files on each action instead of local binding.

To apply : 
    
    /etc/init.d/named stop
    patch /etc/init.d/named < patch_remove_local_bind
    /etc/init.d/named start


