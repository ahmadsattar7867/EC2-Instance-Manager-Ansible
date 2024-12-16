# EC2 Instance Automation with Ansible and Docker

## Description

This project automates the process of managing EC2 instances on AWS, including provisioning, naming, and starting instances based on a specific naming convention. It leverages Ansible for orchestration and configuration management, AWS EC2 API for instance provisioning, and Docker for setting up a scalable web server environment on newly created EC2 instances.

## Features

- **Dynamic EC2 Instance Provisioning**: Automatically fetches existing EC2 instances based on custom tags, extracts the highest instance number, and generates unique names for new instances.
- **EC2 Instance Management**: Facilitates the creation and starting of EC2 instances with specific configurations such as instance type, security group, and AMI ID.
- **Custom Inventory Generation**: Generates an inventory file listing all newly created instances, ready for use in subsequent automation tasks.
- **Apache and Docker Setup**: Installs and configures Apache HTTP server and Docker on new instances, ensuring they are ready for deployment.
- **Secure Instance Access**: Uses public IPs and SSH access with specified keys for secure connection to newly provisioned EC2 instances.

## Prerequisites

- AWS account with appropriate permissions
- Ansible (version X.X or higher)
- AWS CLI configured with your credentials
- Python 3.x
- boto3 library

## Installation

1. Clone this repository:
   ```
   git clone https://github.com/yourusername/ec2-instance-automation.git
   cd ec2-instance-automation
   ```

2. Install required Python packages:
   ```
   pip install -r requirements.txt
   ```

3. Configure your AWS credentials (if not already done):
   ```
   aws configure
   ```

## Usage

1. Update the `vars.yml` file with your desired AWS configuration.

2. Run the main Ansible playbook:
   ```
   ansible-playbook main.yml
   ```

3. Check the generated inventory file for the list of new instances.

## Configuration

Edit the `vars.yml` file to customize:

- AWS region
- Instance type
- AMI ID
- Security group
- SSH key name
- Instance naming convention

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.