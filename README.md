// Totalmente funcional no zabbix V6 e V7(alpha), testado na versão 6.4.10 e 6.5.1


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

# Importe o json no Grafana, as imagens do JSON do grafana estão referenciadas para o https://github.com/botinhadigao/grafana-downdt/tree/main/icones-png mas podem ser anexadas na maquina onde está rodando o server

# Copie os icones para esse diretorio
/var/www/html/public/img/icon-downdetector/
ou
/usr/share/grafana/public/img/icon-downdetector/

# No Grafana
<center><img src="/public/img/icon-downdetector/logo.png" width="250px" /></center>



# Projeto original
https://github.com/remontti/downdetector_zbx_grafana
