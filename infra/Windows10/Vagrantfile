# Vagrantfile para a box Windows 10
# Comentários: este arquivo configura a VM e o provider local.
# - Provider atual: `virtualbox` (mais fácil de instalar/localmente gratuito).
# - Se preferir usar VMware, substitua o provider por "vmware_desktop" e instale
#   o plugin comercial `vagrant-vmware-desktop` (requiere licença/ativação).

Vagrant.configure("2") do |config|
	# Imagem/box usada
	config.vm.box = "gusztavvargadr/windows-10"

	# Configuração específica do provider. Atualmente usa VirtualBox.
	# Para ajustar recursos da VM, altere `vb.memory` e `vb.cpus` conforme necessário.
	config.vm.provider "virtualbox" do |vb|
		# Memória em MB
		vb.memory = 6144
		# Número de CPUs virtuais
		vb.cpus = 4
	end

	# Observações:
	# - Se você pretende usar VMware (já instalado no host), troque o bloco acima
	#   por `config.vm.provider "vmware_desktop" do |vb| ... end` e instale o plugin
	#   `vagrant-vmware-desktop` (comando: `vagrant plugin install vagrant-vmware-desktop`).
	# - Após mudanças no provider, execute `vagrant up --provider=<nome>` para forçar
	#   um provider específico (ex: `vagrant up --provider=virtualbox`).
end



