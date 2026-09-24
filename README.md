Authentication Methods

    AWS CLI Configuration: aws configure
    Environment Variables: AWS_ACCESS_KEY_ID, AWS_SECRET_ACCESS_KEY
    IAM Roles: For EC2 instances or AWS services
    AWS Profiles: Named credential profiles
    
AWS CLI Installation

Check your system architecture first:

# Linux/macOS
uname -m

# Windows PowerShell
$env:PROCESSOR_ARCHITECTURE

Official Website: https://aws.amazon.com/cli/

Windows:

# Using MSI installer (recommended)
# Download from: https://awscli.amazonaws.com/AWSCLIV2.msi

# Using winget
winget install Amazon.AWSCLI

# Using chocolatey
choco install awscli

Ubuntu/Debian:

# Update package index
sudo apt update

# Install AWS CLI v2 (choose based on your architecture)
# For x86_64
curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"

# For ARM64
curl "https://awscli.amazonaws.com/awscli-exe-linux-aarch64.zip" -o "awscliv2.zip"

unzip awscliv2.zip
sudo ./aws/install

# Verify installation
aws --version


Authentication Setup
Method 1: AWS CLI Configuration

aws configure

Enter your:

    AWS Access Key ID
    AWS Secret Access Key
    Default region (e.g., us-east-1)
    Default output format (json)

Method 2: Environment Variables

export AWS_ACCESS_KEY_ID="your-access-key"
export AWS_SECRET_ACCESS_KEY="your-secret-key"
export AWS_DEFAULT_REGION="us-east-1"

Tasks to Complete

    Get familiar with Terraform AWS documentation
        Visit: https://registry.terraform.io/providers/hashicorp/aws/latest
        Explore S3 resource documentation

    Create AWS resources using terraform
        S3 bucket with unique name

    Practice Terraform commands
        Initialize the working directory
        Plan the infrastructure changes
        Apply the configuration
        Verify resources in AWS Console

Important Notes

    Resource Names: S3 bucket names must be globally unique
    Regions: Ensure you're working in your intended AWS region
    Costs: Monitor AWS costs, even in free tier
    Cleanup: Always destroy resources when done practicing

Common Commands

# Initialize Terraform
terraform init

# Validate configuration
terraform validate

# Plan changes
terraform plan

# Apply changes
terraform apply

# Show current state
terraform show

# Destroy resources
terraform destroy

Troubleshooting Tips

    Check AWS credentials are properly configured
    Verify region settings match your intended deployment location
    Ensure S3 bucket names are unique and follow naming conventions
    Review AWS CloudTrail for API call logs if needed
