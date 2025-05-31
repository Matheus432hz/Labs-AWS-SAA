# Portfólio de Laboratórios AWS - MATHEUS-SALLA

Bem-vindo ao meu portfólio de laboratórios da AWS! Este repositório resume os projetos práticos que desenvolvi como parte dos meus estudos na Escola da Nuvem, demonstrando minhas habilidades e conhecimentos em diversos serviços e soluções da Amazon Web Services.

O objetivo é apresentar de forma clara e concisa os desafios propostos em cada laboratório e as soluções implementadas.

## Acesso às Evidências Detalhadas dos Laboratórios

Todos os documentos de instruções detalhadas, passo a passo da execução, e as capturas de tela comprobatórias para cada laboratório estão organizados na seguinte pasta do Google Drive:

➡️ **[Documentação Completa dos Laboratórios AWS no Google Drive](https://drive.google.com/drive/folders/13FqMqbLXGJJ9gTknMQPs4rXCTnl_kkOc?usp=sharing)**


---

## Resumo dos Laboratórios Desenvolvidos

Abaixo, apresento um resumo de cada laboratório realizado:

### 1. Laboratório 1: Introdução à AWS IAM e Segurança
* **Objetivo:** Capacitar no gerenciamento de identidades e permissões de forma eficaz, garantindo o acesso adequado e seguro aos recursos da AWS. Isso incluiu a configuração de usuários, grupos, políticas no IAM e a configuração de um bucket S3 com acesso restrito.
* **Principais Serviços AWS Utilizados:** IAM (Identity and Access Management), Amazon S3.
* **Descrição Breve:** Neste laboratório, configurei o controle de acesso fundamental na AWS, criando diferentes perfis de usuários (Desenvolvedor, Analista, Administrador) com permissões específicas, utilizei grupos para gerenciar essas permissões, implementei MFA para o administrador e restringi o acesso a um bucket S3 através de uma política personalizada. Os testes validaram as configurações de segurança de cada perfil.

### 2. Laboratório 2: Amazon EC2 e Armazenamento EBS
* **Objetivo:** Trabalhar com instâncias EC2 e volumes EBS, aprendendo a criar, configurar e gerenciar esses recursos essenciais de computação e armazenamento na nuvem.
* **Principais Serviços AWS Utilizados:** EC2 (Elastic Compute Cloud), EBS (Elastic Block Store).
* **Descrição Breve:** Provisionei uma instância EC2 para um servidor web simples, adicionei e configurei um volume EBS adicional para armazenamento de dados do site, e explorei a criação de snapshots para backup, garantindo a segurança e disponibilidade dos dados. A conexão SSH foi utilizada para gerenciamento da instância.

### 3. Laboratório 3: Amazon S3 Básico e Avançado
* **Objetivo:** Explorar e aplicar recursos de armazenamento e segurança do Amazon S3, incluindo versionamento de objetos, configuração de regras de ciclo de vida e geração de URLs pré-assinadas para acesso seguro e temporário.
* **Principais Serviços AWS Utilizados:** Amazon S3.
* **Descrição Breve:** Criei e configurei um bucket S3, explorei o versionamento para manter histórico de arquivos, implementei uma regra de ciclo de vida para otimizar custos movendo dados para classes de armazenamento mais frias, e gerei URLs pré-assinadas para compartilhamento controlado de objetos.

### 4. Laboratório 4: Rede Virtual (VPC)
* **Objetivo:** Criar uma VPC (Virtual Private Cloud) funcional com sub-redes pública e privada, configurar grupos de segurança para controle de tráfego e testar a conectividade entre os recursos e a internet.
* **Principais Serviços AWS Utilizados:** VPC, EC2 (para instâncias de teste), NAT Gateway, Internet Gateway, Route Tables, Security Groups.
* **Descrição Breve:** Construí uma rede virtual isolada na AWS, configurando uma sub-rede pública para um servidor web e uma sub-rede privada para um servidor de banco de dados. Implementei Security Groups para proteger as instâncias e configurei o roteamento para permitir acesso à internet para a sub-rede pública (via Internet Gateway) e para a sub-rede privada (via NAT Gateway, demonstrado pelo instrutor). Testes de conectividade foram realizados usando SSH.

### 5. Laboratório 5: Notificações de Upload/Exclusão no S3 com SNS e SQS
* **Objetivo:** Configurar um sistema de notificações por e-mail (via SNS) e registro de eventos em uma fila (via SQS) para ações de upload e exclusão de arquivos em um bucket S3.
* **Principais Serviços AWS Utilizados:** Amazon S3, SNS (Simple Notification Service), SQS (Simple Queue Service).
* **Descrição Breve:** Implementei uma solução para monitoramento e auditoria de um bucket S3. Configurei o S3 para enviar eventos de criação e remoção de objetos para um tópico SNS. Este tópico, por sua vez, notificava um endpoint de e-mail e enviava mensagens para uma fila SQS para registro e processamento posterior. Foram ajustadas políticas de acesso no SNS e SQS para permitir a comunicação entre os serviços.

### 6. Laboratório 6: Auto Scaling e Load Balancing na AWS
* **Objetivo:** Configurar um ambiente web altamente disponível e escalável utilizando Auto Scaling Groups, Launch Templates e um Application Load Balancer para distribuir o tráfego e gerenciar automaticamente o número de instâncias EC2.
* **Principais Serviços AWS Utilizados:** EC2, Auto Scaling Groups, Application Load Balancer (ALB), Launch Templates, VPC (utilizando a VPC padrão).
* **Descrição Breve:** Criei um Launch Template para definir a configuração das instâncias EC2 que serviriam uma aplicação web. Configurei um Auto Scaling Group para manter um número desejado de instâncias e escalar com base na demanda (neste lab, mantivemos um número fixo para demonstração). Um Application Load Balancer foi configurado para distribuir o tráfego HTTP entre as instâncias do Auto Scaling Group, e testes foram realizados para verificar o balanceamento de carga.

### 7. Laboratório 7: Monitoramento e Auditoria com CloudWatch e CloudTrail
* **Objetivos:** Aprender a configurar monitoramento de recursos com alarmes no CloudWatch e habilitar a auditoria de atividades da conta AWS com CloudTrail, armazenando e visualizando os logs gerados.
* **Principais Serviços AWS Utilizados:** CloudWatch, CloudTrail, EC2, SNS, S3.
* **Descrição Breve:** Lancei uma instância EC2 e configurei um alarme no CloudWatch para monitorar sua utilização de CPU, com notificações enviadas para um tópico SNS ao atingir um limite predefinido. Habilitei o CloudTrail para rastrear eventos da API na conta, configurando o armazenamento dos logs em um bucket S3 para auditoria e conformidade. Testei o alarme de CPU e explorei a visualização dos logs do CloudTrail.

---

Agradeço a oportunidade de demonstrar minhas habilidades. Estou sempre buscando aprender e aplicar novas tecnologias da nuvem.
