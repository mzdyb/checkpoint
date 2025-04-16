# Check Point automation with Ansible

This project demonstrates an example of automating Check Point configuration using the Ansible Automation Platform. A standalone deployment is used meaning both the Security Gateway and Security Management Server components are installed on the same virtual machine. The following topology is utilized:

![Check Point lab](files/checkpoint_lab.png)


Job Workflows are used to automate the configuration of Check Point objects (networks, hosts, and groups), security policies and the automatic installation of the policy:

![Job Workflow](files/checkpoint_workflow_template.png)

As we can see the modular approach is used here and instead of having one playbook to configure everything separate Job Templates are used per particular functionality automation. It is implemented by using Ansible Tags in Roles and on Job Templates level. This hierarchy is also reflected in variables definition in group_vars folder (separate variables file per functionality).  
abc