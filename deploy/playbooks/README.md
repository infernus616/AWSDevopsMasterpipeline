# This configuration is focused on the configuration of the k8s multinode cluster using ansible on AWS, AWS Instances will be launched first by Terraform, Then we will configure multinode cluster on those nodes with Ansible.

### We are going to use Red Hat Enterprise Linux 9 (HVM), SSD Volume Type -- Free Tier Eligible
Configure the ansible inventory file, and ansible.cfg file with the necessary details and then we are good to go.

*** Follow the below steps ***



- Run - `ansible-playbook rhel_common.yaml` It will configure the k8s master and slave node with common configurations.
- Run - `ansible-playbook rhel_master.yaml` It will configure k8s master node and it will also join the slave node to the master node.
- Now login to K8s master node , and create usual pods/deployments.
