# Vorbereitungen

- Linux-Umgebung
  - Virtual Box: https://www.virtualbox.org/wiki/Downloads
  - Ubuntu-Image:  https://www.osboxes.org/ubuntu/
  - Import VDI: https://www.makeuseof.com/how-to-import-vdi-file-into-virtualbox/
  - osboxes.org:osboxes.org
- Git: 
  - sudo apt-get update; sudo apt install git
  - git clone git@github.com:viadee/falco-cloudland24.git

# 1. Falco
- Setup Falco-Container: compose.yml
- Aktuelle Falco_rules.yaml hinzufügen --> https://github.com/falcosecurity/rules/blob/main/rules/falco_rules.yaml
- docker-compose up
- Event Generator: docker run -it --rm falcosecurity/event-generator run syscall --loop

--> Events auf der Konsole

 # 2. Falco Sidekick
- 