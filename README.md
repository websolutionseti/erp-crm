
# Instalação do Odoo no Ubuntu 22.04

Este script instala o Odoo em um servidor Ubuntu 22.04. Ele permite a instalação de múltiplas instâncias do Odoo em um único servidor Ubuntu devido ao uso de diferentes portas `xmlrpc_ports`.

## Pré-requisitos

- Um domínio ou subdomínio para configurar o Odoo.
- Acesso root ao seu servidor VPS.

## Passo a Passo

### 1. Baixar o Script de Instalação

Faça o download do script de instalação e torne-o executável:

sudo wget https://path/to/your/script/odoo-install.sh
sudo chmod +x odoo-install.sh


####
-------------------------------

## Configurar o Script Abra o script e edite as variáveis conforme necessário

  - sudo nano odoo-install.sh

## As variáveis importantes a serem configuradas incluem:

As variáveis importantes a serem configuradas incluem:

OE_USER: Nome do usuário do sistema para o Odoo (padrão é odoo).
OE_HOME: Diretório home para o usuário Odoo.
OE_PORT: Porta padrão para o Odoo (padrão é 8069).
OE_VERSION: Versão do Odoo a ser instalada (ex: 17.0).
IS_ENTERPRISE: Defina como True se for instalar a versão Enterprise do Odoo.
INSTALL_NGINX: Defina como True para instalar e configurar o Nginx.
OE_SUPERADMIN: Senha do superadministrador do Odoo.
GENERATE_RANDOM_PASSWORD: Defina como True para gerar uma senha aleatória para o superadmin.
WEBSITE_NAME: Nome do domínio ou subdomínio para o seu site Odoo.
LONGPOLLING_PORT: Porta padrão para longpolling do Odoo (padrão é 8072).
ENABLE_SSL: Defina como True para instalar o certbot e habilitar SSL.
ADMIN_EMAIL: Email para registrar o certificado SSL.

## 3. Executar o Script
  Navegue até o diretório /home e execute o script:

'''Bash
cd /home
sudo ./odoo-install.sh


## 4. Acessar o Odoo
Após a conclusão da instalação, você pode acessar o Odoo no seu navegador usando o domínio ou subdomínio configurado:


'''Bash
http://your-domain.com:8069
Se você configurou SSL, use HTTPS:
'''Bash
https://your-domain.com:8069



**Créditos:**
Créditos
Odoo
PostgreSQL
wkhtmltopdf
