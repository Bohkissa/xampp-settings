# XAMPP Configuration Files Backup & Custom Setups

This repository provides a structured set of Apache and PHP configuration files for XAMPP on Windows. It includes original backups, alternative port versions (8080/8443), and performance-optimized setups for WordPress and heavy plugin usage.

## 📁 Folder Structure

### `/original/`
Contains the original configuration files from a fresh XAMPP installation:
- `httpd.conf`
- `httpd-ssl.conf`
- `php.ini`

### `/port-8080-8443/`
Apache configuration files modified to use alternative ports:
- `httpd.conf` → Port `8080` instead of `80`
- `httpd-ssl.conf` → Port `8443` instead of `443`

Use this set if port 80 is blocked (e.g., PID 4 "System" issue on Windows).

### `/wordpress/`
Optimized configuration for WordPress installations and plugins that require:
- Higher execution time
- Larger file upload limits
- Increased memory

Included files:
- `php.ini` with increased limits:
  - `max_execution_time = 300`
  - `memory_limit = 512M`
  - `upload_max_filesize = 64M`
  - `post_max_size = 64M`
  - `max_input_vars = 5000`

- `httpd.conf` and `httpd-ssl.conf` preconfigured for:
  - Ports 8080 and 8443
  - Optional Apache tweaks for longer timeouts and larger requests

## ✅ How to Use

1. Stop Apache from XAMPP Control Panel.
2. Backup your current config files (if needed).
3. Replace the config files with the ones from your desired folder.
4. Restart XAMPP Control Panel as **Administrator**.
5. If using the 8080 setup, access your site via:
http://localhost:8080/
https://localhost:8443/

## 🧪 Verify Configuration

To confirm PHP settings, create a file named `info.php` in `htdocs/` with the following content:

```php
<?php phpinfo(); ?>