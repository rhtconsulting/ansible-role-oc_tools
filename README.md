# oc_tools

Ansible role for installing the `oc` tools and logging into or out of a given OpenShift instance.

## Role Variables

| parameter      | required | default | choices       | comments 
| -------------- |:--------:|:-------:| ------------- |:-------- 
| `state`        | yes      | login   | login, logout |          
| `openshift_host`     | yes      |         |               | OpenShift host to log into         
| `openshift_username` | yes      |         |               | OpenShift usernmae to log in as         
| `openshift_password` | yes      |         |               | OpenShift username password         
                                   
## Example Playbook

### Log into OpenShift

```
- name: Testing
  hosts: localhost
  roles:
    - role: oc_tools
      state: login
      openshift_host: openshift.example.com:8443
      openshift_username: test
      openshift_password: Test123!@#
```

### Log out of OpenShift

```
- name: Testing
  hosts: localhost
  roles:
    - role: oc_tools
      state: logout
```
