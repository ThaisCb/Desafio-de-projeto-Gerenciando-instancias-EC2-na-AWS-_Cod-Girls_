# Desafio-de-projeto-Gerenciando-instancias-EC2-na-AWS-_Cod-Girls_
Abordando conceitos fundamentais, modelos de custo, principais serviços (EC2, EBS, S3) e arquitetura em nuvem.

# O que é AWS?

AWS é a Amazon Web Services, a plataforma de computação em nuvem da Amazon.
Ela oferece recursos como servidores virtuais, armazenamento, bancos de dados e ferramentas de desenvolvimento para que empresas e pessoas criem, hospedem e escalem aplicações pela internet, pagando só pelo que usam.

## Existem três formas principais de acessar a AWS: Console AWS, AWS CLI, CloudShell

### 1. Console da AWS (Web)

Interface gráfica no navegador.

Fácil de usar, ideal para iniciantes e tarefas manuais.

### 2. AWS CLI (Command Line Interface)

Ferramenta de linha de comando.

Permite automatizar tarefas, criar scripts e gerenciar recursos rapidamente.

### 3. AWS CloudShell

Sem necessidade de instalar nada: você acessa um ambiente Linux já configurado com a AWS CLI e ferramentas comuns.

Permite executar comandos, scripts e gerenciar recursos AWS rapidamente.

Ideal para quem quer experimentar ou gerenciar a AWS sem sair do navegador.

***

## Regiões e Zonas de Disponibilidade

<img width="1196" height="669" alt="Captura de tela 2025-09-23 062600" src="https://github.com/user-attachments/assets/81f2a0b6-357a-4f62-b42c-4ec879ff2e97" />


### Regiões


São áreas geográficas (ex.: us-east-1 na Virgínia, sa-east-1 em São Paulo).

Cada região é independente e possui sua própria infraestrutura.

Você escolhe a região mais próxima dos usuários para reduzir latência e atender requisitos legais.

### Zonas de Disponibilidade (AZs)

Cada região contém duas ou mais AZs.

Uma AZ é formada por um ou mais datacenters separados fisicamente, com energia, rede e refrigeração próprias.

As AZs dentro da mesma região são interconectadas por links rápidos e seguros.

Isso permite criar sistemas redundantes: se uma AZ cair, outra mantém o serviço no ar.
***
# Principais Serviços da AWS

A AWS oferece uma gama enorme de serviços, mas alguns se destacam por serem essenciais para praticamente qualquer projeto na nuvem:

### 1. EC2 (Elastic Compute Cloud)

 É o serviço da AWS que fornece servidores virtuais na nuvem.

Com ele, você pode:

Criar e rodar máquinas virtuais rapidamente;

Escolher o tipo de instância (CPU, memória, armazenamento) de acordo com a necessidade;

Escalar seus recursos de forma flexível, pagando apenas pelo tempo que a instância estiver ativa;

Gerenciar sistemas operacionais e aplicativos como se estivesse em um servidor físico, mas sem se preocupar com a infraestrutura física.


<img width="1131" height="669" alt="Captura de tela 2025-09-23 063119" src="https://github.com/user-attachments/assets/c5baaf99-879a-4282-a0a5-a9c61c153cd2" />

### 2. S3 (Simple Storage Service)

É o serviço de armazenamento de arquivos e objetos da AWS.

Com ele, você pode:

Guardar qualquer tipo de arquivo (imagens, vídeos, backups, documentos) de forma segura e escalável;

Acessar os dados de qualquer lugar pela internet;

Definir permissões e políticas de segurança para controlar quem pode ver ou alterar os arquivos;

Pagar apenas pelo espaço e pela quantidade de dados transferidos, sem precisar de servidor físico.

A sua disponibilidade é de: 99,999999999%


<img width="1031" height="626" alt="Captura de tela 2025-09-23 063026" src="https://github.com/user-attachments/assets/62a388c8-4177-4487-aba5-7587f1ec8df4" />

### 3. EBS (Elastic Block Store)

É o serviço da AWS que fornece armazenamento em bloco para instâncias EC2.

Com ele, você pode:

Criar discos virtuais para guardar dados de forma persistente;

Escolher o tipo de disco (rápido, padrão ou otimizado para I/O) conforme a necessidade;

Anexar ou desanexar volumes de uma instância EC2 facilmente;


Garantir que os dados permanecem salvos mesmo se a instância for desligada.


<img width="1022" height="693" alt="Captura de tela 2025-09-23 062941" src="https://github.com/user-attachments/assets/b8187108-3a29-4d26-b2d9-0c08087ede59" />

***
# Custos e serviços na AWS

A AWS segue o modelo OPEX (Despesa Operacional), ou seja, você paga apenas pelos recursos que usa.


<img width="1052" height="644" alt="Captura de tela 2025-09-23 212021" src="https://github.com/user-attachments/assets/80711d65-9db1-474b-a239-9718aa430f1f" />



Existem três modelos principais de seus serviços:

## IaaS, PaaS e SaaS – Modelos de Serviço na Nuvem

### 1. IaaS (Infraestrutura como Serviço)

Fornece servidores, armazenamento e rede na nuvem.

Você gerencia sistemas operacionais e aplicativos.

Ex.: EC2, EBS.

### 2. PaaS (Plataforma como Serviço)

Fornece uma plataforma completa para criar e rodar aplicativos.

A AWS gerencia a infraestrutura subjacente.

Ex.: Elastic Beanstalk, RDS.

### 3. SaaS (Software como Serviço)

Oferece softwares prontos para uso, totalmente gerenciados pelo provedor.

Você só usa o serviço, sem se preocupar com infraestrutura ou manutenção.

Ex.: WorkDocs, Chime.


<img width="1104" height="648" alt="Captura de tela 2025-09-23 212042" src="https://github.com/user-attachments/assets/ddfd9a0d-453b-4cd4-9af9-ef10f3d93ff4" />

***
# AMIs e Snapshots na AWS

### 1. AMI (Amazon Machine Image)

É uma imagem pronta de uma instância EC2, incluindo sistema operacional, aplicativos e configurações.

Permite criar novas instâncias rapidamente com a mesma configuração.

Pode ser pública (compartilhada) ou privada.


<img width="1111" height="659" alt="Captura de tela 2025-09-23 213113" src="https://github.com/user-attachments/assets/5ae86a29-bffb-4a3d-99ca-ad32abbd232e" />


### 2. Snapshot

É uma cópia de segurança de um volume EBS em determinado momento.

Usado para backup e recuperação de dados.

Pode ser usado para criar novos volumes EBS ou migrar dados entre regiões.


<img width="1104" height="549" alt="Captura de tela 2025-09-23 213149" src="https://github.com/user-attachments/assets/267eec41-10c8-457d-999f-07fd021ae856" />



<img width="1054" height="638" alt="Captura de tela 2025-09-23 213211" src="https://github.com/user-attachments/assets/b4516754-d209-4fb3-b5f1-ce4046f6076d" />

***

# Conclusão

A AWS é uma plataforma de nuvem flexível, segura e escalável, que oferece serviços de computação, armazenamento e bancos de dados para atender desde pequenos projetos até grandes empresas. Com modelos de custo e ferramentas que facilitam gerenciamento, automação e backup, ela permite criar e expandir ambientes digitais de forma prática e eficiente.







