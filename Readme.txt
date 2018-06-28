Step 1:
Run "vagrant up" to provision the infrastructure. It contains one web server and one app server

Step 2:

Run ansible-playbooy to deploy the content to App server

eg: 
  To deploy war file
	ansible-playbook -i .vagrant/provisioners/ansible/inventory playbooks/vagrant-deploy-app.yml -u vagrant
  To deploy zip file
	ansible-playbook -i .vagrant/provisioners/ansible/inventory playbooks/vagrant-deploy-zip.yml -u vagrant
Step 3:
Set host entry as follows to access the service through web
	10.0.0.100 vagrant.web.com
