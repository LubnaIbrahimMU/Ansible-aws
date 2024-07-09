ansible-playbook -i demo.aws_ec2.yml --private-key lu3  gate.yml -e "@all.yml" 

ansible-playbook -i demo.aws_ec2.yml --private-key lu3  gate.yml -e "@all.yml" --tags=laravel

ansible-playbook -i demo.aws_ec2.yml --private-key lu3  gate.yml -e "@all.yml" --tags=vol

ansible-playbook -i demo.aws_ec2.yml --private-key lu3  stop-linux-vm-aws.yml -e "@all.yml"

ansible-playbook -i demo.aws_ec2.yml --private-key lu3  start-linux-vm-aws.yml -e "@all.yml"

ansible-playbook -i demo.aws_ec2.yml --private-key lu3  re-start-linux-vm-aws.yml -e "@all.yml"

ansible-playbook -i demo.aws_ec2.yml  delete-linux-vm-aws.yml -e "@all.yml"

ansible-playbook delete-all-aws.yml -e "@all.yml"

ansible-inventory -i demo.aws_ec2.yml --list
ansible-inventory -i demo.aws_ec2.yml --graph

# to create the SSH public key  with the cst name replace lana

ssh-keygen -t rsa -b 4096  -f ~/.ssh/lana

# for user ssh  ...

ssh cloud_gate@<public_ip>  ##get it from /data_resources/instance_info.json

php artisan key:generate  ## ec2 key-test 

sudo nginx -t  