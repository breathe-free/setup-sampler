## Get started

    # You need to be able to ssh to each machine as the user
    # specified in ansible.cfg, without a password.
    
    # Create inventory
    cp inventory.sample inventory  # Now edit inventory to match your needs.
    
    # Then, test things are ok
    ansible all -m ping -i inventory

## Get stuff

You will need to put Pumps.py in your secrets directory.

## Deploy

    ansible-playbook breathe-free.yml