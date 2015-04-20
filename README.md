## Get started

First, install ansible and any other tools.

    pip install -r requirements.txt

Ensure you are able to ssh to each machine as the user specified in ansible.cfg, without needing a password, and run commands using `sudo` without a password, too. (`ssh-copy-id` a good way.)

Then:

    # Create inventory
    cp inventory.sample inventory  # Now edit inventory to match your needs.
    
    # After that, test things are ok.  You should get a message from each machine.
    ansible all -m ping

## Get stuff

You will need to put Pumps.py in your secrets directory, or the install will fall over.  For the moment, this is intentional.  You can configure the location in `roles/sampling/defaults/main.yml`.

## Deploy!

This can take some time, because Raspberry Pis are not super quick:

    ansible-playbook breathe-free.yml

The good thing about using ansible is that it's not too slow the next time around; it only changes what it needs to.