# Using Ansible Playbooks

Ansible playbooks are YAML files that define a series of tasks to automate IT processes. Follow these steps to use an Ansible playbook:

## Prerequisites
1. Install Ansible on your control machine.
2. Ensure SSH access to the target hosts.
3. Configure the `inventory` file with the target hosts.

## Steps to Run a Playbook
1. **Navigate to the Playbook Directory**  
    Open a terminal and navigate to the directory containing your playbook.

2. **Run the Playbook**  
    Use the following command to execute the playbook:
    ```bash
    ansible-playbook -i inventory playbook.yml
    ```
    Replace `inventory` with your inventory file and `playbook.yml` with the name of your playbook.

3. **Check the Output**  
    Review the output in the terminal to ensure tasks were executed successfully.

## Example
Here’s an example command to run a playbook:
```bash
ansible-playbook -i hosts site.yml
```

## Additional Options
- Use `--check` for a dry run:
  ```bash
  ansible-playbook -i inventory playbook.yml --check
  ```
- Use `--limit` to target specific hosts:
  ```bash
  ansible-playbook -i inventory playbook.yml --limit host_group
  ```

For more details, refer to the [Ansible Documentation](https://docs.ansible.com/).