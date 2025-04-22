# ai-ansible-ollama-virt-lightning
Get up and running with large language models running in a VM for close to zero footprint.

You should have at least 8 GB of RAM available to run the 7B models.

You need to already have 'sudo dnf group info virtualization' installed <br />
You need to already have 'sudo dnf info ansible' installed <br />

This will install virt-lightning https://github.com/virt-lightning/virt-lightning <br />
This will install in the VM https://ollama.com/ https://github.com/ollama/ollama with openchat model <br />

Put **vlo.yml** and **ollama.yml** files in your home directory
Run below to install:

**ansible-playbook vlo.yml -K**


I was testing AI to help me make these ansible scripts.

If you want to just test AI LLM with podman do below commands:

[jimccann@jimccann-thinkpadp1gen3$ podman run -d -v ollama:/root/.ollama -p 11434:11434 --name ollama ollama/ollama
[jimccann@jimccann-thinkpadp1gen3$ podman exec -it ollama ollama run openchat


This was done/run on Fedora Linux
