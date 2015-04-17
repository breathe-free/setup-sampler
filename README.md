## Get started

First, install ansible and any other tools.

    pip install -r requirements.txt

Ensure you are able to ssh to each machine as the user specified in ansible.cfg, without needing a password. Then:

    # Create inventory
    cp inventory.sample inventory  # Now edit inventory to match your needs.
    
    # After that, test things are ok.  You should get a message from each machine.
    ansible all -m ping -i inventory

## Get stuff

You will need to put Pumps.py in your secrets directory, or the install will fall over.  For the moment, this is intentional.

## Deploy!

This can take some time, because Raspberry Pis are not super quick:

    ansible-playbook breathe-free.yml

The good thing about using ansible is that it's not too slow the next time around; it only changes what it needs to.