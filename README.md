// Totalmente funcional no zabbix V6 e V7(alpha), testado na versão 6.4.10 e 6.5.1



# Copie os arquivos para o diretório de scripts do Zabbix
(/usr/lib/zabbix/externalscripts/)
downdetector.py
downdetectorDiscovery.py
downdetectorlist.list

cd (/usr/lib/zabbix/externalscripts/)
chmod +x downdetector.py
chmod +x downdetectorDiscovery.py


# Faça a instalação das dependencias no servidor Zabbix
apt install python3-pip 
pip3 install bs4 
pip3 install requests 
pip3 install cloudscraper

# Importe o Template e o Host
zbx_export_templates.yaml
zbx_export_hosts.yaml

![zabbix-alarmes](https://github.com/botinhadigao/grafana-downdt/assets/89220727/996ce500-db60-4bb5-ac71-76b40a6f6acf)
![trigger_discovery](https://github.com/botinhadigao/grafana-downdt/assets/89220727/4821848b-246c-498e-8bff-be31af1b8d20)
![discovery-template](https://github.com/botinhadigao/grafana-downdt/assets/89220727/2e467af3-064e-4857-a72c-f5307d8df73e)



# Importe o json no Grafana, 
as imagens do JSON do grafana estão referenciadas para o "https://github.com/botinhadigao/grafana-downdt/tree/main/icones-png" mas podem ser anexadas na maquina onde está rodando o server
downdetector-problemas-1706479330520.json
DownDetector-1706479318668.json

![grafana-userview](https://github.com/botinhadigao/grafana-downdt/assets/89220727/f1dfaca1-b652-4faf-bdb3-75d23372bf57)
![grafana-downdetector-problems](https://github.com/botinhadigao/grafana-downdt/assets/89220727/b8d47b9f-c2ae-4248-bed9-96602b145b14)









# Projeto original
https://github.com/remontti/downdetector_zbx_grafana
