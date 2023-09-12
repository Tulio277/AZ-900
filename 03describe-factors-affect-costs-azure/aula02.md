# AZ-900
### Descrever a finalidade do Microsoft Purview
- O Microsoft Purview é uma família de soluções de governança, risco e conformidade de dados que ajuda você a obter uma única exibição unificada em seus dados
- Com o Microsoft Purview, você pode se manter atualizado sobre seu cenário de dados graças a:
    - Descoberta de dados automatizada
    - Classificação de dados confidenciais
    - Linhagem de dados de ponta a ponta
- Duas áreas de solução principais compreendem o Microsoft Purview: 
    - risco e conformidade 
    - governança unificada de dados.
#### Soluções de risco e conformidade do Microsoft Purview
- Recursos do Microsoft 365 como um componente principal das soluções de risco e conformidade do Microsoft Purview.
- O Microsoft Purview, gerenciando e monitorando seus dados, pode ajudar sua organização:
    - Proteja dados confidenciais entre nuvens, aplicativos e dispositivos.
    - Identifique os riscos de dados e gerencie os requisitos de conformidade regulatória.
    - Introdução à conformidade regulatória.

#### Governança de dados unificada
- O Microsoft Purview tem soluções robustas e unificadas de governança de dados que ajudam a gerenciar seus dados locais, multinuvem e de software como serviço.
- A governança unificada de dados do Microsoft Purview ajuda sua organização:
    - Crie um mapa atualizado de todo o seu patrimônio de dados que inclua classificação de dados e linhagem de ponta a ponta.
    - Identifique onde os dados confidenciais são armazenados em sua propriedade.
    - Crie um ambiente seguro para que os consumidores de dados encontrem dados valiosos.
    - Gere insights sobre como seus dados são armazenados e usados.
    - Gerencie o acesso aos dados em sua propriedade com segurança e em escala.

### Descrever a finalidade do Azure Policy
- Como garantir que seus recursos permaneçam em conformidade? Você poderá receber um alerta se a configuração de um recurso for alterada?
- O Azure Policy é um serviço do Azure que permite criar, atribuir e gerenciar políticas que controlam ou auditam os recursos
#### Como o Azure Policy define as políticas?
- O Azure Policy permite que você defina políticas individuais e grupos de políticas relacionadas, conhecidas como iniciativas. 
- As Políticas do Azure podem ser definidas em cada nível, permitindo que você defina políticas em um recurso específico, um grupo de recursos, uma assinatura e assim por diante
- vem com definições de iniciativa e política internas para Armazenamento, Rede, Computação, Central de Segurança e Monitoramento
- pode corrigir automaticamente os recursos e as configurações sem conformidade para garantir a integridade do estado dos recursos.

#### O que são iniciativas do Azure Policy?
- Uma iniciativa do Azure Policy é uma forma de agrupar políticas relacionadas.
- A definição de iniciativa contém todas as definições de política para ajudar a acompanhar seu estado de conformidade para atingir uma meta maior
- Com essa iniciativa, as seguintes definições de política são incluídas:
    - Monitorar um banco de dados SQL não criptografado na Central de Segurança
    - Monitorar vulnerabilidades de SO na Central de Segurança
    - Monitorar o Endpoint Protection ausente na Central de Segurança

### Descrever a finalidade dos bloqueios de recursos
- Um bloqueio de recurso impede que os recursos sejam excluídos ou alterados acidentalmente.
#### Tipos de Bloqueios de Recursos
- Há dois tipos de bloqueios de recursos, um que impede que os usuários excluam e outro que impede que os usuários alterem ou excluam um recurso.
    - A exclusão significa que os usuários autorizados ainda poderão ler e modificar um recurso, mas não poderão excluir o recurso.
    - ReadOnly significa que os usuários autorizados poderão ler um recurso, mas não poderão excluir ou atualizar o recurso.
