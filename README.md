## Terraform AWS Infrastructure Deployment

This Terraform project automates the deployment of an AWS infrastructure with the following components:

- **VPC:** A virtual network to launch AWS resources.
- **Internet Gateway:** A gateway to allow internet access to resources within the VPC.
- **Custom Route Table:** A route table to define how network traffic is directed.
- **Subnets:** Subdivisions of the VPC's IP range across availability zones.
- **Security Group:** A set of firewall rules to control inbound and outbound traffic.
- **Network Interface:** A network interface with an IP address in one of the subnets.
- **Elastic IP:** A static IPv4 address for the network interface.
- **EC2 Instance:** An Ubuntu server instance with Apache HTTP server installed and enabled.

## Prerequisites

Before running this Terraform project, ensure you have:

- An AWS account with appropriate permissions.
- AWS Access Key ID and Secret Access Key.
- Terraform CLI installed on your local machine.

## Usage

1. **Clone this repository:**

    ```bash
    git clone https://gitlab.com/razielsa/Terraform-AWS-Deploy](https://github.com/RazielSa/Terraform-AWS-Deploy.git
    ```

2. **Navigate to the project directory and initialize Terraform:**

    ```bash
    cd terraform-aws-project
    terraform init
    ```

3. **Review and adjust the `terraform.tfvars` file to customize your deployment.**

4. **Run Terraform validation:**

    ```bash
    terraform validate
    ```

5. **Plan the deployment:**

    ```bash
    terraform plan -out "terraform.plan"
    ```

6. **Apply the changes and confirm with yes when prompted:**

    ```bash
    terraform apply "terraform.plan"
    ```

7. **Once the deployment is successful, you can access your web application using the EC2 instance's public IP address. Here's a screenshot of the deployed web application:**

   ![Web Application Screenshot](https://i.ibb.co/1bsxrYn/Terraform.png)


## Outputs

Upon successful deployment, you will get the following outputs:

- **Server Public IP:** Public IP address of the EC2 instance.
- **Server Private IP:** Private IP address of the EC2 instance.
- **Server ID:** ID of the EC2 instance.

## Cleanup

To destroy the infrastructure and clean up resources, run Terraform destroy and confirm with yes when prompted:

```bash
terraform destroy
```
## Contributing

Contributions are welcome! Please feel free to submit issues or pull requests.
