// Totalmente funcional no zabbix V6 e V7(alpha), testado na versão 6.4.10 e 6.5.1
![grafana-downdetector-problems](https://github.com/botinhadigao/grafana-downdt/assets/89220727/73c5a1b7-f1f1-4abe-b4ac-36ae1fa9e05c)


# Copie os arquivos para o diretório de scripts do Zabbix (/usr/lib/zabbix/externalscripts/)
downdetector.py
downdetectorDiscovery.py
downdetectorlist.list

cd /usr/lib/zabbix/externalscripts/
chmod +x downdetector.py
chmod +x downdetectorDiscovery.py


# Faça a instalação das dependencias no servidor Zabbix
apt install python3-pip 
pip3 install bs4 
pip3 install requests 
pip3 install cloudscraper

# Importe o Template e o Host

![zabbix-alarmes](https://github.com/botinhadigao/grafana-downdt/assets/89220727/996ce500-db60-4bb5-ac71-76b40a6f6acf)
![trigger_discovery](https://github.com/botinhadigao/grafana-downdt/assets/89220727/4821848b-246c-498e-8bff-be31af1b8d20)
![discovery-template](https://github.com/botinhadigao/grafana-downdt/assets/89220727/2e467af3-064e-4857-a72c-f5307d8df73e)



# Importe o json no Grafana, 
as imagens do JSON do grafana estão referenciadas para o "https://github.com/botinhadigao/grafana-downdt/tree/main/icones-png" mas podem ser anexadas na maquina onde está rodando o server
![Uploading ![grafana-userview](https://github.com/botinhadigao/grafana-downdt/assets/89220727/45a6871c-ceb4-4957-9e93-73287a9a38c1)
grafana-downdetector-problems.png…]()



# Copie os icones para esse diretorio

"/var/www/html/public/img/icon-downdetector/"
ou
"/usr/share/grafana/public/img/icon-downdetector/"

# No Grafana
"<center><img src="/public/img/icon-downdetector/logo.png" width="250px" /></center>"



# Projeto original
https://github.com/remontti/downdetector_zbx_grafana
