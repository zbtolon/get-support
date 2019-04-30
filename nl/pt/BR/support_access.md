---

copyright:

  years: 2018,2019

lastupdated: "2019-04-18"

keywords: access to cases, get access for cases, assign cases

subcollection: get-support

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

Ao criar um caso, é possível fornecer a outros usuários acesso total a esse caso incluindo seu e-mail no campo **Incluir outra pessoa nesse caso**. Todos os usuários incluídos têm acesso para visualizar, editar e atualizar somente esse caso na conta. Eles também recebem notificações quando o caso é atualizado.
{: tip}

Para usuários da infraestrutura clássica, as permissões para designar acesso ao caso de suporte agora estão disponíveis em [grupos de acesso de permissão de infraestrutura clássica migrados](/docs/iam?topic=iam-infrapermission#predefined). Os grupos de acesso de permissão migrados incluem a política do IAM no serviço de gerenciamento de usuários com a função de visualizador designada.

## Criando um grupo de acesso para trabalhar com casos
{: #creating-access-group}

Para aperfeiçoar o processo de designação de acesso, é possível aproveitar a designação de uma política para usuários por meio de grupos de acesso. Conclua as etapas a seguir para criar um grupo de acesso com acesso ao serviço do centro de suporte:

1. Na barra de menus, acesse **Gerenciar** &gt; **Acesso (IAM)**, selecione **Grupos de acesso** e clique em **Criar**. 
2. Insira um nome e uma descrição do grupo de acesso e clique em **Criar**. 
3. Clique em **Políticas de acesso** > **Designar acesso**.
4. Selecione **Designar acesso aos serviços de gerenciamento de conta**.
5. Selecione **Centro de suporte**.
6. Selecione a função **Visualizador**, **Editor** ou **Administrador**, dependendo do tipo de acesso que você deseja que esse grupo tenha e clique em **Designar**.

Se você deseja que seus usuários sejam capazes de visualizar todos os outros usuários na conta, também é possível incluir a função de visualizador de gerenciamento de usuários em seu grupo de acesso:

1. Clique em **Políticas de acesso** > **Designar acesso**.
2. Selecione **Designar acesso aos serviços de gerenciamento de conta**.
3. Selecione **Gerenciamento de usuários**.
4. Selecione **Visualizador** e clique em **Designar**.

A tabela a seguir lista as permissões que estão incluídas em cada função para trabalhar com casos.

| Função | Ações | 
|--------|---------------|
|Visualizador  | Visualizar e procurar casos |
|Aplicativos | Visualizar, procurar, criar e atualizar casos|
|Administrador | Visualizar, procurar, criar e atualizar casos; gerenciar funções do centro de suporte para outros usuários|
{: caption="Tabela 1. Funções e ações para o serviço do Centro de suporte" caption-side="top"}

## Incluindo usuários em seu grupo de acesso de gerenciamento de caso
{: #add-user-access-group} 

Agora que o grupo de acesso foi criado, inclua usuários:

1. Na guia **Usuários** para seu grupo de acesso, clique em **Incluir usuários**.
2. Selecione o usuário que você deseja incluir no grupo e clique em **Incluir no grupo**.

## Concedendo acesso de usuários individuais aos casos 

O uso de grupos de acesso para designar os serviços de centro de suporte e de gerenciamento de usuários é a maneira mais eficiente para você designar acesso, mas também é possível designar as mesmas permissões a usuários individuais. 

1. Clique em **Gerenciar** &gt; **Acesso (IAM)** e, em seguida, selecione **Usuários**. 
2. Clique em **Políticas de acesso** > **Designar acesso**.
3. Selecione **Designar acesso aos serviços de gerenciamento de conta**.
4. Selecione **Centro de suporte**.
5. Selecione a função **Visualizador**, **Editor** ou **Administrador**, dependendo do tipo de acesso que você deseja que esse grupo tenha e clique em **Designar**.
6. Se você deseja que um usuário seja capaz de visualizar todos os outros usuários na conta, também é possível designar a ele a função de visualizador de gerenciamento de usuários. 
