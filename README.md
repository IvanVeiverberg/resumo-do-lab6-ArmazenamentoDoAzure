# Armazenamento do Azure
---
Este repositório contém o resumo das lições aprendidas durante o desenvolvimento do lab Armazenamento na Azure na plataforma DIO

---
## Introdução

Neste laboratório foram apresentados os principais conceitos relacionados aos serviços de armazenamento do Microsoft Azure, abrangendo desde tipos de armazenamento e redundância até gerenciamento e migração de dados. O objetivo é fornecer uma visão geral completa para aqueles que desejam se familiarizar com as opções e funcionalidades oferecidas pelo Azure para armazenamento de dados na nuvem.

## Serviços de Armazenamento

O Azure oferece uma variedade de serviços de armazenamento para atender diferentes necessidades, incluindo:

**1. Blob do Azure:**

- Ideal para armazenar grandes volumes de dados não estruturados, como arquivos de texto, imagens, vídeos e outros dados binários.
- Amplamente utilizado por aplicações que requerem flexibilidade na gestão de dados.

**2. Arquivos do Azure:**

- Permite a criação de compartilhamentos de arquivos de rede altamente disponíveis, acessíveis via protocolo SMB (Server Message Block).
- Compartilha a popularidade com o Blob do Azure, sendo frequentemente utilizado em cenários corporativos.

**3. Disco do Azure:**

- Oferece discos virtuais para máquinas virtuais, aplicações e outros serviços.
- Essencial para o funcionamento de ambientes de computação em nuvem que exigem armazenamento persistente.

**4. Fila do Azure:**

- Serviço de armazenamento de mensagens para lidar com grandes quantidades de mensagens.
- Cada mensagem pode ter até 64 KB.
- Utilizado em arquiteturas de aplicações assíncronas e distribuídas.

**5. Tabelas do Azure:**

- Armazenamento de dados estruturados NoSQL com um design sem esquema.
- Oferece um modelo chave/atributo para acesso rápido aos dados.

## Redundância de Armazenamento

A redundância garante a disponibilidade dos dados em caso de falhas. O Azure oferece diferentes opções de redundância:

**1. LRS (Locally Redundant Storage):**

- Cópias dos dados são mantidas no mesmo datacenter.
- **Não recomendado para produção**, pois uma falha no datacenter pode resultar na perda de dados.

**2. ZRS (Zone Redundant Storage):**

- Cópias dos dados são distribuídas em diferentes zonas de disponibilidade dentro da mesma região.
- Maior resiliência a falhas de datacenter, ideal para ambientes de produção.

**3. GRS (Geo-Redundant Storage):**

- Replicação dos dados para uma região secundária, garantindo a recuperação em caso de desastre regional.

**4. RA-GRS (Read-Access Geo-Redundant Storage):**

- Oferece acesso de leitura aos dados na região secundária, além da replicação para disaster recovery.

## Gerenciamento e Migração de Arquivos

O Azure disponibiliza ferramentas para gerenciar e migrar dados:

**1. AzCopy:**

- Utilitário de linha de comando para copiar blobs ou arquivos de/para contas de armazenamento.
- Realiza sincronização unidirecional.

**2. Gerenciador de Armazenamento do Azure:**

- Interface gráfica do usuário similar ao Windows Explorer para gerenciar arquivos.
- Compatibilidade com Windows, MacOS e Linux.

**3. Sincronização de Arquivos do Azure:**

- Sincronização bidirecional entre arquivos locais e do Azure.
- Mantém os arquivos frequentemente acessados localmente, liberando espaço na nuvem.

**4. Azure Data Box:**

- Serviço de migração física para transferir grandes volumes de dados (até 80 TB).
- Ideal para migrar dados de ambientes locais para o Azure, backups de recuperação de desastre e cenários com conectividade limitada.

**5. Migrações para Azure:**

- Plataforma unificada de migração com ferramentas integradas e autônomas para avaliação e migração de workloads para o Azure.

## Camadas de Acesso de Armazenamento

As camadas de acesso permitem otimizar custos de armazenamento com base na frequência de acesso:

- **Frequente:** Dados acessados com frequência.
- **Arquivo Morto:** Dados raramente acessados, ideal para backups e arquivamento.

O custo de armazenamento **diminui** à medida que os dados são movidos para camadas de acesso menos frequentes.

## Pontos de Extremidade Públicos do Serviço de Armazenamento

As contas de armazenamento do Azure devem:

- Ter um nome globalmente exclusivo.
- Fornecer acesso à internet em todo o mundo.
- Determinar os serviços de armazenamento e opções de redundância a serem utilizados. 



