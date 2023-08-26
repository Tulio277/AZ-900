# AZ-900
### Descrever os serviços de diretório do Azure
- O Azure AD (Azure Active Directory) é um serviço de diretório que permite que você entre e acesse aplicativos de nuvem da Microsoft e aplicativos de nuvem que você desenvolve
- Em ambientes locais, o Active Directory em execução no Windows Server fornece um serviço de gerenciamento de identidade e acesso gerenciado pela sua organização
- você controla as contas de identidade, mas a Microsoft garante que o serviço esteja disponível globalmente

### Quem usa o Azure AD?
- Administradores de TI
- Desenvolvedores de aplicativos
- Usuários
- Assinantes do serviço online

### O que o Azure AD faz?
- Autenticação
- Logon único
- Gerenciamento de aplicativo
- Gerenciamento de dispositivo

### Posso conectar meu AD local com Azure AD?
-  você pode conectar o Active Directory com o Azure AD, possibilitando uma experiência de identidade consistente entre a nuvem e o local.
- Um método de conexão do Azure AD com o AD local é usar o Azure AD Connec
- Azure AD Connect sincroniza alterações entre os dois sistemas de identidade

### O que é o Azure Active Directory Domain Services?
- O Azure AD DS (Azure Active Directory Domain Services) é um serviço que fornece serviços de domínio gerenciado, como ingresso no domínio, política de grupo, protocolo LDAP e autenticação Kerberos/NTLM
- Você pode realizar lift-and-shift desses aplicativos herdados do seu ambiente local para um domínio gerenciado, sem a necessidade de gerenciar o ambiente de AD DS na nuvem.
- O Azure AD DS integra-se com o seu locatário existente do Azure AD

### Como funciona o Azure AD DS?
- Ao criar um domínio gerenciado do Azure AD DS, você define um namespace exclusivo. Esse namespace é o nome de domínio
- A plataforma do Azure manipula os DCs como parte do domínio gerenciado, incluindo backups e a criptografia em repouso usando o Azure Disk Encryption.

### Descrever os métodos de autenticação do Azure
- Autenticação é o processo de estabelecer a identidade de uma pessoa, um serviço ou um dispositivo
- Ela não confirma que você tem a passagem, só prova que você é quem diz ser.

### O que é o logon único?
- O SSO (logon único) permite que um usuário entre uma vez e use essa credencial para acessar vários recursos e aplicativos de provedores diferente
- Um número maior de identidades significa mais senhas para se lembrar e alterar.

**Importante** O logon único será tão seguro quanto o autenticador inicial, pois as conexões subsequentes serão todas baseadas na segurança do autenticador inicial.

### O que é a Autenticação multifator?
- A autenticação multifator é o processo de solicitar a um usuário uma forma (ou um fator) adicional de identificação durante o processo de entrada
- A autenticação multifator fornece segurança adicional para as identidades, exigindo dois ou mais elementos para a autenticação completa
    - Algo que o usuário saiba– essa pode ser uma pergunta de desafio.
    - Algo que o usuário tenha – pode ser um código enviado para o telefone celular do usuário
    - Algo que o usuário seja – normalmente é algum tipo de propriedade biométrica

#### O que é a Autenticação Multifator do Azure AD?
- A Autenticação Multifator do Azure AD é um serviço da Microsoft que fornece funcionalidades de autenticação multifator.
- A Autenticação Multifator do Azure AD permite que os usuários escolham uma forma adicional de autenticação durante a conexão, como uma chamada telefônica ou uma notificação no aplicativo móvel

### O que é a autenticação sem senha?
- Recursos como a MFA são ótimas maneiras de proteger sua organização, mas os usuários geralmente ficam frustrados ao precisar memorizar senhas com a camada de segurança adicional
- A autenticação sem senha precisa ser configurada em um dispositivo para poder funcionar. Por exemplo, seu computador é algo que você tem
- O Azure e Azure Governamental da Microsoft global oferece estas três opções de autenticação sem senha que se integram ao Azure Active Directory (Azure AD):
    - Windows Hello para Empresas
        - Credenciais biométricas e de PIN estão diretamente ligadas ao computador do usuário, o que impede o acesso de quem não seja o proprietário
    - Aplicativo Microsoft Authenticator
        - O aplicativo Authenticator transforma qualquer telefone iOS ou Android em uma credencial forte e sem senha.
    - Chaves de segurança FIDO2
        - A FIDO (Fast Identity online) Alliance ajuda a promover padrões de autenticação aberta e a reduzir o uso de senhas como forma de autenticação.


### Descrever as identidades externas do Azure 
- Uma identidade externa é uma pessoa, um dispositivo, um serviço etc. que está fora da sua organização.
- todas as maneiras pelas quais você pode interagir com usuários fora da organização com segurança.
- As identidades externas podem soar semelhantes ao logon único
- As seguintes funcionalidades compõem identidades externas:
    - Colaboração B2B (Business to business) 
    - Conexão direta B2B
    - Azure AD B2C (business to customer) 

### Descrever o acesso condicional do Azure
- O Acesso Condicional é uma ferramenta que o Azure Active Directory usa para permitir (ou negar) o acesso a recursos com base em sinais de identidade
- Esses sinais incluem quem é o usuário, onde ele está e de qual dispositivo está solicitando acesso.
- O acesso condicional ajuda os administradores de TI a:
    - Capacitar os usuários a serem produtivos em qualquer lugar e sempre.
    - Proteger os ativos da organização.
- O Acesso Condicional também proporciona uma experiência de autenticação multifator mais granular para os usuários

#### Quando posso usar o acesso condicional?
- Exija a MFA (autenticação multifator) para acessar um aplicativo,
- Exigir acesso a serviços somente por meio de aplicativos cliente aprovados
- Exigir que os usuários acessem seu aplicativo somente de dispositivos gerenciados.
- Bloquear o acesso de fontes não confiáveis

### Descrever o controle de acesso baseado em função do Azure
- Quando você tem várias equipes de TI e engenharia, como é possível controlar o acesso que eles têm aos recursos no seu ambiente de nuvem?
- O princípio de privilégios mínimos diz que você só deve conceder acesso até o nível necessário para concluir uma tarefa
- O Azure fornece funções internas que descrevem regras de acesso comuns para os recursos de nuvem. 
-  Cada função tem um conjunto associado de permissões de acesso relacionadas a essa função

### Como o controle de acesso baseado em função é aplicado aos recursos?
- O controle de acesso baseado em função é aplicado a um escopo, que é um recurso ou um conjunto de recursos ao qual esse acesso se aplica.
- relação entre funções e escopos, escopos incluem::
    - Um grupo de gerenciamento (uma coleção de várias assinaturas).
    - Uma assinatura única.
    - Um grupo de recursos.
    - Um recurso individual.
- O RBAC do Azure é hierárquico, porque quando você permite acesso a um escopo pai, essas permissões são herdadas por todos os escopos filho. Por exemplo:
    - Quando você atribui a função Proprietário a um usuário no escopo do grupo de gerenciamento
    - Quando você atribui a função Leitor a um grupo no escopo da assinatura

### Como o RBAC do Azure é imposto?
- O RBAC do Azure é imposto em qualquer ação iniciada em um recurso do Azure que passa pelo Azure Resource Manager
- Normalmente, você acessa o Resource Manager no portal do Azure, no Azure Cloud Shell, no Azure PowerShell e na CLI do Azure
- O RBAC do Azure usa um modelo de permissão. Quando você recebe uma função, o RBAC do Azure permite que você execute ações dentro do escopo dessa função

### Descrever o modelo de Confiança Zero
- A Confiança Zero é um modelo de segurança que pressupõe o pior cenário e protege os recursos com essa expectativa. 
- Confiança Zero pressupõe uma violação desde o início e verifica cada solicitação como se ela tivesse sido originada em uma rede não controlada.
- Baseia nestes princípios orientadores:
    - Verificar de modo explícito – sempre autentique e autorize com base em todos os pontos de dados disponíveis.
    - Usar o acesso com o mínimo de privilégios – limite o acesso do usuário com JIT/JEA
    - Pressupor a violação – minimize o raio de alcance e segmente o acesso.

### Ajustando-se à Confiança Zero
- Tradicionalmente, as redes corporativas eram restritas, protegidas e, em geral, supostamente seguras
- Em vez de supor que um dispositivo é seguro porque está dentro da rede corporativa, ele requer que todos se autentiquem. 