# AZ-900
### Descrever ferramentas para interagir com o Azure
- O Azure fornece várias ferramentas para gerenciar seu ambiente, incluindo:
    - Portal do Azure
    - Azure PowerShell
    - CLI (Interface de Linha de Comando) do Azure.
#### O que é o portal do Azure?
- é um console unificado baseado na Web que fornece uma alternativa para as ferramentas de linha de comando
- você pode gerenciar a assinatura do Azure usando uma interface gráfica do usuário. Você pode:
    - Compile, gerencie e monitore tudo, desde aplicativos Web simples a implantações em nuvem complexas
    - Crie painéis personalizados para ter uma exibição organizada dos recursos
    - Configure opções de acessibilidade para ter a experiência ideal

#### Azure Cloud Shell
- é uma ferramenta de shell baseada em navegador que permite criar, configurar e gerenciar recursos do Azure usando um shell
- tem vários recursos que o tornam uma oferta exclusiva para dar suporte ao gerenciamento do Azure
    - É uma experiência de shell baseada em navegador sem a necessidade de instalação ou configuração local.
    - é autenticado em suas credenciais do Azure, portanto, quando você faz logon, ele sabe inerentemente quem você é e quais permissões você tem.
    - Você escolhe o shell com o qual está mais familiarizado;

#### O que é a CLI do Azure?
- A CLI do Azure é funcionalmente equivalente ao Azure PowerShell, sendo a principal diferença a sintaxe dos comandos
- Enquanto o Azure PowerShell usa comandos do PowerShell, a CLI do Azure usa comandos Bash.

### Descrever a finalidade do Azure Arc
- O gerenciamento de ambientes híbridos e de várias nuvens pode se complicar rapidamente
- O Azure oferece uma série de ferramentas para provisionar, configurar e monitorar recursos do Azure
- O Azure Arc fornece uma forma centralizada e unificada para:
    - Gerenciar todo o seu ambiente projetando os recursos que não são do Azure no ARM.
    - Gerencie máquinas virtuais híbridas e de várias nuvens, clusters do Kubernetes e bancos de dados
    - Use as funcionalidades familiares de gerenciamento e serviços do Azure, independentemente de onde eles estejam hospedados.
    - Continuar usando a ITOps tradicional, introduzindo práticas de DevOps para dar suporte a novos padrões nativos de nuvem no seu ambiente.
    - Configurar localizações personalizadas como uma camada de abstração no cluster de Kubernetes
#### O que o Azure Arc pode fazer fora do Azure?
- Atualmente, o Azure Arc permite que você gerencie os seguintes tipos de recursos hospedados fora do Azure:
    - Servidores
    - Clusters do Kubernetes
    - Serviços de Dados do Azure
    - SQL Server
    - Máquinas virtuais (versão prévia)
### Descrever modelos do Azure Resource Manager e do ARM do Azure
- O ARM (Azure Resource Manager) é o serviço de implantação e gerenciamento do Azure
- Sempre que você faz qualquer coisa com seus recursos do Azure, o ARM está envolvido.
- Quando um usuário envia uma solicitação de ferramentas, APIs ou SDKs do Azure, o ARM recebe a solicitação.

#### Benefícios do Azure Resource Manager
- Com o Azure Resource Manager, você pode:
    - Gerenciar sua infraestrutura por meio de modelos declarativos em vez de scripts
    - implantar, gerenciar e monitorar todos os recursos da sua solução como um grupo em vez de tratá-los individualmente.
    - Reimplantar a solução durante o ciclo de vida de desenvolvimento
    - Definir as dependências entre os recursos para que eles sejam implantados na ordem correta.
    - Aplicar o controle de acesso a todos os serviços porque o RBAC é integrado nativamente à plataforma de gerenciamento.
    - Aplicar marcas aos recursos para organizar de modo lógico todos os recursos em sua assinatura.
    - Esclarecer a cobrança da organização exibindo os custos de um grupo de recursos que compartilham a mesma marca.


#### Infraestrutura como código
- A infraestrutura como código é um conceito em que você gerencia sua infraestrutura como linhas de código
- você pode usar a infraestrutura como conceito de código para gerenciar implantações inteiras usando modelos e configurações repetíveis.

#### Modelos de ARM
- Ao usar os modelos do ARM, você pode descrever os recursos que deseja usar em um formato JSON declarativo
- Com um modelo do ARM, o código de implantação é verificado antes da execução de qualquer código. Isso garante que os recursos serão criados e conectados corretamente
- o DevOps profissional ou o profissional de TI precisa apenas definir o estado desejado e a configuração de cada recurso no modelo do ARM e o modelo fará o resto

#### Benefícios de usar modelos do ARM
- Os modelos do ARM proporcionam muitos benefícios ao planejar a implantação de recursos do Azure. Alguns desses benefícios incluem:
    - Sintaxe declarativa
    - Resultados repetidos
    - Orquestração
    - Arquivos modulares
    - Extensibilidade

#### Bicep
- O Bicep é uma linguagem que usa sintaxe declarativa para implantar recursos do Azure
- Embora semelhante a um modelo do ARM, que é escrito em JSON, os arquivos Bicep tendem a usar um estilo mais simples e conciso.
- Alguns benefícios do Bicep são:
    - Suporte para todos os tipos de recursos e versões de API:
    - Sintaxe simples
    - Resultados repetidos
    - Orquestração
    - Modularidade