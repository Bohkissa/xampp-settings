# XAMPP Configuration Files

This repository contains backup and modified versions of key XAMPP configuration files. It aims to help developers and students easily switch between default, custom port, and WordPress-optimized setups.

## 📁 Directory Structure

### php/
- `original-php.ini`: Default `php.ini` from a clean XAMPP installation.
- `wordpress-ready-php.ini`: Optimized for WordPress use, including:
  - `max_execution_time = 300`
  - `memory_limit = 512M`
  - `upload_max_filesize = 64M`
  - `post_max_size = 64M`

### apache/
- `original-httpd.conf` / `original-httpd-ssl.conf`: Default Apache configuration files.
- `port-8080-httpd.conf`: Apache configured to listen on port 8080 instead of 80.
- `port-8443-httpd-ssl.conf`: SSL configuration set to use port 8443.
- `wordpress-ready-httpd.conf` / `wordpress-ready-httpd-ssl.conf`: Configuration optimized for WordPress installations with higher resource limits.

## ✅ Use Cases

- Quickly restore original configuration after errors
- Resolve port conflicts (e.g., PID 4 using port 80)
- Prepare XAMPP for modern WordPress development
- Switch easily between development modes

## 💡 Notes

- Always restart Apache after making changes.
- Run XAMPP Control Panel as **Administrator** on Windows.
- Use `http://localhost:8080/` if using the 8080 config.

## 🧑‍💻 Author

Maintained by [Paolo Balzano](https://www.balzanoconsulting.com) – IT Consultant and Technical Teacher.

---

> Feel free to fork or contribute improvements. This repo may be especially useful for students, educators, or developers working in constrained or shared environments.
