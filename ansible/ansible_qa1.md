<p align="right" width="100%">

1) What is Ansible, and what is it used for?

Ansible is an open-source automation tool that simplifies software configuration management, application deployment, and infrastructure orchestration. Ansible uses a declarative language to describe the state of a system and automates tasks that would otherwise be performed manually.

2) What is the difference between Ansible and other configuration management tools?

Ansible is agentless, which means it doesn't require any software or agents to be installed on the target system. This makes it easy to install and manage. Other configuration management tools like Puppet and Chef require an agent to be installed on the target system.

3) What is the role of the inventory file in Ansible?

The inventory file is a text file that contains a list of hosts that Ansible can manage. Ansible uses this 
file to know which hosts to connect to and which tasks to execute.

4) What is a playbook in Ansible?

A playbook is a file written in YAML format that contains a set of tasks and plays that are executed against a set of hosts defined in the inventory file. Playbooks describe a desired state of a system and the steps needed to reach that state.

5) What is a task in Ansible?

A task is a single action that Ansible performs, such as installing a package, copying a file, or restarting a service. Tasks are defined in a playbook and are executed sequentially.

6) What is a role in Ansible?

A role is a collection of tasks, templates, files, and variables that can be reused across multiple playbooks. Roles allow you to organize your code and share it with other teams.

7) What is an Ansible module?

An Ansible module is a small piece of code that performs a specific task, such as managing packages, files, users, or services. Modules can be called from within a playbook or a role to perform a specific action on the target system.

8) How does Ansible ensure idempotence?

Ansible ensures idempotence by checking the current state of the system before executing a task. If the desired state has already been achieved, Ansible will not execute the task again. This ensures that the same playbook can be run multiple times without causing any harm to the system.

9) How does Ansible communicate with remote hosts?

Ansible communicates with remote hosts using SSH (Secure Shell) protocol. Ansible establishes an SSH connection to the remote host and uses a temporary Python script to execute tasks on the remote host.

10) How do you define variables in Ansible?

Variables can be defined in several ways in Ansible, such as in the playbook itself, in inventory files, or in separate variable files. Variables can also be passed to Ansible on the command line using the --extra-vars option.

</p>