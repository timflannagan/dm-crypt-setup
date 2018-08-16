Normal dm-crypt setup:
======================
1. Format: cryptsetup luksFormat **device_path**
2. Open: cryptsetup luksOpen **device_path** **luks_volume_name**
3. Setup fs: mkfs.**fs_type** /dev/mapper/**luks_volume_name**
4. Setup mount: mount -t '**fs_type**' /dev/mapper**luks_volume_name** **mount_location**

To-Do:
======
1. Place task flow into tasks/
2. Set defaults
3. Specify variables and role instance in main.yml

Notes:
======
1. Ansible's **crypttab** module seems fairly useless
