# One-Tier Web Application with Squid Whitelisting

This project sets up a one-tier web application using an EC2 instance and implements a Squid Proxy server to whitelist specific URLs. It ensures that the EC2 instance can only access the whitelisted URLs, with all other traffic being denied.

## Table of Contents
- [Phase 1: One-Tier Website using EC2](#phase-1-one-tier-website-using-ec2)
- [Phase 2: Set Up Squid Proxy for Whitelisting](#phase-2-set-up-squid-proxy-for-whitelisting)
- [Usage](#usage)
- [Configuration](#configuration)
- [Contributing](#contributing)
- [License](#license)

## Phase 1: One-Tier Website using EC2

In this phase, we create a one-tier web application using an EC2 instance. Follow these steps:

1. **Launch an EC2 instance:**
   - Choose an appropriate AMI and instance type.
   - Configure security groups to allow incoming traffic on ports 80 and 443 for web traffic.
   - Connect to the EC2 instance and deploy your web application.

## Phase 2: Set Up Squid Proxy for Whitelisting

In this phase, we set up a Squid Proxy server to whitelist specific URLs. Follow these steps:

1. **Launch a Squid Proxy instance:**
   - Create a new EC2 instance and choose an appropriate AMI and instance type.
   - Configure security groups to allow incoming traffic on port 3128 for Squid Proxy.
   - Connect to the Squid Proxy instance.

2. **Install and Configure Squid:**
   - Install Squid on the Squid Proxy instance.
   - Edit the Squid configuration file to specify whitelisted URLs and deny all other traffic.

3. **Restart Squid:**
   - Restart the Squid service to apply the configuration changes.

4. **Update EC2 Routing and Security Groups:**
   - Ensure that the EC2 instance hosting your website uses the security group associated with the Squid Proxy.
   - Adjust routing and subnet settings to route traffic through the Squid Proxy for internet access.

## Usage

- Your one-tier web application should now be able to access only the whitelisted URLs you specified.

## Configuration

- You can customize the Squid Proxy configuration in the `/etc/squid/squid.conf` file to modify the whitelisted URLs or further customize the access control.

## Contributing

Contributions to this project are welcome. Please follow the standard GitHub fork and pull request workflow.

##  License
This repository is licensed under the MIT License.

---

**Note:** Always make sure to follow best practices for security, and regularly update and maintain your infrastructure to address security vulnerabilities.
