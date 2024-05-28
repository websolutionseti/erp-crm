erp-crm
Essa aplicação é para usuários iniciantes.

Instalação do Odoo no Ubuntu 22.04
Este script instala o Odoo em um servidor Ubuntu 22.04. Ele permite a instalação de múltiplas instâncias do Odoo em um único servidor Ubuntu devido ao uso de diferentes portas xmlrpc_ports.

Pré-requisitos
Um domínio ou subdomínio para configurar o Odoo.
Acesso root ao seu servidor VPS.
Passo a Passo
Baixar o Script de Instalação Faça o download do script de instalação e torne-o executável:
sudo wget https://path/to/your/script/odoo-install.sh
sudo chmod +x odoo-install.sh

Configurar o Script Abra o script e edite as variáveis conforme necessário:
sudo nano odoo-install.sh
As variáveis importantes a serem configuradas incluem:
OE_USER: Nome do usuário do sistema para o Odoo (padrão é odoo).
OE_HOME: Diretório home para o usuário Odoo.
OE_PORT: Porta padrão para o Odoo (padrão é 8069).
OE_VERSION: Versão do Odoo a ser instalada (ex: 17.0).
IS_ENTERPRISE: Defina como True se for instalar a versão Enterprise do Odoo.
INSTALL_NGINX: Defina como True para instalar e configurar o Nginx.
OE_SUPERADMIN: Senha do superadministrador do Odoo.
…
Executar o Script Navegue até o diretório /home e execute o script:
cd /home
sudo ./odoo-install.sh

Acessar o Odoo Após a conclusão da instalação, você pode acessar o Odoo no seu navegador usando o domínio ou subdomínio configurado:
http://<seu-dominio.com.br>:8069
Se você configurou SSL, use HTTPS: https://<seu-dominio.com.br>:8069
Créditos
Odoo
PostgreSQL
wkhtmltopdf
