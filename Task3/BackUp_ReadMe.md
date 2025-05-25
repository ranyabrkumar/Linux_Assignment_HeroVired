# APACHE_NGINUX_BKPUP.sh

This script automates the backup of Apache and Nginx configuration files and web content. It creates compressed archives and logs the backup process.

## Features

- Backs up Apache (`/etc/apache2`, `/var/www/html`) and Nginx (`/etc/nginx`, `/usr/share/nginx/html`) directories. [using tar -xcf command] 
- Stores backups in `$HOME/backups/apache` and `$HOME/backups/ngnix`.
- Verifies backup archive integrity. [verify the backup using tar -tzf command whether the archive can be read without any  error]
- Logs all actions and results. [ logs are also captured in backup folders]

## Usage

1. Place the script on your Linux system.

2. Run the script:
    ```bash
    ./APACHE_NGINUX_BKPUP.sh
    ```

## Notes

- Run as a user with read access to the configuration and web directories.
- Backup archives and logs are stored in your home directory under `apache_backups` and `nginx_backups`.
- Check the log files for backup status and integrity verification.

## License

MIT License.
