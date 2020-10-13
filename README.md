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

# Resolução

## Primeira etapa: 
Criação de usuario: useradd -m usuario </br>
Criação de pastas: mkdir </br>
Permissionamento de arquivos e pastas:  chmod e chown </br>
iostat: Comando utilizado para mostrar o relatório de uso de CPU e de entrada/saída dos dispositivos de armazenamento. </br> 
htop: Comando utilizado para monitorar dados como: processos, consumo de CPU, consumo de RAM, PID das tarefas. </br>
ps -ef: Comando utilizado para verificação de processos em execução na maquina. </br>
grep: É o comando que utilizamos quando queremos especificar algo. por exemplo: netstat -anp | grep 8080. </br>
top: Top é o antecessor do htop, o htop é mais robusto. </br> 
free -m: O comando free do Linux é muito útil para se observar e monitorar o uso da memória do sistema. </br>
df -h: Mostra o espaço livre/ocupado/compartilhado de cada partição. </br> 
fdisk -l:  Comando que fornece funções de particionamento de disco. </br>
netstat -tplun: É uma ferramenta utilitária de rede de linha de comando que exibe conexões de rede. </br>
awk: Na verdade o awk não é um simples comando, ele é uma linguagem de programação. Resumidamente, podemos dizer que seu príncipio se baseia em procurar em um ou mais arquivos por linhas que contenham um determinado padrão e, quando encontrar, executar uma determinada ação. </br>
sed: O comando SED no Linux é uma ferramenta poderosa que ajuda a executar tarefas de uso geral. Entre elas: analisar e transformar textos.

## Segunda etapa:

#### ec2 (Elastic Compute cloud) 
É um serviço Web que disponibiliza capacidade computacional segura e redimensionável na nuvem. Computer refere-se aos recursos que estão sendo apresentados, cloud se refere ao fato de que estes são  recursos de computação hospedados na nuvem e Elastic se refere ao fato de que, se configurado corretamente você pode aumentar ou diminuir a quantidade de servidores exigido por um aplicativo automaticamente de acordo com as demandas atuais dessa aplicação.

#### RDS
Amazon RDS é o serviço da AWS que proporciona a criação de um banco de dados relacional hospedado totalmente na nuvem AWS sem precisar de uma administração contínua.

#### CloudWatch
Amazon CloudWatch é basicamente um serviço de monitoramento que permite monitorar seus recursos AWS e os aplicativos que você executa neles em tempo real. Alguns recursos do Amazon CloudWatch incluem coleta e rastreamento de métricas como utilização de CPU, transferência de dados, utilização de disco e etc, também podemos monitorar serviços para recursos e aplicativos em nuvem, além disso, você tem a  capacidade de definir alarmes em qualquer uma das suas métricas para enviar notificações ou realizar alguma ação automatizada. 

#### Router 53 
Route 53 é um sistema de nomes de domínio ou DNS, que é um serviço projetado para fornecer a empresas e desenvolvedores de forma confiável e altamente escalável para rotear usuários finais para terminais. 

#### EBS (Elastic Block Store)
Os volumes EBS podem ser usados como uma unidade de armazenamento para suas instâncias ec2, então sempre que você acha que precisa de espaço em disco para suas instâncias em execução na AWS, você pode pensar sobre elas. Esses volumes podem ser discos rígidos ou dispositivos SSD. O EBS permite que você aumente ou mude o tipo do seu armazenamento, isso significa que você pode mudar de disco rígido para SSD. 

#### Load Balance 
O Elastic Load Balancing distribui automaticamente o tráfego de entrada de aplicativos entre diversos destinos, como instâncias do Amazon EC2, contêineres, endereços IP e funções Lambda. O serviço pode lidar com a carga variável de tráfego dos aplicativos em uma única zona de disponibilidade ou em diversas zonas de disponibilidade. O Elastic Load Balancing oferece três tipos de load balancers, todos eles com a alta disponibilidade, a escalabilidade automática e a segurança robusta necessárias para tornar os aplicativos tolerantes a falhas.

#### VPC (Virtual Private Cloud)
Virtual Private Cloud é o serviço de rede AWS que atenderá seus requisitos de rede. Amazon VPC permite que você crie uma rede privada dentro da nuvem AWS que usa muitos dos mesmos conceitos e constrói como uma rede local.

#### Auto Scaling 
Auto Scaling ajuda a garantir que você tenha o número correto de instâncias ec2 disponíveis para Lidar com a carga da sua aplicação.
