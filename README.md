# ansible
Learning ansible

================

# What is ansible?
Ansible is an open source automation and configuration management tool and also use to automate tasks.
Ansible provides open-source automation that reduces complexity and runs everywhere. Using Ansible lets you automate virtually any task.


# Steps to install ansible
sudo apt update
sudo apt install software-properties-common
sudo add-apt-repository --yes --update ppa:ansible/ansible
sudo apt install ansible

# Ansible commands

To ping hosts- 
ansible -i hosts all -m ping

To run playbook-
ansible-playbook -i hosts file.yml

# Ansibel galaxy 

# Use the ansible-galaxy command to create a new role structure:
ansible-galaxy init my_role_name

Directory Structure of a Role:

my_role_name/
├── defaults/
│   └── main.yml    # Default variables for the role
├── files/          # Static files that can be copied to remote hosts
├── handlers/       # Handlers to be notified on changes (e.g., restart a service)
├── meta/           # Metadata, including dependencies, author info
│   └── main.yml
├── tasks/          # Main tasks that the role will perform
│   └── main.yml
├── templates/      # Jinja2 templates to be rendered
├── tests/          # Test playbooks for role verification
├── vars/           # Variables specific to the role
│   └── main.yml
└── README.md       # Documentation for the role