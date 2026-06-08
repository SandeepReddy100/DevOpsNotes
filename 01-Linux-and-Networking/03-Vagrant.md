# Virtualization and Vagrant

## Understanding Virtualization
* Virtualization allows a single computer system to run multiple operating systems that are completely isolated from each other[cite: 57, 58].
* It utilizes a **Hypervisor** to manage the underlying hardware and the Virtual Machines (VMs)[cite: 60, 67].
* **Popular Linux VMs:** CentOS and Ubuntu[cite: 78, 79].

### Types of Hypervisors
* **Type 1 (Bare Metal):** Runs directly on the computer's hardware. It is typically used for production environments (e.g., VMware ESXi)[cite: 70, 71, 72].
* **Type 2 (Hosted):** Runs as a software application on top of a host operating system. It is primarily used for learning and testing (e.g., Oracle VirtualBox)[cite: 68, 69, 74, 75].

## Manual vs. Automatic VM Setup
* **Manual Setup:** Requires downloading server images (like CentOS-stream-9 ISO), attaching files to a storage section in VirtualBox, and modifying network adapters[cite: 81, 88, 89, 91, 92, 94, 95, 96].
* **Automatic Setup (Vagrant):** Vagrant automates the entire VM setup process[cite: 101, 102]. It uses a `Vagrantfile` to define configurations and handles the network settings and hypervisor communication for you[cite: 103, 107, 109].

### Essential Vagrant Commands
First, create a dedicated folder for your OS, navigate into it (`cd`), and run the following commands in Git Bash[cite: 114, 115, 116, 117, 120]:

* `vagrant init`: Initializes a new Vagrant environment and creates a Vagrantfile[cite: 121].
* `vagrant up`: Starts and provisions the VM[cite: 122].
* `vagrant halt`: Stops the running VM[cite: 124].
* `vagrant reload`: Restarts the VM, applying any new changes made to the configuration[cite: 123].
* `vagrant destroy`: Deletes the VM entirely[cite: 125].
* `vagrant box list`: Lists all downloaded Vagrant boxes[cite: 126].
* `vagrant ssh`: Connects you securely to the VM's command line[cite: 128].
* `exit`: Exits the Vagrant SSH session[cite: 129].