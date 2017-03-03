# oc_tools

Ansible role for installing the `oc` tools and logging into or out of a given OCP instance.

## Role Variables

| parameter      | required | default | choices       | comments 
| -------------- |:--------:|:-------:| ------------- |:-------- 
| `state`        | yes      | login   | login, logout |          
| `ocp_host`     | yes      |         |               | OCP host to log into         
| `ocp_username` | yes      |         |               | OCP usernmae to log in as         
| `ocp_password` | yes      |         |               | OCP username password         
                                   
## Example Playbook

### Log into OCP

```
- name: Testing
  hosts: localhost
  roles:
    - role: oc_tools
      state: login
      ocp_host: openshift.example.com:8443
      ocp_username: test
      ocp_password: Test123!@#
```

### Log out of OCP

```
- name: Testing
  hosts: localhost
  roles:
    - role: oc_tools
      state: logout
```
