# Mandic-Test
Esse repositorio tem como objetivo detalhar todo o processo de resolução do teste técnico aplicado pela empresa Mandic Cloud Solution. O teste foi ministrado pelo gerente de engenharia SRE - Diogo Lima. 

## Proposta de teste:

### 1. Estudar comandos básicos Linux

- Criação de usuários; 
- Criação de pastas; 
- Permissionamento de arquivos e pastas;
- Entender os comandos:
(iostat, htop, ps -ef, grep , top, free -m, df -h, fdisk -l, netstat -tplun, awk, sed)
(apoś o entendimento dos comandos mescle eles).

### 2. Estudar recursos da AWS
Leia sobre Serviços AWS como: </br> 
EC2, RDS, CloudWatch, Route 53, EBS, Elastic Load Balancer (ELB), VPC e Auto-Scaling.

### 3. instalação dos componentes Básicos - S.O CENTOS

Instalar e configurar na máquina que lhe passei acesso os seguintes componentes:

- Nginx;
- Php-fpm;

### 4. Atividades

- Criar um domínio e ajustar as entradas de DNS
- Criar um webserver USE o SEU ATUAL 
- Configurar uma loja com Magento
- Configurar um blog com WordPress
- Configurar o Tomcat
- criar certificado SSL wildcard

## Aceitação
- Ao menos um dos sites deve estar configurado com o certificado SSL
- Cada um dos ambientes precisa ter o seu próprio virtual host no Nginx
- As configurações dos sites devem ficar no diretório /var/www/html/NOME-DA-PASTA ou /usr/share/nginx/html/NOME-DA-PASTA, com uma pasta para cada ambiente
- O Tomcat precisa apenas estar no ar e via Nginx entregar a página padrão

### entradas:
- sites.dominio < DNS do site estático
- loja.dominio < DNS do Magento
- blog.dominio < dns do WordPress
- tomcat.dominio < dns do Tomcat
- o site deve apontar para um index.php
- o blog não pode abrir com /wordpress na frente
- documentação dos passos realizados para a criação desse ambiente.
