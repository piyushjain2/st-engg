# Ansible Playbook: Install Prometheus Node Exporter

This Ansible playbook installs Prometheus Node Exporter on Ubuntu servers.

## Prerequisites

- Ansible installed on the machine where you'll run the playbook.

## Usage

1. Save the playbook code into a file with a `.yml` extension, for example, `install_node_exporter.yml`.

2. Create an inventory file (`inventory.ini`) listing your target servers:

    ```ini
    [your_ubuntu_servers]
    server1 ansible_ssh_user=your_remote_user
    server2 ansible_ssh_user=your_remote_user
    # Add more servers if needed
    ```

    Replace `server1`, `server2`, and `your_remote_user` with your actual server information.

3. Install Ansible on your machine (if not already installed):

    - On Ubuntu:

      ```bash
      sudo apt-get update
      sudo apt-get install ansible
      ```

    - On CentOS:

      ```bash
      sudo yum install ansible
      ```

    - On macOS (using Homebrew):

      ```bash
      brew install ansible
      ```

4. Run the playbook:

    ```bash
    ansible-playbook -i inventory.ini install_node_exporter.yml
    ```

    Replace `inventory.ini` and `install_node_exporter.yml` with your actual inventory file and playbook filename if they have different names.

Ansible will connect to the specified servers, execute the tasks defined in the playbook, and install Prometheus Node Exporter.

If you encounter any issues or have specific requirements, feel free to ask for further assistance!
