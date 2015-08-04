# Musicjungle with Vagrant and Puppet

Working with Vagrant
---------------------


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

Working with Puppet
---------------------

#### Create web.pp file into manifests directory
```
  Vagrafile-directory/manifests/web.pp
```

#### Create command to update apt-get
```ruby
exec { "apt-update":
  command => "/usr/bin/apt-get update"
}
```

#### Install openjdk and tomcat7
```ruby
package { ["openjdk-7-jre", "tomcat7"]:
  ensure => installed,
  require => Exec["apt-get"]
}
```

#### Executing puppet file
```
  sudo puppet apply /vagrant/manifests/web.pp
```

#### Executing puppet file in debbug mode
```
  sudo puppet apply -dv /vagrant/manifests/web.pp
```
