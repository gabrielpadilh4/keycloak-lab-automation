# My Keycloak Automated Lab

This repository contains an Ansible playbook for deploying a Keycloak server, PostgreSQL database, and LDAP server using Podman containers. The playbook also sets up a Keycloak realm for user authentication and management with LDAP configured.

## Prerequisites

Before running the playbook, ensure you have the following installed on your local machine:

- **Ansible**: Install Ansible from [Ansible's installation guide](https://docs.ansible.com/ansible/latest/installation_guide/index.html).
- **Ansible Navigator**: Install Ansible Navigator from [Ansible Navigator's installation guid](https://ansible.readthedocs.io/projects/navigator/installation).
- **Podman**: Install Podman from [Podman's official site](https://podman.io/).

## Repository Structure
~~~
├── ansible.cfg
├── ansible-navigator.yml
├── collections
│   └── requirements.yml
├── playbooks
│   ├── setup-keycloak-container-environment.yml
│   └── setup-keycloak-realm-and-user-federation.yml
├── playbook.yml
├── README.md
└── vars
    └── keycloak.yml
~~~

- **ansible.cfg**: Configuration file for Ansible.
- **ansible-navigator.yml**: Configuration for Ansible Navigator
- **collections/**: Collections directory
- **playbooks/**: Playbooks directory with basic playbooks
- **vars/keycloak.yml**: Actual variables used in the playbook
- **playbook.yml**: The main playbook file to run.

## Usage

1. **Clone the Repository**

   ```sh
   git clone https://github.com/gabrielpadilh4/keycloak-lab-automation
   cd keycloak-lab-automation
   ```


2. Install required collections
   ```sh
   ansible-galaxy collection install -r collections/requirements.yml
   ```

3. Update the variables with the desired values in `vars/keycloak.yml`

4. Run the playbook to start the environment
   ```sh
   ansible-navigator run playbook.yml 
   ```

# Contributing
Contributions are welcome! Please open an issue or submit a pull request for any improvements or bug fixes.

# Acknowledgements
Special thanks to the open-source community for providing tools and resources that make projects like this possible.