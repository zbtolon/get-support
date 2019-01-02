---

copyright:

  years: 2018

lastupdated: "2018-11-28"

---


{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:important: .important}
{:new_window: target="_blank"}

# Designando acesso de usuário para trabalhar com casos de suporte
{: #access}

Por padrão, os usuários em sua conta não têm acesso para criar, atualizar, procurar ou visualizar casos. Como o proprietário da conta, deve-se fornecer acesso aos usuários designando uma política de acesso do Identity and Access Management (IAM). Use o serviço de gerenciamento de conta do Centro de suporte para designar aos usuários acesso para trabalhar com casos de suporte.
{:shortdesc}

As políticas de acesso do Centro de suporte fornecem aos usuários acesso para trabalhar com casos de suporte. No entanto, essas políticas de acesso não fornecem acesso para que os usuários visualizem outros usuários na conta. Portanto, se um proprietário da conta tiver definido a [**Configuração de visibilidade da lista de usuários**](/docs/iam/userlist.html#userlistview) como **Visualização restrita**, os usuários que tiverem acesso para gerenciar casos poderão não estar aptos a acessarem os casos designados a outros usuários ou ao proprietário da conta. Para assegurar que os usuários possam visualizar todos os casos, deve-se fornecer acesso adicional também designando uma política de acesso do IAM ao serviço de gerenciamento de conta de gerenciamento de usuário com a função Visualizador designada. 

Para fornecer aos usuários específicos acesso total a certos casos na conta, em vez de acesso a todos os casos usando uma política de acesso do IAM, inclua-os no caso inserindo seus e-mails ao criar o caso. Ao incluir usuários em um caso que você cria, eles têm acesso para visualizar, editar e atualizar somente esse caso na conta. Eles também recebem notificações quando há atualizações para o caso.

Para usuários de infraestrutura clássica que usavam permissões de infraestrutura clássica anteriormente para designar acesso ao caso de suporte, essas permissões agora estão disponíveis em [grupos de acesso de permissão de infraestrutura clássica migrados](/docs/iam/infrastructureaccess.html#predefined). Os grupos de acesso de permissão migrados incluem a política do IAM no serviço de Gerenciamento de usuário com a função Visualizador designada.

Para designar a um usuário uma política de acesso do IAM em um serviço de gerenciamento de conta, como o serviço do Centro de suporte ou o serviço de Gerenciamento de usuário, conclua as etapas a seguir:

1. Na barra de menus, clique em **Gerenciar** &gt; **Acessar (IAM)** e, em seguida, selecione **Usuários**.
2. Selecione um usuário da lista.
3. Clique em **Políticas de acesso**.
4. Clique em **Designar acesso**.
5. Selecione **Designar acesso aos serviços de gerenciamento de conta**.
6. Selecione um serviço na lista. 
5. Selecione uma função para designar o acesso desejado.

Verifique a tabela a seguir para entender exatamente quais permissões estão incluídas em cada função.

| Função | Ações | 
|--------|---------------|
|Visualizador  | Visualizar e procurar casos |
|Administrador | Visualizar, procurar, criar e atualizar casos|
{: caption="Tabela 1. Funções e ações para o serviço do Centro de suporte" caption-side="top"}

