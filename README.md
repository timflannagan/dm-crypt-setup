Normal dm-crypt setup:
======================
1. Format: cryptsetup luksFormat '*device_path*'
2. Open: cryptsetup luksOpen '*device_path*' '*luks_volume_name*'
3. Setup fs: mkfs*'fs_type*' /dev/mapper/'*luks_volume_name*'
4. Setup mount: mount -t '*fs_type*' /dev/mapper'*luks_volume_name*' '*mount_location*'
