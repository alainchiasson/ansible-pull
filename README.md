# ansible-pull

This is a simple test for ansible pull to see what works:

- For this repo.
- Clone the new repo localy
- cd in the directory
- Vagrant up - will install git, ansible and dependancies
- run
```
ansible -U gitrepo
```

This will clone your repo, and run localhost.yaml on the system.
