# Virtualization and Vagrant

## Understanding Virtualization
* Virtualization allows a single computer system to run multiple operating systems that are completely isolated from each other.
* It utilizes a **Hypervisor** to manage the underlying hardware and the Virtual Machines (VMs).
* **Popular Linux VMs:** CentOS and Ubuntu.

### Types of Hypervisors
* **Type 1 (Bare Metal):** Runs directly on the computer's hardware. It is typically used for production environments (e.g., VMware ESXi).
* **Type 2 (Hosted):** Runs as a software application on top of a host operating system. It is primarily used for learning and testing (e.g., Oracle VirtualBox).

## Manual vs. Automatic VM Setup
* **Manual Setup:** Requires downloading server images (like CentOS-stream-9 ISO), attaching files to a storage section in VirtualBox, and modifying network adapters.
* **Automatic Setup (Vagrant):** Vagrant automates the entire VM setup process. It uses a `Vagrantfile` to define configurations and handles the network settings and hypervisor communication for you.

### Essential Vagrant Commands
First, create a dedicated folder for your OS, navigate into it (`cd`), and run the following commands in Git Bash:

* `vagrant init`: Initializes a new Vagrant environment and creates a Vagrantfile.
* `vagrant up`: Starts and provisions the VM.
* `vagrant halt`: Stops the running VM.
* `vagrant reload`: Restarts the VM, applying any new changes made to the configuration.
* `vagrant destroy`: Deletes the VM entirely.
* `vagrant box list`: Lists all downloaded Vagrant boxes.
* `vagrant ssh`: Connects you securely to the VM's command line.
* `exit`: Exits the Vagrant SSH session.