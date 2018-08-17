Normal dm-crypt setup:
======================
1. Format: cryptsetup luksFormat **device_path**
2. Open: cryptsetup luksOpen **device_path** **luks_volume_name**
3. Setup fs: mkfs.**fs_type** /dev/mapper/**luks_volume_name**
4. Setup mount: mount -t '**fs_type**' /dev/mapper**luks_volume_name** **mount_location**

To-Do:
======
- [x] Place task flow into tasks/
- [x] Set defaults
- [ ] Specify variables and role instance in main.yml

Notes:
======
1. Ansible's **crypttab** module seems fairly useless.
2. Can't use variables as keys in Ansible.
3. Expect/response block will time out if variable is used as key in response control.
