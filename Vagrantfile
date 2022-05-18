Vagrant.configure("2") do |config|
  config.vm.synced_folder ".", "/vagrant", disabled: true
  config.vm.synced_folder "shared/", "/home/vagrant/shared", create: true
  config.vm.provision "shell", path: "prov.sh"
 
  config.vm.box = "debian/bullseye64"
 
 
  # Pakota pienet resurssit
  config.vm.provider "virtualbox" do |vb|
    vb.memory = 1024
    vb.cpus = 1
  end
 
  # Master
  config.vm.define "vg01" do |vg01|
    vg01.vm.hostname = "vg01"
      # Saltin master-asennus
    # Saltin minion-asennus
    vg01.vm.provision "shell", path: "salt-minion.sh"
  end
 
  # Minion 1
  config.vm.define "vg02" do |vg02|
    vg02.vm.hostname = "vg02"
    # Saltin minion-asennus
    vg02.vm.provision "shell", path: "salt-minion.sh"
  end
 
  # Minion 2
  config.vm.define "vg03" do |vg03|
    vg03.vm.hostname = "vg03"
    # Saltin minion-asennus
    vg03.vm.provision "shell", path: "salt-minion.sh"
  end
 
  # Minion 3
  config.vm.define "vg04" do |vg04|
    vg04.vm.hostname = "vg04"
    # Saltin minion-asennus
    vg04.vm.provision "shell", path: "salt-minion.sh"
  end
 
end