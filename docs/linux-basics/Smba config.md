```
sudo nano /etc/samba/smb.conf
```

`[name]`
   `#This is the main storage drive with media files`
   `path = /`
   `browsable = yes`
   `writable = yes`
   `guest ok = no`
   `valid users = hive`
   `create mask = 0660`
   `directory mask = 0770`
   `veto files = /.Trash*/lost+found/`
   `delete veto files = yes`