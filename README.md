# ansible-pull DEMO

This is a simple test for ansible pull to see what works:

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
