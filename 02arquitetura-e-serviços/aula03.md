# AZ-900
## Descrever os serviços do armazenamento do Azure
### Descrever as contas de armazenamento do Azure
- Uma conta de armazenamento fornece um namespace exclusivo para os dados do Armazenamento do Azure que podem ser acessados de qualquer lugar do mundo por HTTP ou HTTPS
- O tipo de conta determina os serviços de armazenamento e as opções de redundância e tem impacto nos casos de uso
    - LRS (armazenamento com redundância local)
    - Armazenamento com redundância geográfica (GRS)
    - RA-GRS (armazenamento com redundância geográfica com acesso de leitura)
    - ZRS (armazenamento com redundância de zona)
    - Armazenamento com redundância de zona geográfica (GZRS)
    - RA-GZRS (armazenamento com redundância de zona geográfica com acesso de leitura)

### Pontos de extremidade da conta de armazenamento
- Ao nomear sua conta de armazenamento, lembre-se dessas regras
    - Os nomes da conta de armazenamento devem ter entre 3 e 24 caracteres e podem conter apenas números e letras minúsculas
    - O nome da sua conta de armazenamento deve ser exclusivo no Azure
- O nome da sua conta de armazenamento deve ser exclusivo no Azure
    - Armazenamento de Blobs	https://<storage-account-name>.blob.core.windows.net
    - Data Lake Storage Gen2	https://<storage-account-name>.dfs.core.windows.net
    - Arquivos do Azure	        https://<storage-account-name>.file.core.windows.net
    - Armazenamento de Filas	https://<storage-account-name>.queue.core.windows.net
    - Armazenamento de Tabelas	https://<storage-account-name>.table.core.windows.net

### Descrever a redundância de armazenamento do Azure
- O Armazenamento do Azure sempre armazena várias cópias dos seus dados para que eles fique protegidos contra eventos planejados e não planejados, como 
    - falhas de hardware transitórias 
    - interrupções de energia ou rede 
    - desastres naturais
- Os fatores que ajudam a determinar qual opção de redundância você deve escolher incluem:
    - Como os dados são replicados na região primária
    - Se os dados são replicados em uma segunda região que está geograficamente distante da região primária
    - Se o aplicativo requer acesso de leitura aos dados replicados na região secundária

### Redundância na região primária
- Os dados em uma conta de Armazenamento do Azure são sempre replicados três vezes na região primária
- O Armazenamento do Azure oferece duas opções para a replicação dos dados na região primária
    - LRS (armazenamento com redundância local)
        - O LRS replica seus dados três vezes em um único data center na região primária
        - O LRS oferece pelo menos 11 noves de durabilidade dos objetos em um determinado ano
        -  menor custo e oferece a menor durabilidade em comparação com outras opções
        - LRS protege seus dados contra falhas de unidade e rack do servidor
        - um incêndio ou uma inundação, todas as réplicas de uma conta de armazenamento que use o LRS poderão ser perdidas
    - ZRS (armazenamento com redundância de zona).
        - replica os dados do Armazenamento do Azure de maneira síncrona em três zonas de disponibilidade do Azure na região primária
        - oferece durabilidade para objetos de dados do Armazenamento do Azure de, pelo menos, 12 noves em um ano.
        - Com o ZRS, seus dados ainda podem ser acessados por operações de leitura e de gravação, mesmo em caso de não disponibilidade de uma zona
        - Se uma zona se tornar indisponível, o Azure realizará atualizações da rede, como o redirecionamento de DNS

### Redundância em uma região secundária
- Para aplicativos que exigem alta durabilidade, você pode optar por também copiar os dados em sua conta de armazenamento para uma região secundária que esteja a centenas de quilômetros de distância da região primária
- O Armazenamento do Azure oferece duas opções para copiar seus dados em uma região secundária:
    - GRS (armazenamento com redundância geográfica)
        - O GRS é semelhante à execução do LRS em duas regiões
        - O GRS copia seus dados três vezes em um único local físico na região primária usando LRS
        - O GRS oferece durabilidade para objetos de dados do Armazenamento do Azure de, pelo menos, 16 noves
    - GZRS (armazenamento com redundância de zona geográfica)
        - GZRS é semelhante à execução de ZRS na região primária e LRS na região secundária.
        - O GZRS combina a alta disponibilidade fornecida pela redundância entre zonas de disponibilidade com a proteção contra interrupções regionais fornecidas pela replicação geográfica
        - Os dados em uma conta de armazenamento GZRS são copiados entre três zonas de disponibilidade
        - A Microsoft recomenda o uso do GZRS para aplicativos que exigem consistência, durabilidade e disponibilidade máximas, excelente desempenho e resiliência para recuperação de desastres.

**Importante:**  Como os dados são replicados na região secundária de maneira assíncrona, uma falha que afete a região primária poderá resultar na perda de dados se a região primária não puder ser recuperada. O intervalo entre as gravações mais recentes na região primária e a última gravação na região secundária é conhecido como objetivo de ponto de recuperação (RPO)

### Descrever os serviços do armazenamento do Azure
- A plataforma de Armazenamento do Microsoft Azure inclui os seguintes serviços de dados:
    - Blobs do Azure: um repositório de objetos altamente escalonável para texto e dados binários
    - Arquivos do Azure: compartilhamentos de arquivos gerenciados para implantações locais e em nuvem
    - Filas do Azure: um armazenamento de mensagens para um sistema de mensagens
    - Azure Disks: volumes de armazenamento em nível de bloco para VMs do Azure.
    - Tabelas do Azure: opção de tabela NoSQL para dados estruturados e não relacionais.

### Benefícios do Armazenamento do Azure
- Durável e altamente disponível
- Seguro
- Escalonável
- Gerenciado
- Acessível

### Blobs do Azure
- O armazenamento de Blobs do Azure é uma solução de armazenamento de objetos para a nuvem
- Ele pode armazenar grandes quantidades de dados, como texto ou dados binários
- O armazenamento de Blobs do Azure não é estruturado
- Um blob pode conter gigabytes de dados binários transmitidos de um instrumento científico
- Uma vantagem do Armazenamento de Blobs em relação ao Armazenamento em Disco é que ele não exige que os desenvolvedores pensem em discos e nem os gerenciem
- O armazenamento de Blobs é ideal para:
    - Fornecimento de imagens ou de documentos diretamente a um navegador.
    - Armazenamento de arquivos para acesso distribuído.
    - Transmissão por streaming de áudio e vídeo.
    - Armazenamento de dados de backup e restauração, recuperação de desastres e arquivamento.
    - Armazenamento de dados para análise por um serviço local ou hospedado no Azure.
#### Camadas do Armazenamento de Blobs
- Os dados armazenados na nuvem podem crescer em um ritmo exponencial
- é útil organizar seus dados com base em atributos como frequência de acesso e período de retenção planejado
- Alguns dados são acessados com frequência no início do seu tempo de vida, mas esse acesso cai drasticamente à medida que os dados envelhecem
- As camadas de acesso disponíveis incluem:
    - Camada de acesso quente: otimizada para armazenar dados que são acessados com frequência
    - Camada de acesso frio: otimizada para dados acessados com menos frequência
    - Camada de acesso fria: otimizada para armazenamento de dados acessados com pouca frequência
    - Camada de acesso aos arquivos: adequada para dados acessados raramente

### Arquivos do Azure
- O armazenamento dos Arquivos do Azure oferece compartilhamento de arquivo totalmente gerenciado na nuvem e acessível por meio do protocolo SMB ou NFS (Network File System) padrão do setor
- É possível acessar os compartilhamentos de Arquivos do Azure com:
    - protocolo SMB em clientes Windows, Linux e macOS
    - protocolo NFS em clientes Linux e macOS
    - protocolo SMB podem ser armazenados em cache nos Windows Servers
#### Principais benefícios dos Arquivos do Azure:
- Acesso compartilhado
- Totalmente gerenciados
- Script e ferramentas
- Resiliência
- Programação familiar

### Filas do Azure
- O Armazenamento de Filas do Azure é um serviço usado para armazenar grandes quantidades de mensagens
- As filas são normalmente usadas para criar uma lista de pendências de trabalho

### Discos do Azure
-  armazenamento em disco do Azure ou o os discos gerenciados do Azure são volumes de armazenamento em nível de bloco gerenciados pelo Azure para serem usados com VMs do Azure.

### Tabelas do Azure
- O Armazenamento de Tabelas do Microsoft Azure armazena grandes quantidades de dados estruturados. As tabelas do Azure são um repositório de dados NoSQL que aceita chamadas autenticadas de dentro e de fora da nuvem do Azure

### Identificar as opções de migração de dados do Azure
#### Migrações para Azure
- O Migrações para Azure é um serviço que ajuda você a migrar de um ambiente local para a nuvem
- O Migrações para Azure funciona como um hub para ajudar você a gerenciar a avaliação e a migração do datacenter local para o Azure
    - Plataforma de migração unificada
    - Variedade de ferramentas:
    - Avaliação e migração:

### Ferramentas integradas
- Além de trabalhar com ferramentas de ISVs, o hub do Migrações para Azure também inclui as seguintes ferramentas para ajudar na migração:
    - Migrações para Azure: Descoberta e avaliação.
    - Migrações para Azure: Migração de Servidor
    - Assistente de Migração de Dados.
    - Serviço de Migração de Banco de Dados do Azure
    - Assistente de migração de aplicativo Web
    - Azure Data Box

### Azure Data Box
- O Azure Data Box é um serviço de migração física que ajuda a transferir grandes quantidades de dados de maneira rápida, barata e confiável
- O Data Box é transportado entre o datacenter por meio de uma empresa regional
- Você pode solicitar o dispositivo Data Box pelo portal do Azure para importar dados de ou exportar dados para o Azure
-  Todo o processo é acompanhado de ponta a ponta pelo serviço Data Box no portal do Azure

#### Casos de uso
- O Data Box é ideal para transferir os tamanhos de dados maiores do que 40 TB em cenários com conectividade de rede limitada a inexistente.
- cenários em que o Data Box pode ser usado para importar dados para o Azure.
    - Migração única - grande volume de dados do local é transferido para o Azure.
    - Movimentação de uma biblioteca de mídia de fitas offline para o Azure para a criação de uma de mídia online.
    - Migração do farm de VMs, do SQL Server e de aplicativos para o Azure.
    - Migração de dados históricos para o Azure para análise e relatórios detalhados com o HDInsight.
    - Transferência em massa inicial – quando uma transferência em massa inicial é feita usando o Data Box
    - Carregamentos periódicos - quando grandes quantidades de dados são geradas periodicamente
- cenários em que o Data Box pode ser usado para exportar dados do Azure.
    - Recuperação de desastre – quando uma cópia dos dados do Azure é restaurada para uma rede local
    - Requisitos de segurança – quando você precisa ser capaz de exportar dados provenientes do Azure devido a requisitos governamentais ou de segurança.
    - Migre de volta para o local ou para outro provedor de serviços de nuvem

### Identificar as opções de movimentação de arquivos do Azure
- Além da migração em larga escala usando serviços como Migrações para Azure e Azure Data Box, o Azure também tem ferramentas projetadas para ajudar você a mover ou interagir com arquivos individuais ou grupos de arquivos pequenos.
- Entre essas ferramentas estão AzCopy, Gerenciador de Armazenamento do Azure e Sincronização de Arquivos do Azure.

#### AzCopy
- AzCopy é um utilitário de linha de comando que você pode usar para copiar blobs ou arquivos de/para uma conta de armazenamento
- Você pode carregar arquivos, baixar arquivos, copiar arquivos entre contas de armazenamento e até mesmo sincronizar arquivos.

#### Gerenciador de Armazenamento do Azure
- é um aplicativo autônomo que fornece uma interface gráfica para gerenciar arquivos e blobs em sua Conta do Armazenamento do Azure.
- Ele funciona em sistemas operacionais Windows, macOS e Linux e usa o AzCopy no back-end para executar todas as tarefas de gerenciamento de arquivos e blobs
- você pode carregar no Azure, baixar do Azure ou mover entre contas de armazenamento.

### Sincronização de Arquivos do Azure
- A Sincronização de Arquivos do Azure é uma ferramenta que permite centralizar seus compartilhamentos de arquivos no serviço Arquivos do Azure e manter a flexibilidade, o desempenho e a compatibilidade de um servidor de arquivos do Windows.
- Com a Sincronização de Arquivos do Azure, você pode:
    - Usar qualquer protocolo disponível no Windows Server para acessar seus dados localmente, incluindo SMB, NFS e FTPS.
    - Ter tantos caches quantos precisar em todo o mundo.
    - Substituir um servidor local com falha instalando a Sincronização de Arquivos do Azure em um novo servidor no mesmo datacenter.
    - Configurar a camada de nuvem para que os arquivos acessados com mais frequência sejam replicados localmente,