# Kernel Logs Automation

A Linux automation solution that periodically collects kernel logs, compresses them, and uploads the archives to Dropbox.

## Features

* Collect kernel logs from the last hour
* Generate timestamped log files
* Compress logs automatically
* Upload archives to Dropbox
* Automatic cleanup of temporary files
* Scheduled execution using systemd timers

## Technologies

* Bash
* systemd
* journalctl
* tar
* dbxcli

## Workflow

1. Retrieve kernel logs from the last hour.
2. Save logs to a timestamped file.
3. Compress the file.
4. Upload the archive to Dropbox.
5. Remove temporary files.
6. Repeat automatically according to the timer schedule.

## Requirements

* Linux
* systemd
* dbxcli
* Dropbox account configured with dbxcli

## Installation

```bash
chmod +x collect-logs.sh
systemctl --user enable kernel-logs.timer
systemctl --user start kernel-logs.timer
```

## Learning Outcomes

This project demonstrates Linux automation, system monitoring, log management, scheduled tasks, and cloud integration using shell scripting.
