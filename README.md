## Ansible hands-on lab
### I, Install ansible
- Install virtualenv
  ```
  Linux: sudo apt install python3-virtualenv
  CentOS: sudo yum install epel-release -y
  Windows: python3 -m venv myenv
  ```
- Activate virtualenv
  ```
  Linux: virtualenv venv && source venv/bin/activate
  CentOS: python3 -m venv myenv && source venv/bin/activate
  Windows: .\myenv\Scripts\activate
  ```
- Install ansible inside virtualenv
  ```
  pip install ansible
  ```
- Test ansible installation:
  ```
  ansible --version
  ```

### II, Install collection
- Install community.docker
  ```
  ansible-galaxy collection install community.docker
  ```
### III, How to use

To execute each playbook, cd to the corresponding directory and run this command (with flag --ask-become-pass you must be enter your root password):

```
ansible-playbook -i inventory.yaml --ask-become-pass setup.yaml
```
