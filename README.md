# Aleph-VM-MacOs



### Setup

- Install Vagrant & Virtual Box 

1.  Run : ``` Vagrant up ``` | (``` destroy ```  to stop the process & don't forget to remove box list ) 

2.  In your Vagrantfile add :

```   config.vm.provision "shell", path: "bootstrap.sh" ```

3. Add ``` bootstrap.sh ``` file in the dir as follow : 

``` apt-get update

sudo apt-get install -y python3-pip libsecp256k1-dev squashfs-tools

pip3 install uvicorn[standard] aleph-client fastapi eth_account

``` 

- Running Aleph-client : 

In the dir run :

``` aleph program ./NAME_OF_YOUR_DIR/ main:app ``` 



#### Links :

[Aleph explorer](https://explorer.aleph.im/address/ETH/0x561AC1B0fD15Ba029a176892761c29000A508768/message/PROGRAM/d5ebd087ed488c6b349737ba7b5cafdc595bd75ea95a3f096766176ec024fded)

[The execution on the vm executer provided by Aleph](https://aleph.sh/vm/d5ebd087ed488c6b349737ba7b5cafdc595bd75ea95a3f096766176ec024fded)





