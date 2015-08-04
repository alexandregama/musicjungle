# Musicjungle with Vagrant and Puppet

##### Executing vagrant into Vagrantfile directory
```
vagrant up
```

##### Sign-in into web server
```
vagrant ssh web
```

##### Updating apt-get
```
sudo apt-get update
```

#### Installing Java7 and Tomcat7
```
sudo apt-get install openjdk7-jre tomcat7
```

#### Write the following ip to private_network
```
192.168.50.10
```

#### Access the tomcat address to check if everything is working fine
```
http://192.168.50.10:8080
```

#### To destroy the web machine
```
vagrant destroy
```
