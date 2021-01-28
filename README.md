# react-deployment

## Boostrapping the deployment nodes
1. Create ssh public/private key pair
2. Add the public key string to line 29 as the "key" of the /bootstrap.yml file
3. Add the directory location of the private key on the local server to the private_key_file parameter of the /ansible.cfg file
4. Run in the terminal: ansible-playbook --ask-become-pass bootstrap.yml
5. Uncomment the remote_user parameter in the /ansible.cfg file

## Install Dependencies
1. Run: `ansible-galaxy install geerlingguy.certbot`