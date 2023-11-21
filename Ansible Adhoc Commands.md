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
7. Copying file from server to nodes using Ad-hoc command
    ```sh 
   ansible all -m copy -a "src=myfile dest=/home/admin"
   ```
8. Installing Package using Yum module in Ansible
    ```sh 
   ansible all -m yum -a "pkg=httpd state=present" -b
   ```
9. Removing package using yum module in ansible
 ```sh 
   ansible all -m yum -a "pkg=httpd state=absent" -b
   ```
10. Updating package using state as latest
   ```sh 
   ansible all -m yum -a "pkg=httpd state=latest" -b
   ```
11. Starting Service in any package using ad-hoc
   ```sh 
   ansible all -m service -a "pkg=httpd state=stated" -b
   ```