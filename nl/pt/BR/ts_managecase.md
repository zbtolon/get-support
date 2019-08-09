---

copyright:

  years: 2015, 2019

lastupdated: "2019-07-25"

keywords: help managing cases, resolve issues managing cases, trouble working with cases

subcollection: get-support

---


{:tsSymptoms: .tsSymptoms}
{:tsCauses: .tsCauses}
{:tsResolve: .tsResolve}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}


# Resolução de problemas para gerenciar casos de suporte
{: #Supportcases}

É possível encontrar problemas com a criação e o gerenciamento de casos de suporte do {{site.data.keyword.Bluemix}}. Em muitos casos, é possível recuperar-se desses problemas seguindo algumas etapas simples.
{:shortdesc}

## Por que não posso criar ou editar casos de suporte? 
{: #ts_service_broker}

Não é possível criar ou editar um caso de suporte do {{site.data.keyword.Bluemix_notm}} e você recebe uma mensagem de erro de que não tem o acesso apropriado. 
{:shortdesc}

Quando você tenta criar um caso, a mensagem de erro a seguir é exibida:   
{: tsSymptoms}

`Parece que você não tem acesso para criar casos para essa conta.`

Problemas gerais com o acesso e o gerenciamento de casos de suporte podem ser causados por
não ter a política de acesso do Identity and Access Management (IAM) para o serviço de gerenciamento de conta do Centro de suporte. A função de editor ou administrador no serviço de gerenciamento de conta do centro de suporte deve ser designada a você para criar casos. 
{: tsCauses}

Para resolver o problema, o proprietário da conta, um administrador no serviço do centro de suporte ou o administrador em todos os serviços de gerenciamento de conta pode designar uma política do IAM no centro de suporte para gerenciar casos. 
{: tsResolve}

Se você for o proprietário da conta ou um administrador do Centro de suporte, conclua as etapas a seguir para criar uma política de acesso para trabalhar com casos de suporte:

1. Acesse **Gerenciar** &gt; **Acessar (IAM)** e selecione **Usuários**.
2. Selecione um nome de usuário e clique em **Políticas de acesso**. 
3. Clique em **Designar acesso**. 
4. Selecione **Designar acesso aos serviços de gerenciamento de conta**. 
5. No menu **Serviço**, selecione **Centro de suporte**. 
6. Selecione uma função para definir o nível de acesso do usuário. 


## Por que não posso visualizar todos os casos na conta?
{: #ts_viewcasedetails}

Não é possível visualizar todos os casos na conta porque você não tem acesso para visualizar todos os usuários na conta. 
{:shortdesc}

Quando você tenta visualizar os casos de suporte associados à conta, não é possível ver todos os casos abertos. 
{: tsSymptoms}

O proprietário da conta define a [configuração de visibilidade da lista de usuários](/docs/iam?topic=iam-userlistview#userlistview) como restrita. Quando a configuração está configurada como restrita e você não tem uma política de acesso adicional para visualizar usuários na conta, você não tem o acesso necessário para visualizar todos os casos na conta. É possível visualizar somente os usuários convidados para a conta, compartilhar uma associação de organização do Cloud Foundry ou usuários que estão em sua hierarquia de usuário da infraestrutura clássica. 
{: tsCauses}

Deve-se estar designado a uma política do IAM com pelo menos a função Visualizador no serviço de gerenciamento de conta de Gerenciamento de usuário, além de sua política de acesso ao serviço de gerenciamento de conta do Centro de suporte. Para visualizar seu acesso atual, acesse **Gerenciar** &gt; **Acesso (IAM)** e selecione o seu nome na página **Usuários**. Clique na guia **Políticas de acesso** e revise suas políticas designadas. 
{: tsResolve}

Para resolver o problema, entre em contato com o proprietário da conta para solicitar o acesso apropriado. 

## Por que não consigo localizar um caso que criei anteriormente? 
{: #ts_viewarchivedcase}

Não é possível localizar os casos criados antes da experiência de plataforma aprimorada do {{site.data.keyword.Bluemix_notm}}. 
{:shortdesc}

Depois de acessar a guia **Gerenciar casos** no Centro de suporte, não será possível localizar nenhum caso criado antes de 2 de dezembro de 2018.
{: tsSymptoms}

Os casos abertos antes de 2 de dezembro de 2018 são visíveis apenas em **Visualizar casos arquivados**. 
{: tsCauses}

Para visualizar seus casos, acesse **Suporte**, selecione **Gerenciar casos** e clique em **Visualizar casos arquivados**.
{: tsResolve} 






