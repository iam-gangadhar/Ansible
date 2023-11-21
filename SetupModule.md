### Ansible SETUP module
1. usually we using setup module to collect all the information about our nodes
   ```sh 
   ansible all -m setup
   ```
2. To filter required data in setup module using filter
    ```sh 
   ansible all -m setup -a 'fitler=ipv4'
   ```
3. to know the machine name of the nodes using filter
    ```sh 
   ansible all -m setup -a 'filter=ansible_nodename'
   ```