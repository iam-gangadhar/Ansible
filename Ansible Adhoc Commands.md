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
3. Using Command module to Run Linux Commands to the Nodes
    ```sh 
   ansible all -m command -a "hostname"
   ```
    ```sh 
   ansible all -a "ls"  # to see all files in current admin directory
   ```
4. Create a file /directory
    ```sh 
   ansible all -a "touch myfile"   # creating myfile to all nodes
   ```
5. Checking Nodes are Reachable or Not
    ```sh 
   ansible all -m ping   # Fetching the information from nodes.
   ```
6. Installing Package using Ad-hoc command
    ```sh 
   ansible all -a "sudo yum install tree -y"
   ```


