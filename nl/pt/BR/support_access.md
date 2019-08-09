---

copyright:

  years: 2018,2019

lastupdated: "2019-07-25"

keywords: access to cases, get access for cases, assign cases, watchlist

subcollection: get-support

---


{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:important: .important}
{:new_window: target="_blank"}

# Designando acesso de usuário para trabalhar com casos de suporte
{: #access}

Por padrão, os usuários em sua conta não têm acesso para criar, atualizar, procurar ou visualizar casos. Como o proprietário da conta, deve-se fornecer acesso aos usuários designando uma política de acesso do Identity and Access Management (IAM). Use o serviço de gerenciamento de conta do Centro de suporte para designar aos usuários acesso para trabalhar com casos de suporte. 
{:shortdesc}

Ao criar um caso, é possível fornecer a outros usuários acesso total a esse caso incluindo seu e-mail no campo **Incluir outra pessoa nesse caso**. Todos os usuários incluídos têm acesso para visualizar, editar e atualizar somente esse caso na conta. Eles também recebem notificações quando o caso é atualizado.
{: tip}

Ao dar acesso a um usuário designando uma função no serviço do Centro de suporte, você permite que os usuários visualizem, editem ou criem casos de suporte. Eles podem não ser capazes de visualizar todos os casos em uma conta. Se o proprietário da conta definir a configuração de visibilidade da lista de usuários como restrita, os usuários verão apenas os casos que eles mesmos criarem. Para assegurar que um usuário possa sempre visualizar ou editar todos os casos na conta, deve-se designar uma segunda política de acesso com a função de visualizador no serviço de gerenciamento de usuários. 

Para usuários da infraestrutura clássica, as permissões para designar acesso ao caso de suporte agora estão disponíveis em [grupos de acesso de permissão de infraestrutura clássica migrados](/docs/iam?topic=iam-infrapermission#predefined). Os grupos de acesso de permissão migrados incluem a política do IAM no serviço de gerenciamento de usuários com a função de visualizador designada.
{: note}

## Criando um grupo de acesso para trabalhar com casos
{: #creating-access-group}

Para aperfeiçoar o processo de designação de acesso, é possível aproveitar a designação de uma política para usuários por meio de grupos de acesso. Conclua as etapas a seguir para criar um grupo de acesso com acesso ao serviço do centro de suporte:

1. Na barra de menus, acesse **Gerenciar** &gt; **Acesso (IAM)**, selecione **Grupos de acesso** e clique em **Criar**. 
2. Insira um nome e uma descrição do grupo de acesso e clique em **Criar**. 
3. Clique em **Políticas de acesso** > **Designar acesso**.
4. Selecione **Designar acesso aos serviços de gerenciamento de conta**.
5. Selecione **Centro de suporte**.
6. Selecione a função Visualizador, Editor ou Administrador dependendo do tipo de acesso que você deseja que esse grupo tenha e clique em **Designar**. A tabela a seguir lista as ações que estão incluídas em cada função para trabalhar com casos.

| Função | Ações | 
|--------|---------------|
|Visualizador  | Visualizar e procurar casos |
|Editor | Visualizar, procurar, criar e atualizar casos|
|Administrador | Visualizar, procurar, criar e atualizar casos; gerenciar funções do centro de suporte para outros usuários|
{: caption="Tabela 1. Funções e ações para o serviço do Centro de suporte" caption-side="top"}

Por padrão, os usuários com uma função de serviço do Centro de suporte podem acessar somente os casos de suporte aos quais eles são designados, a menos que uma das condições a seguir seja atendida:

* A visibilidade da lista de usuários é configurada para a visualização Irrestrita pelo proprietário da conta.
* O usuário é designado com uma função de serviço de gerenciamento de conta de gerenciamento de usuários.


Se você deseja assegurar que os seus usuários podem visualizar todos os casos de suporte na conta, também é possível incluir uma política com a função de visualizador para o serviço de Gerenciamento de usuários para o seu grupo de acesso:

1. Clique em **Políticas de acesso** > **Designar acesso**.
2. Selecione **Designar acesso aos serviços de gerenciamento de conta**.
3. Selecione **Gerenciamento de usuários**.
4. Selecione **Visualizador** e clique em **Designar**.


## Incluindo usuários em seu grupo de acesso de gerenciamento de caso
{: #add-user-access-group} 

Após você criar o grupo de acesso, conclua as etapas a seguir para incluir usuários:

1. Na guia **Usuários** para seu grupo de acesso, clique em **Incluir usuários**.
2. Selecione o usuário que você deseja incluir e clique em **Incluir no grupo**.

## Concedendo acesso de usuários individuais aos casos 

O uso de grupos de acesso para designar os serviços de centro de suporte e de gerenciamento de usuários é a maneira mais eficiente para você designar acesso, mas também é possível designar as mesmas permissões a usuários individuais. 

1. Clique em **Gerenciar** &gt; **Acesso (IAM)** e, em seguida, selecione **Usuários**. 
2. Clique em **Políticas de acesso** > **Designar acesso**.
3. Selecione **Designar acesso aos serviços de gerenciamento de conta**.
4. Selecione **Centro de suporte**.
5. Selecione a função **Visualizador**, **Editor** ou **Administrador** dependendo do tipo de acesso que deseja que esse grupo tenha e clique em **Designar**.
6. Se você deseja que um usuário seja capaz de visualizar todos os outros usuários na conta, também é possível designar a ele a função de visualizador de gerenciamento de usuários. 
