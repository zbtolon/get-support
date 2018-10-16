---

copyright:

  years: 2015, 2018

lastupdated: "2018-10-04"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}

# Visualizando o status e as notificações do sistema
{: #viewing-bluemix-status}

A página Status é o local central para localizar notificações e anúncios sobre os eventos chave que estão afetando a plataforma {{site.data.keyword.Bluemix_notm}} e os serviços principais.
{:shortdesc}

Na página Status, é possível localizar as informações a seguir:

  * O status atual de serviços e componentes em todas as regiões do {{site.data.keyword.Bluemix_notm}} Foundry Service.
  * Uma lista de anúncios, em ordem cronológica, para manutenção e incidentes. É possível filtrar a lista ou abrir um anúncio individual para obter detalhes adicionais.
  * Janelas de manutenção planejada para as quais aviso prévio é fornecido, exceto em circunstâncias extremas.
  * Incidentes ou indisponibilidades não planejados, que são postados assim que a equipe do {{site.data.keyword.Bluemix_notm}} toma conhecimento deles. As notificações do incidente são atualizadas regularmente até que sejam resolvidas.
  * Referências a boletins de segurança afetam os vários serviços do {{site.data.keyword.Bluemix_notm}} ou a plataforma.
  * Outros anúncios de toda a plataforma de interesse geral para você.
  * [Um feed RSS o qual é possível assinar](#subscribing-rss-feed).

É possível localizar a página Status, escolhendo uma das opções a seguir:

  * Efetue login no console do {{site.data.keyword.Bluemix_notm}}. Na barra de menus, clique em **Suporte** e selecione **Status**. Verifique os recursos listados para o ícone ![alguns problemas](images/some_issues.svg). Esse ícone pode indicar uma indisponibilidade.
  * Acesse-o diretamente em [{{site.data.keyword.Bluemix_notm}} - Status ![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo")](https://console.bluemix.net/status){: new_window}.


## Melhores práticas para monitorar o status
{: #best-practices}

Use as melhores práticas a seguir para monitorar o status de {{site.data.keyword.Bluemix_notm}} para manter-se informado e planejar adequadamente.

### Verifique as próximas janelas de manutenção
{: #monbp-checmaintwin}

Verifique as próximas janelas de manutenção postadas na página Status, pelo menos uma vez a cada 24 horas, usando uma das opções a seguir:
* Navegando diretamente para a página [Status ![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo")](https://console.bluemix.net/status){: new_window}
* Usando o feed RSS ou um encaminhador de RSS para e-mail

### Verifique as janelas atualmente em manutenção ou um incidente em andamento
{: #monbp-checcurmaninprog}

Se você suspeitar que o {{site.data.keyword.Bluemix_notm}} não está funcionando conforme o esperado, verifique a página Status para janelas de manutenção atual ou um incidente em andamento. Para relatar um incidente que ainda não está listado na página Status, abra um chamado de suporte clicando em **Suporte** e selecionando **Incluir chamado** na barra de menus ou acessando a página de ajuda do [Suporte do {{site.data.keyword.Bluemix_notm}} ![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo")](http://www.ibm.biz/bluemixsupport){: new_window}.

### Aproveite várias regiões do {{site.data.keyword.Bluemix_notm}} Foundry Service
{: #monbp-multpreg}

Todos os usuários do {{site.data.keyword.Bluemix_notm}} Public têm acesso automaticamente às regiões Sul dos EUA, Reino Unido, Alemanha, Sydney, Leste dos EUA e Norte da Ásia-Pacífico. A equipe de Operações Globais do {{site.data.keyword.Bluemix_notm}} gerencia todas as regiões para evitar impactos de manutenção e minimizar o risco de incidentes que afetem todas as regiões ao mesmo tempo.

Para alternar regiões, na barra de menus do {{site.data.keyword.Bluemix_notm}}, expanda o menu de região e, em seguida, selecione outra região.

### Prepare-se para interrupções menores
{: #monbp-prepmininter}

Na maioria dos casos, o {{site.data.keyword.Bluemix_notm}} pode continuar sendo usado normalmente, mesmo durante a janela de manutenção. No entanto, as interrupções menores de um serviço nem sempre podem ser evitadas. Os aplicativos em execução geralmente permanecem disponíveis mesmo se as funções de gerenciamento do aplicativo do {{site.data.keyword.Bluemix_notm}}, como apps de início e de parada, estiverem temporariamente interrompidas. Para maximizar a disponibilidade de seus aplicativos em execução, execute pelo menos três instâncias de cada aplicativo.

## Assinando um feed RSS
{: #subscribing-rss-feed}

Receba alertas de quaisquer notificações assinando o feed RSS da página Status do {{site.data.keyword.Bluemix_notm}}. Essa abordagem fornece uma maneira de obter atualizações sem precisar consultar regularmente a página Status.

Para assinar, siga estas etapas:

1. Faça download e instale um leitor RSS.
2. Use seu leitor para assinar o feed por um dos métodos a seguir:
    * Arraste o ícone RSS ![RSS](images/rss.svg) para seu leitor RSS.
    * Clique com o botão direito no ícone RSS, selecione **Copiar endereço de link** e cole a URL em seu leitor RSS.

Para obter mais informações, veja a seção de **Ajuda** de seu leitor. 	   

Outros métodos de leitura de feeds RSS estão disponíveis por meio de plug-ins do navegador da web, tais como:
  * [Feed RSS ![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo")](http://feeder.co/){: new_window} Reader for Chrome
  * [Brief ![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo")](https://addons.mozilla.org/en-US/firefox/addon/brief/){: new_window} add-on for Firefox

Novas fontes, como os sites a seguir, também fornecem métodos para ler feeds RSS:
  * [Feedly ![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo")](http://www.feedly.com/){: new_window}
  * [G2reader ![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo")](http://www.g2reader.com/en/){: new_window}

Também é possível usar um serviço de terceiro para enviar automaticamente um e-mail para cada atualização de RSS. A lista a seguir fornece alguns serviços de terceiros de exemplo:

  * www.feedmyinbox.com
  * www.rssforward.com
  * www.feedrabbit.com
  * www.mailchimp.com
  * www.feedmailer.com
  * www.iftt.com

O {{site.data.keyword.Bluemix_notm}} geralmente tem cerca de 50 atualizações por mês.


## Configurando notificações de incidentes e manutenção
{: #setting-up-notifications}

Para {{site.data.keyword.Bluemix_notm}} Public, é possível se inscrever para notificações da plataforma, que são alertas de e-mail opcionais para eventos de incidente e manutenção na plataforma. Para configurar as notificações, clique em **Gerenciar** > **Conta** > **Notificações** e selecione a guia **Plataforma**. 
