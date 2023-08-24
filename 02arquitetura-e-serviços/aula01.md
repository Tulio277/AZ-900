# AZ-900
### O que é o Microsoft Azure
- O Azure é um conjunto de serviços de nuvem, em constante expansão, que ajuda você a superar os desafios empresariais atuais e se preparar para os desafios futuros. O Azure oferece a liberdade de criar, gerenciar e implantar aplicativos em uma enorme rede global usando suas ferramentas e estruturas favoritas.

### O que o Azure oferece?
- pronto para o futuro: suporte ao desenvolvimento dos negócios no presente e às visões de produto para o futuro.
- Crie de acordo com seus termos: suporte para todos as linguagens e estruturas, implante onde preferir.
- Opere de modo contínuo: localmente, na nuvem e na borda, integre e gerencie seus ambientes com ferramentas e serviços projetados para uma solução de nuvem híbrida.
- Confie em sua nuvem: obtenha segurança desde o início apoiada por uma equipe de especialistas.

## Introdução a contas do Azure
- Para criar e usar os serviços do Azure, você precisa de uma assinatura do Azure
- Depois de criar uma conta do Azure, você poderá criar assinaturas adicionais. Por exemplo: 
    - conta do Azure para departamentos de desenvolvimento, 
    - conta do Azure para departamentos de marketing 
    - conta do Azure para departamentos de vendas. 
- Depois de criar uma assinatura do Azure, você poderá começar a criar recursos do Azure dentro de cada assinatura.

### Criar uma conta do Azure
- Inscrevendo-se no site do Azure ou por meio de um representante da Microsoft. 
- Também é possível comprá-lo por meio de um parceiro da Microsoft.

### O que é a conta gratuita do Azure?
- Acesso gratuito a produtos populares do Azure por 12 meses.
- Um crédito a ser usado nos primeiros 30 dias.
- Acesso a mais de 25 produtos que são sempre gratuitos.

### O que é a área restrita do Microsoft Learn?
- Assinatura temporária permite que você crie recursos do Azure durante o módulo do Microsoft Learn


### Exercício – Explorar a área restrita do Learn

## Descrever a infraestrutura física do Azure
-  Os principais componentes da arquitetura do Azure podem ser divididos em dois agrupamentos principais: 
    - infraestrutura física
    - infraestrutura de gerenciamento

### Infraestrutura física
- São instalações com recursos organizados em racks com energia, refrigeração e infraestrutura de rede dedicadas.
### Regiões
- região é uma área geográfica do planeta que contém pelo menos um data center
- Quando você implanta um recurso no Azure, precisa escolher a região em que deseja que ele seja implantado
- Alguns serviços ou recursos de VM estão disponíveis somente em determinadas regiões, como 
    - tamanhos específicos de VMs
    - tipos de armazenamento
- há alguns serviços globais do Azure que não exigem que você selecione uma região específica, como o 
    - Azure Active Directory, 
    - Gerenciador de Tráfego do Azure 
    - DNS do Azure
### Zonas de Disponibilidade
- são datacenters separados fisicamente dentro de uma região do Azure
- Cada zona de disponibilidade é composta de um ou mais datacenters
- Zonas de disponibilidade são conectadas por meio de redes de fibra óptica privadas de alta velocidade

**Importante:** Para garantir a resiliência, no mínimo três zonas de disponibilidade separadas estão presentes em todas as regiões habilitadas para zona de disponibilidade. No entanto, nem todas as Regiões do Azure atualmente dão suporte a zonas de disponibilidade

### Pares de regiões
- Essa abordagem permite a replicação de recursos em uma geografia, o que ajuda a reduzir a probabilidade de interrupções devido a eventos como desastres naturais

**Importante:** Nem todos os serviços do Azure replicam dados automaticamente ou retornam automaticamente de uma região com falha para replicação cruzada para outra região habilitada. Nesses cenários, a recuperação e a replicação devem ser configuradas pelo cliente.

#### Vantagens adicionais dos pares de regiões:
- Se ocorrer uma interrupção ampla do Azure, uma região de cada par será priorizada
- As atualizações planejadas do Azure são distribuídas para regiões emparelhadas uma por vez
- Os dados continuam residindo na mesma geografia que seu par (com exceção do Sul do Brasil) para fins de jurisdição

### Regiões soberanas
- Regiões soberanas são instâncias do Azure isoladas da instância principal do Azure

## gerenciamento do Azure
- A infraestrutura de gerenciamento inclui recursos do Azure e grupos de recursos, assinaturas e contas
### Recursos e grupos de recursos do Azure
- Um recurso é o bloco de construção básico do Azure
- VMs (máquinas virtuais), redes virtuais, bancos de dados, serviços cognitivos etc.
- Quando você aplicar uma ação a um grupo de recursos, essa ação será aplicada a todos os recursos dentro do grupo de recursos
- grupos de recursos são um modo de organizar logicamente os recursos

### Assinaturas do Azure
- são uma unidade de gerenciamento, cobrança e escala
- as assinaturas permitem organizar logicamente seus grupos de recursos e facilitar a cobrança
- Você pode usar dois tipos de limites de assinatura:
    - Limite de cobrança: Esse tipo de assinatura determina como uma conta do Azure é cobrada pelo uso do Azure
    - Limite de controle de acesso: O Azure aplica políticas de gerenciamento de acesso no nível da assinatura

### Criar assinaturas adicionais do Azure
-  para separar recursos por função ou acesso,
    - Ambientes
    - Estruturas organizacionais
    - Cobrança
### Grupos de gerenciamento do Azure
- Se você tiver muitas assinaturas, talvez precise de um modo de gerenciar o acesso, as políticas e a conformidade com eficiência para essas assinaturas
- Você organiza as assinaturas em contêineres chamados grupos de gerenciamento e aplica as condições de governança a esses grupos.