# ansible-pull DEMO

This is a simple test for ansible pull to see what works:

- For this repo.
- Clone the new repo localy
- cd in the directory
- Vagrant up - will install git, ansible and dependancies
- run

# How it works

This is realy a testing framework / vm :

- Vagrant starts up and installs git, ansible and set the ansible host file.
- You login and run:

```
ansible-pull -U https://github.com/alainchiasson/ansible-pull.git -i localhost,
```

- This will pull down the "local.yml" file, and run ansible script. 

So you can replace the ust replace the git repo with your own, and use this to test.

# Additional items

- You can do a two pass "ansible-galaxy" to pull in additional roles.

