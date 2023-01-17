Vagrant.require_version ">= 2.2.2"

Vagrant.configure(2) do |config|
  config.vm.define "ansible-nas-test" do
    config.vm.box = "ubuntu/bionic64"
    config.vm.network "private_network", ip: "192.168.56.11"
    config.ssh.insert_key = false

    config.vm.provision "ansible_local" do |ansible|
      ansible.playbook = "run.yml"
      ansible.become = true
    end
  end
end
