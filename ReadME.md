# Instructions to create and deploy kubernetes cluster on ec2 instance

## Steps
- Create an ec2 instance (Amazon Linux Inferred t2.micro free tier) using aws-console,
  you may choose other instance where some of the utility programs are already available
- Download the .pem file, move it to the secured/hidden directory
- Create a new hidden directory using `mkdir .dir_name`, preferably under home directory (~/)
- If its the existing directory then use `mv dir_name .dir_name`
- Once the ec2_secret_key is available in the secured directory, use `chmod 400 ec2_secret_key.pem`, this step makes it more secured
- ssh into ec2 instance using `ssh -i ~/.dir_name/ec2_secret_key.pem Public_IPv4_DNS`
- Clone the git repo containing yml files for services that needs to deployed using `git clone git_repo_path`
- If git is not installed on ec2 then install it using `sudo yum install git`
