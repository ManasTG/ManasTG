# RCLONE
> Used to clone file to google drive or vice-versa

### To sync the local file location to the google drive's `college` folder
```bash
rclone sync '/run/media/krane/Local Disk 2/Manas/College' gdrive:college
```

### To sync the folder and showing the progress of it
```bash
rclone sync '/run/media/krane/Local Disk 2/Manas/College' gdrive:college --progress
```

### To check if there are any problem IF we sync the file to google drive
```bash
rclone sync '/run/media/krane/Local Disk 2/Manas/College' gdrive:college --dry-run
```

### Format of rclone
```bash
rclone sync SOURCE DESTINATION
```
