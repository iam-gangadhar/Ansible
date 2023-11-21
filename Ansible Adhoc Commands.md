### Ansible Ad-hoc commands
1. To See All the Hosts server IP address in Hosts File
   ```sh 
   ansible all --list-hosts
   ```
2. Calling Nodes using Adhoc Commands
    ```sh 
   ansible webserver[0] --list-host   #first Node will call
   ```
    ```sh 
   ansible webserver[-1] --list-host   #Last Node will call
   ```
