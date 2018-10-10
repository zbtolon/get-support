---

copyright:

  years: 2015, 2018

lastupdated: "2018-10-02"

---


{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}


# Como obter uma resposta rápida para o meu chamado?
{: #quicktickresp}

Ao entrar em contato com o suporte e abrir um chamado de suporte, é possível solicitar um nível de severidade específico, dependendo do tipo e da urgência do problema. O nível de severidade pode afetar a rapidez com que seu problema é tratado.
{:shortdesc}

Você define a severidade do problema com base em suas necessidades de negócios e seu nível de suporte. Para obter mais informações sobre os níveis de planos de suporte, veja [Planos de suporte](/docs/get-support/index.html). Todos os chamados são investigados para identificar e resolver a causa raiz do problema. Quando a equipe de suporte precisa de dados diagnósticos do problema para determinar a causa raiz, é solicitada sua aprovação para acessar arquivos de log e outros dados de determinação de problema por meio de seu aplicativo. Sem esses dados, a resolução de seu problema pode ser atrasada.

## Coletando informações sobre diagnóstico
{: #collecting-diagnostic-information}

Para diagnosticar e resolver problemas com aplicativos e serviços do {{site.data.keyword.Bluemix_notm}}, a equipe de suporte do {{site.data.keyword.Bluemix_notm}} pode solicitar informações de diagnóstico. Use as instruções a seguir para reunir e fornecer as informações solicitadas o mais rápido possível.

Antes de coletar informações de diagnóstico, conclua as etapas a seguir:

1. Assegure-se de que tenha a versão mais atual da interface da linha de comandos do Cloud Foundry instalada. Para obter mais informações, veja [Instalando a interface da linha de comandos do Cloud Foundry](/docs/starters/install_cli.html).
>**Nota:** se você não tiver a versão mais atual, depois que a linha de comandos do Cloud Foundry for conectada ao {{site.data.keyword.Bluemix_notm}}, o comando `cf logs` poderá não retornar saída.
2. Assegure-se de que tenha conectado a interface da linha de comandos do Cloud Foundry na qual o {{site.data.keyword.Bluemix_notm}} está em execução usando o comando `cf api`.

Use um dos scripts a seguir para coletar informações de diagnóstico:

  * Para sistemas operacionais Windows, faça download do arquivo [bmdiag-general.bat ![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo")](http://bluemix-mustgather.mybluemix.net/mustgather/general/bmdiag-general.bat){: new_window} e execute-o.
  * Para sistemas operacionais Linux e Mac, faça download do arquivo [bmdiag-general.sh ![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo")](http://bluemix-mustgather.mybluemix.net/mustgather/general/bmdiag-general.sh){: new_window} e execute-o.

Os scripts usam a interface da linha de comandos do Cloud Foundry para extrair as informações a seguir do ambiente de aplicativos:
  * Logs do aplicativo
  * Metadados do aplicativo
  * Rotas configuradas
  * Eventos
  * Serviços provisionados

## Escalando casos de suporte
{: #escalation}

Use o processo de escalada para problemas críticos de superfície ou se você sentir que o seu caso de suporte não está sendo tratado adequadamente. Quando um caso é escalado, o gerente de plantão revisa as informações no caso de suporte, envolve os membros apropriados da equipe técnica de suporte do {{site.data.keyword.Bluemix_notm}} e fornece a você as atualizações apropriadas.

É possível solicitar assistência adicional, escalando o seu caso para o Support Manager do {site.data.keyword.Bluemix_notm}} de plantão como um cliente com qualquer assinatura paga. 

Para escalar um caso de suporte, deve-se ter um caso de suporte aberto para o problema. Além disso, assegure-se de fornecer uma descrição detalhada do problema técnico no caso de suporte que você abriu.

 Para escalar um caso, conclua as etapas a seguir:

  1. Entre em contato com a Equipe de suporte do {{site.data.keyword.Bluemix_notm}} por telefone ou bate-papo:
    * Por telefone para o seguinte número: 866-403-7638.
    * Por bate-papo no [Centro de suporte![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo")](https://console.bluemix.net/unifiedsupport/supportcenter){: new_window} do {{site.data.keyword.Bluemix_notm}} ou pelo [portal do cliente ![Ícone de link externo](../icons/launch-glyph.svg)](https://control.softlayer.com/){:new_window} se você tiver uma conta da SoftLayer que não esteja vinculada.
  2. Forneça seu número de caso existente e solicite para escalar o caso.
  3. Forneça a justificação para escalação e o impacto no negócio de seu caso.

Os {{site.data.keyword.Bluemix_notm}} Support Managers estão de plantão e disponíveis 24 horas por dia, todos os dias da semana. Os gerenciadores de plantão envolvem os recursos apropriados para cuidar de seu caso e, em seguida, informam sobre as ações tomadas.
