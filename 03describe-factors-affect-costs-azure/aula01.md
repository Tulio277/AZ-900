# AZ-900
### Descrever fatores que podem afetar os custos no Azure
- O Azure desloca os custos de desenvolvimento de CapEx (despesa de capital) de criar e manter a infraestrutura e instalações para OpEx (despesa operacional) de alugar a infraestrutura conforme necessário, seja computação, armazenamento, rede etc.
    - Tipo de recurso
    - Consumo
    - Manutenção
    - painel Geografia do app's selecionado
    - Tipo de assinatura
    - Azure Marketplace

#### Tipo de recurso
- as configurações do recurso e a região do Azure afetarão o custo de um recurso
- Quando você provisiona um recurso do Azure, a plataforma cria instâncias limitadas para esse recurso

#### Consumo
- O pagamento conforme o uso é um tema consistente em todo o processo
-  Azure também permite que o usuário se comprometa a usar uma quantidade definida de recursos de nuvem com antecedência e receber descontos nesses recursos "reservados"
- Quando você reserva capacidade, você está se comprometendo a usar e pagar por uma determinada quantidade de recursos do Azure durante um determinado período

#### Manutenção
- A flexibilidade da nuvem possibilita ajustar rapidamente os recursos com base na demanda
- O uso de grupos de recursos pode ajudar a manter todos os seus recursos organizados
- Para controlar os custos, é importante manter o ambiente de nuvem

#### painel Geografia do app's selecionado
- Ao provisionar a maioria dos recursos no Azure, você precisa definir uma região em que o recurso é implantado
- O tráfego de rede também é afetado conforme a área geográfica.
    - As zonas de cobrança são um fator para determinar o custo de alguns serviços do Azure.
    - A largura de banda refere-se aos dados que entram e saem dos datacenters do Azure.
    - Uma zona é um agrupamento geográfico de regiões do Azure para fins de cobrança

#### Tipo de assinatura
- Alguns tipos de assinatura do Azure também incluem as concessões de uso, que afetam os custos.
- uma assinatura de avaliação gratuita do Azure fornece acesso a vários produtos do Azure gratuitos por 12 meses.

#### Azure Marketplace
- O Azure Marketplace permite comprar soluções e serviços baseados no Azure de fornecedores de terceiros
    -  servidor com software pré-instalado e configurado
    - dispositivos de firewall de rede gerenciados
    - conectores para serviços de backup de terceiros

### Comparar as calculadoras Preço e Custo Total de Propriedade
- A calculadora de preços e a calculadora TCO (custo total de propriedade) ajudam a entender possíveis despesas do Azure.

#### Calculadora de preço
- A calculadora de preços foi projetada para fornecer um custo estimado para provisionar recursos no Azure
- A calculadora de preços é apenas para fins informativos
- você pode estimar o custo de todos os recursos provisionados, incluindo computação, armazenamento e custos de rede associados. 

#### Calculadora de TCO
- infraestrutura local versus uma infraestrutura de nuvem do Azure.
- você insere sua configuração de infraestrutura atual, incluindo servidores, bancos de dados, armazenamento e tráfego de rede de saída.

### Descreva a ferramenta Gerenciamento de Custos da Microsoft
- O Microsoft Azure é um provedor de nuvem global, o que significa que você pode provisionar recursos em qualquer lugar do mundo.
-  Se você provisionar acidentalmente novos recursos, talvez não esteja ciente deles até a hora da fatura. 
- O Gerenciamento de Custos é um serviço que ajuda a evitar essas situações.

#### O que é o Gerenciamento de Custo?
- O Gerenciamento de Custos permite 
     - verificar rapidamente os custos de recursos do Azure
     - criar alertas com base nos gastos com recursos
     - criar orçamentos que podem ser usados para automatizar o gerenciamento de recursos.

#### Alertas de custo
- Os alertas de custo fornecem um só local para verificar rapidamente todos os diferentes tipos de alerta
    - Alertas de orçamento
    - Alertas de crédito
    - Alertas de cota de gastos do departamento.
##### Alertas de orçamento
-  notificam você quando os gastos, com base em uso ou custos, atingem ou excedem o valor definido na condição de alerta do orçamento
##### Alertas de crédito
- notificam você quando seus compromissos monetários de crédito do Azure são consumidos
- Sempre que um alerta é gerado, ele se reflete nos alertas de custo e no email enviado aos proprietários da conta.
##### Alertas de cota de gasto do departamento
- notificam você quando os gastos do departamento atingem um limite fixo da cota
- As cotas de gasto são configuradas no Portal do EA. Sempre que um limite é atingido, ele gera um email para os proprietários do departamento

#### Orçamentos
- define um limite de gastos para o Azure
- pode definir orçamentos com base em uma assinatura, grupo de recursos, tipo de serviço ou outros critérios
- Um uso mais avançado de orçamentos permite que as condições orçamentárias disparem a automação que suspende ou modifica recursos depois que a condição de gatilho ocorre.

### Descrever a finalidade das marcas
- À medida que o seu uso de nuvem aumenta, passa a ser cada vez mais importante manter-se organizado.
- Uma forma de organizar os recursos relacionados é colocá-los nas próprias assinaturas
- As marcas de recursos são outra maneira de organizar os recursos
- As marcas fornecem informações extras ou metadados sobre os recursos. Esses metadados são úteis para:
    - Gerenciamento de recursos
    - Gerenciamento e otimização de recursos 
    - Gerenciamento de operações
    - Segurança
    - Governança e conformidade regulatória
    - Automação e otimização de carga de trabalho 

#### Como fazer para gerenciar marcas de recursos?
- Você pode adicionar, modificar ou excluir marcas de recursos por meio do Windows PowerShell, da CLI do Azure, dos modelos do Azure Resource Manager, da API REST ou do portal do Azure.
- Você pode usar o Azure Policy para impor a marcação de regras e convenções.