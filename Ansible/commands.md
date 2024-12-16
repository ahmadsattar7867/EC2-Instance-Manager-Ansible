ansible-playbook -i inventory/ec2_inventory.ini  playbook.yaml --vault-password-file vault.pass


to create instace, dir ec2


# for server control node
ssh-keygen -lf ~/.ssh/id_rsa

# new instances
ssh-keygen -t rsa -b 4096
ssh-copy-id -i ~/.ssh/id_rsa.pub 

# on client, first one on do folder, next one on playbook
ssh-copy-id -i ~/.ssh/id_rsa.pub ubuntu@52.90.138.7 
ssh ubuntu@52.90.138.7



