---

copyright:

  years: 2015, 2018

lastupdated: "2018-05-14"

---


{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}


# Como obter uma resposta rápida para o meu caso?
{: #quicktickresp}

Ao entrar em contato com o suporte e abrir um caso de suporte, é possível solicitar um nível de severidade específico, dependendo do tipo e da urgência do problema. O nível de severidade pode afetar a rapidez com que seu problema é tratado.
{:shortdesc}

Você define a severidade do problema com base em suas necessidades de negócios e seu nível de suporte. Veja [Planos de suporte](/docs/get-support/index.html) para obter mais informações sobre os níveis de planos de suporte. Todos os casos são investigados para identificar e resolver a causa raiz do problema. Quando dados diagnósticos do problema forem necessários para determinar a causa raiz do problema, será solicitado que você obtenha aprovação para acessar arquivos de log e outros dados de determinação de problema de seu aplicativo. Sem esses dados, a resolução de seu problema pode ser atrasada.

## Coletando informações sobre diagnóstico
{: #collecting-diagnostic-information}

Para diagnosticar e resolver problemas com aplicativos e serviços {{site.data.keyword.Bluemix_notm}}, a equipe de Suporte {{site.data.keyword.Bluemix_notm}} pode solicitar que você colete informações de diagnóstico. Use as instruções a seguir para reunir e fornecer as informações solicitadas o mais rápido possível.

Antes de coletar informações de diagnóstico, conclua as etapas a seguir:

1. Assegure-se de ter instalado a interface da linha de comandos mais recente do Cloud Foundry. Para obter mais informações, veja [Instalando a interface da linha de comandos do Cloud Foundry](/docs/starters/install_cli.html).
>**Nota:** se você não tiver a interface de linha de comandos mais recente do Cloud Foundry instalada, após a linha de comandos cf ser conectada ao {{site.data.keyword.Bluemix_notm}}, o comando `cf logs` poderá não retornar a saída.
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

Como um cliente {{site.data.keyword.Bluemix_notm}}, é possível solicitar assistência adicional escalando seu caso para o {{site.data.keyword.Bluemix_notm}} Support Manager de plantão. O processo de escalação permite emergir problemas críticos e também expressar sua preocupação caso você sinta que seu caso de suporte não está sendo tratado de forma apropriada. Depois que um caso é escalado, o gerente em serviço revisa as informações no caso de suporte, envolve os membros apropriados da equipe técnica de suporte do {{site.data.keyword.Bluemix_notm}} e fornece a você as atualizações apropriadas.

Para escalar um caso de suporte, deve-se ter o suporte avançado ou premium do {{site.data.keyword.Bluemix_notm}} e ter aberto um caso de suporte para o problema. Além disso, assegure que o problema técnico seja bem documentado no caso de suporte que você abriu.

 Para escalar um caso, conclua as etapas a seguir:

  1. Entrar em contato com a Equipe de suporte do {{site.data.keyword.Bluemix_notm}} por telefone ou bate-papo :
    * Por telefone para o seguinte número: 866-403-7638.
    * Por bate-papo, por meio do [Centro de suporte ![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo")](https://console.bluemix.net/unifiedsupport/supportcenter){: new_window} do {{site.data.keyword.Bluemix_notm}} ou, se você tiver uma conta do SoftLayer que não esteja vinculada, por meio do [portal do cliente ![Ícone de link externo](../icons/launch-glyph.svg)](https://control.softlayer.com/){:new_window}.
  2. Forneça seu número de caso existente e solicite para escalar o caso.
  3. Forneça a justificação para escalação e o impacto no negócio de seu caso.

Os {{site.data.keyword.Bluemix_notm}} Support Managers estão de plantão e disponíveis 24 horas por dia, todos os dias da semana. Os gerenciadores de plantão envolvem os recursos apropriados para cuidar de seu caso e, em seguida, informam sobre as ações tomadas.
