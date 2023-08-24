# AZ-900
## Descrever Máquinas Virtuais do Azure
- Com as VMs do Azure, você pode criar e usar VMs na nuvem
-  Como em um computador físico, você pode personalizar todos os programas de software em execução na VM
- As VMs são uma opção ideal quando você precisa de:
    - Controle total sobre o SO (sistema operacional).
    - Capacidade para executar um software personalizado.
    - Usar configurações personalizadas de hospedagem.
- Uma imagem é um modelo usado para criar uma VM e pode já incluir um sistema operacional e outros softwares

## Dimensionar VMs no Azure
- Você pode executar VMs únicas para teste, desenvolvimento ou para tarefas secundárias
- Pode agrupar VMs para fornecer alta disponibilidade, escalabilidade e redundância

### conjuntos de escala de máquina virtual
- Os Conjuntos de Dimensionamento de Máquinas Virtuais permitem criar e gerenciar um grupo de VMs idênticas e com balanceamento de carga
- com conjuntos de dimensionamento de máquinas virtuais, o Azure automatiza a maior parte desse trabalho.
- Os conjuntos de dimensionamento permitem que você gerencie, configure e atualize centralmente um grande número de VMs em minutos

## Conjuntos de disponibilidade da máquina virtual
- Os conjuntos de disponibilidade de máquinas virtuais são outra ferramenta para ajudá-lo a criar um ambiente mais resiliente e altamente disponível
-  Garantir que as VMs escalonem atualizações e tenham conectividade de rede e energia variadas
- Os conjuntos de disponibilidade fazem isso agrupando VMs de duas maneiras: domínio de atualização e domínio de falha.
    - Domínio de atualização: as VMs de grupos de domínio de atualização que podem ser reinicializadas ao mesmo tempo.
    - Domínio de falha: o domínio de falha agrupa suas VMs por origem de energia comum e comutador de rede

## Exemplos de quando usar VMs
- Alguns exemplos comuns ou casos de uso para máquinas virtuais incluem:
    - Durante o teste e o desenvolvimento. As VMs fornecem uma maneira rápida e fácil de criar diferentes configurações de sistema operacional e de aplicativo
    - Ao executar aplicativos na nuvem. A capacidade de executar determinados aplicativos na nuvem pública, em vez de criar uma infraestrutura tradicional para executá-los
    - Ao estender seu datacenter para a nuvem: uma organização pode estender os recursos de sua própria rede local criando uma rede virtual no Azure e adicionando VMs a ela
    - Durante a recuperação de desastre: assim como acontece com a execução de determinados tipos de aplicativos na nuvem e com a extensão de uma rede local para a nuvem

## Migrar para a nuvem com VMs
- As VMs também são uma excelente opção quando você migra de um servidor físico para a nuvem (também conhecido como lift-and-shift).
- Você pode criar uma imagem do servidor físico e hospedá-la em uma VM com poucas ou nenhuma alteração

## Recursos da VM
- Tamanho (finalidade, número de núcleos de processador e quantidade de RAM)
- Discos de armazenamento (unidades de disco rígido, unidades de estado sólido etc.)
- Rede (rede virtual, endereço IP público e configuração de porta)

## Descrever a Área de Trabalho Virtual do Azure
- A Área de Trabalho Virtual do Azure é um serviço de virtualização de área de trabalho e aplicativos que é executado na nuvem
- Ele permite que você use uma versão do Windows hospedada na nuvem em qualquer localização.

## Aprimorar a segurança 
- A Área de Trabalho Virtual do Azure oferece gerenciamento de segurança centralizado para as áreas de trabalho dos usuários com o Azure AD (Azure Active Directory)
- Os dados e aplicativos ficam separados do hardware local

## Descrever contêineres do Azure
- Se você quer executar várias instâncias de um aplicativo em um só computador host
## O que são contêineres?
- Contêineres são um ambiente de virtualização
- você pode executar vários contêineres em apenas um host físico ou virtual
- Os contêineres são leves e projetados para serem criados, dimensionados e interrompidos dinamicamente

## Instâncias de Contêiner do Azure
- As Instâncias de Contêiner do Azure oferecem a maneira mais rápida e simples de executar um contêiner no Azure, sem a necessidade de gerenciar máquinas virtuais nem adotar serviços adicionais

## Aplicativos de Contêiner do Azure
- Eles permitem que você comece a trabalhar imediatamente, removem a parte de gerenciamento de contêineres e são uma oferta de PaaS

## Serviço de Kubernetes do Azure
- Serviço de Kubernetes do Azure (AKS) é um serviço de orquestração de contêiner

## Usar contêineres em suas soluções
- Contêineres geralmente são usados para criar soluções que utilizam uma arquitetura de microsserviço
- Essa arquitetura é onde você divide as soluções em partes menores e independentes

## Descrever Azure Functions
- O Azure Functions é uma opção de computação sem servidor controlada por eventos que não requer a manutenção de máquinas virtuais ou contêineres
- Com o Azure Functions, um evento desperta a função, reduzindo a necessidade de manter os recursos provisionados quando não há eventos.

## Benefícios do Azure Functions
- é ideal quando você está preocupado apenas com o código que executa o serviço
- temporizador ou uma mensagem de outro serviço do Azure - conclusão em segundos
- As funções são dimensionadas automaticamente com base na demanda
- As funções podem ser sem estado ou com estado
    - sem estado (o padrão), elas se comportam como se fossem reiniciadas sempre que respondem a um evento
    - com estado (chamadas de Durable Functions), um contexto é passado pela função para acompanhar a atividade anterior
- As funções são um componente chave da computação sem servidor.

## Descrever as opções de hospedagem de aplicativo
- Se você precisar hospedar seu aplicativo no Azure, poderá inicialmente recorrer a uma VM (máquina virtual) ou contêineres
## Serviço de aplicativo do Azure
- O Serviço de Aplicativo permite que você crie e hospede aplicativos Web, trabalhos em segundo plano, back-ends de dispositivos móveis e APIs RESTful na linguagem de programação de sua escolha sem gerenciar a infraestrutura
- oferece dimensionamento automático e alta disponibilidade
- é uma opção de hospedagem robusta que você pode usar para hospedar seus aplicativos
- permite que você se concentre em criar e manter seu aplicativo

## Tipos de serviços de aplicativos
- Aplicativos Web
    - inclui suporte completo para a hospedagem de aplicativos Web usando ASP.NET, ASP.NET Core
    - Windows ou Linux como sistema operacional do host
- Aplicativos de API
    - você pode criar APIs Web baseadas em REST usando a linguagem e a estrutura que você quiser
    - suporte completo do Swagger e a capacidade de empacotar e publicar sua API no Azure Marketplace
- WebJobs
    - recurso do WebJobs para executar um script
    - podem ser agendados ou executados por um gatilho
    - é usado para executar tarefas em segundo plano
- Aplicativos móveis
    - Armazenar dados de aplicativo móvel em um Banco de Dados SQL baseado em nuvem.
    - Autenticar os clientes em relação a provedores sociais comuns, como MSA, Google, Twitter e Facebook.
    - Enviar notificações por push.
    - Executar a lógica personalizada de back-end no C# ou Node.js.

## Descrever a Rede Virtual do Azure
- As redes virtuais e as sub-redes virtuais do Azure permitem que recursos do Azure, como VMs, aplicativos Web e bancos de dados, comuniquem-se uns com os outros, com usuários na Internet e com computadores cliente locais.
- As redes virtuais do Azure oferecem as seguintes funcionalidades de rede essenciais:
    - Isolamento e segmentação
    - Comunicação pela Internet
    - Comunicação entre recursos do Azure
    - Comunicação com os recursos locais
    - Rotear tráfego de rede
    - Filtrar tráfego de rede
    - Conectar redes virtuais
- A rede virtual do Azure dá suporte a pontos de extremidade públicos e privados
    - Pontos de extremidade públicos têm um endereço IP público e podem ser acessados de qualquer lugar do mundo
    - Pontos de extremidade privados existem em uma rede virtual e têm um endereço IP privado dentro do espaço de endereço dessa rede virtual.

## Isolamento e segmentação
- Quando você configura uma rede virtual, define um espaço de endereço IP privado usando intervalos de endereços IP públicos ou privados
- Para a resolução de nomes, é possível usar o serviço de resolução de nomes interno do Azure

## Comunicações com a Internet
- É possível habilitar conexões de entrada da Internet atribuindo um endereço IP público a um recurso do Azure ou colocar o recurso atrás de um balancear carga público.
## Comunicação entre recursos do Azure
- Você pode fazer isso de duas maneiras:
    - As redes virtuais podem conectar não apenas VMs, mas outros recursos do Azure, como Ambiente do Serviço de Aplicativo para Power Apps, Serviço de Kubernetes
    - Os pontos de extremidade de serviço podem se conectar a outros tipos de recursos do Azure, como bancos de dados SQL do Azure e contas de armazenamento

## Comunicação com os recursos locais
- As redes virtuais do Azure permitem vincular recursos em seu ambiente local e na assinatura do Azure
- Há três mecanismos para você obter essa conectividade
    - As conexões de rede virtual privada ponto a site são de um computador fora da organização de volta para a rede corporativa
    - Redes virtuais privadas site a site vinculam seu dispositivo VPN ou gateway de VPN local ao Gateway de VPN do Azure em uma rede virtual
    - O Azure ExpressRoute fornece uma conectividade privada dedicada para o Azure que não passa pela Internet. 

## Rotear tráfego de rede
- Por padrão, o Azure faz o roteamento de tráfego entre sub-redes em redes virtuais conectadas, em redes locais e na Internet.
- Você também pode controlar o roteamento e substituir essas configurações da seguinte maneira:
    - As tabelas de rotas permitem definir regras sobre como o tráfego deve ser direcionado.
    - O BGP (Border Gateway Protocol) funciona com Gateways de VPN do Azure, Servidor de Rota do Azure ou Azure ExpressRoute para propagar as rotas BGP locais para redes virtuais do Azure.

## Filtrar tráfego de rede
- As redes virtuais do Azure permitem filtrar o tráfego entre sub-redes usando as seguintes abordagens:
    - Grupos de segurança de rede são recursos do Azure que podem conter várias regras de segurança de entrada e saída.
    - Soluções de virtualização de rede são VMs especializadas que podem ser comparadas a um dispositivo de rede protegida.
## Conectar redes virtuais
- Você pode vincular redes virtuais usando o emparelhamento dessas redes.
- O emparelhamento permite que duas redes virtuais se conectem diretamente entre si.
- O emparelhamento permite que os recursos em cada rede virtual se comuniquem entre si
- As UDR (rotas definidas pelo usuário) permitem controlar as tabelas de roteamento entre sub-redes em uma rede virtual

