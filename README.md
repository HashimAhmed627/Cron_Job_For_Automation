# Cron Job For Automation ⏰🤖

## Objective 
This project demonstrates how to automate a task using a cron job on a Linux server. In this case, the cron job will run a script to back up a directory every day at midnight.

## Tasks Covered
- Creating a simple bash script for backup.
- Setting up a cron job to run the script daily at midnight.

__________________________________________________________________________________________________________________________________
### Bash Script for Daily Backups
![bash script](https://github.com/user-attachments/assets/eb4d4a5a-2a33-43bd-9b97-e0d3500fe9b2)

Let's break down this script: 

- `#! /bin/bash`: This is called a shebang and tells the system that this script should be run using the Bash shell.
- `TIMESTAMP=$(date +"%F")`: This line gets the current date and stores it in the `TIMESTAMP` variable. 

  - The `date +"%F"` command formats the date as `YYYY-MM-DD` (e.g., `2025-02-03`).

- `BACKUP_DIR= "/home/cyberhashim/backups"`: This sets the `BACKUP_DIR` variable to the path where the backup will be saved (in this case, `/home/cyberhashim/backups`).

- `SOURCE_DIR= "/home/cyberhashim/data"`: This sets the `SOURCE_DIR` variable to the path of the directory that is being backed up (in this case, `/home/cyberhashim/data`).

- `tar -czf $BACKUP_DIR/backup-$TIMESTAMP.tar.gz $SOURCE_DIR`: This command creates a tarball (compressed archive) of the `SOURCE_DIR` variable.

  - `tar`: This command is used to create or extract tarballs
  - `-c`: Creates a new archive
  - `-z`: Compresses the archive using gzip
  - `-f`: Specifies the name of the output file
  - `$BACKUP_DIR/backup-$TIMESTAMP.tar.gz`: This is the file where the backup will be saved. It includes the timestamp, so each backup will have a unique name.
  - `$SOURCE_DIR`: The directory to be backed up (`/home/cyberhashim/data`)

_________________________________________________________________________________________________________________________________
### Setting Up The Cron Job
![crontab -e](https://github.com/user-attachments/assets/d2114828-2339-4949-aad0-6865f889b45e)
![cronjob explanation](https://github.com/user-attachments/assets/b1354580-cb22-4a42-8854-a94b98e09860)
![my cronjob](https://github.com/user-attachments/assets/0a6c3a2f-8686-43ea-80fa-a63186849d88)



## Lessons Learned
