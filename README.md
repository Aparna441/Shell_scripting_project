# Linux Server Health Monitoring and Automated Alerting

## Project Overview

This project automates basic Linux server health checks using Bash scripting.

It monitors CPU utilization, memory utilization, disk usage, server uptime, and failed systemd services. The script records timestamped results and identifies resource utilization that exceeds configurable thresholds.

## Features

* CPU utilization monitoring
* Memory utilization monitoring
* Disk space monitoring
* Server uptime reporting
* Failed systemd service detection
* Configurable warning and critical thresholds
* Timestamped log generation
* Cron-based scheduled execution
* Foundation for email and cloud notification integrations

## Technology Stack

* Ubuntu Linux
* Bash Shell Scripting
* Linux command-line utilities
* AWK and GREP
* Cron
* Git and GitHub

## Prerequisites

* A Linux system with Bash
* Required system utilities such as `awk`, `df`, `free`, and `top`
* `systemd` for systemd service checks
* Appropriate permissions to read system information

## How to Run

Clone the repository:

```bash
git clone YOUR_REPOSITORY_URL
cd linux-server-health-monitor
```

Make the script executable:

```bash
chmod +x health_monitor.sh
```

Execute it:

```bash
./health_monitor.sh
```

## Automation

Configure Cron to execute the monitoring script at regular intervals.

Example: run every five minutes.

```cron
*/5 * * * * /absolute/path/to/health_monitor.sh
```

## Logging

Each execution generates a timestamped log containing server health information and detected warnings or critical conditions.

## Future Enhancements

* Email and cloud-based notifications
* Support for multiple servers
* Configurable service health checks
* Automated log rotation and retention
* Unit tests for threshold evaluation
* JSON output for integration with monitoring platforms
* Integration with Prometheus or other observability tools
* Secure remote execution through SSH

## Disclaimer

This project is intended for learning and demonstration. Validate metric calculations, permissions, alert delivery, and failure handling before using it in production.
