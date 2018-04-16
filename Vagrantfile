Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/xenial64"
  config.vm.box_version = "20180413.0.0"
  config.vm.network "private_network", ip: "192.168.99.101"
  config.vm.provider "virtualbox" do |v|
    v.memory = 8192
    v.cpus = 2
  end
  condaversion = "3-5.1.0-Linux-x86_64"
  condaloc = "/usr/share/anaconda"
  config.vm.provision "shell", inline: <<-SHELL
    if [ ! -f #{condaloc} ]; then
      curl -s https://repo.continuum.io/archive/Anaconda#{condaversion}.sh -o Anaconda.sh
      bash Anaconda.sh -b -f -p /usr/share/anaconda
    fi
    echo "PATH=/usr/share/anaconda/bin:$PATH" > /etc/profile.d/anaconda.sh
  SHELL
end
