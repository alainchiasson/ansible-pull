# ansible-pull DEMO

This is a simple test for ansible pull to see what works:

On the machine it is required to have Ansible, Git and dependancies. 

## Local Vagrant setup


- For this repo.
- Clone the new repo localy
- cd in the directory
- Vagrant up - will install git, ansible and dependancies
- run

```
ansible-pull -U https://github.com/alainchiasson/ansible-pull.git -i localhost,
```

Just replace the git repo with your own.

This will clone your repo, and run localhost.yaml on the system.

## Production use (as much as we can call this production)

After setting up hardware, and installing the required software, you can run the following command:

```
ansible-pull -U https://github.com/alainchiasson/ansible-pull.git -i services,
```

This base module will install the required software, and then run the services.yaml playbook. The services playbook establlishes a base machine for a homelab. This includes:

- A regular base linux system, manageable by cockpit.
- Creates a environment to run virtaual machines
- Creates the environment to run containers via podman.

Additioanlly, for all the services, the coresponding cockpit module is installed. This allows for easy management of the services.

## TODO

- For VM's and containers, figure out how to use terraform modules. The state file should be local to the machine, and not in the repo. The basic premis is we should have a simplified config in the repo, and the repo should be run much in the way ansible pull runs. 

We may want to wrap some of this so we can better manage the loop.

