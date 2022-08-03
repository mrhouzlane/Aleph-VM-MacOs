# Aleph-VM-MacOs



### Vagrant : 

- Install Vagrant & Virtual Box 

1.  Run : ``` Vagrant up ``` | (``` destroy ```  to stop the process & don't forget to remove box list ) 
2.  In your Vagrantfile do :

```   config.vm.provision "shell", path: "bootstrap.sh" ```

3. Add ``` bootstrap.sh ``` file in the dir as follow : 

``` apt-get update

sudo apt-get install -y python3-pip libsecp256k1-dev squashfs-tools

pip3 install uvicorn[standard] aleph-client fastapi eth_account

``` 

- Running Aleph-client : 

In the dir run :

``` aleph program ./NAME_OF_YOUR_DIR/ main:app ``` 


