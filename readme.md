# Vorbereitungen

- Linux-Umgebung
  - Virtual Box: https://www.virtualbox.org/wiki/Downloads
  - Ubuntu-Image:  https://www.osboxes.org/ubuntu/
  - Import VDI: https://www.makeuseof.com/how-to-import-vdi-file-into-virtualbox/
  - osboxes.org:osboxes.org
- Git 
  - sudo apt-get update; sudo apt install git
  - git clone https://github.com/viadee/falco-cloudland24.git
- Docker
  - https://docs.docker.com/engine/install/ubuntu/#install-using-the-repository

# 1. Falco
- Setup Falco-Container: compose.yml
- Aktuelle Falco_rules.yaml hinzufügen --> https://github.com/falcosecurity/rules/blob/main/rules/falco_rules.yaml
- docker-compose up
- Event Generator: docker run -it --rm falcosecurity/event-generator run syscall --loop

--> Events auf der Konsole

 # 2. Falco Sidekick
- compose.yml um falcosecurity/falcosidekick erweitern
- falco-Konfiguration für Weboutput anpassen

--> Vom Sidekick können Exportziele beliefert werden

# 3. Falco Sidekick-UI
Anzeige der Falco Events in einer einfachen UI
- compose.yml um falcosecurity/falcosidekick-ui erweitern
- Redis dient als Datenspeicher

--> UI unter http://localhost:2802 admin:admin
