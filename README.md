# terraform-to-jenkins
Deploy and Configure Jenkins on AWS with Terraform

## Step 1: Initialize Terraform
```
terraform init
```

## Step 2: Plan Resources
```
terraform plan -var-file="template.tfvars"
```

## Step 3: Apply Resources
```
terraform apply -var-file="template.tfvars"
```

## Step 4: SSH to instance to get the admin password
```
chmod 400 <keypair>
ssh -i <keypair> ec2-user@<public_dns>
sudo cat /var/lib/jenkins/secrets/initialAdminPassword
```
