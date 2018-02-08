---

copyright:

  years: 2015, 2018

lastupdated: "2018-01-10"

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

Você define a severidade do problema com base em suas necessidades de negócios e seu nível de suporte. Todos os chamados são investigados para identificar e resolver a causa raiz do problema. Quando os dados diagnósticos do problema forem necessários para determinar a causa raiz do problema, será solicitada a sua aprovação para acessar arquivos de log e outros dados de determinação de problema outros de seu aplicativo. Sem esses dados, a resolução de seu problema pode ser atrasada.

Se for solicitado que você forneça informações de diagnóstico, use as instruções a seguir para reunir e fornecer as informações solicitadas o mais rápido possível.

## Coletando informações sobre diagnóstico
{: #collecting-diagnostic-information}

Para diagnosticar e resolver problemas com aplicativos e serviços {{site.data.keyword.Bluemix_notm}}, a equipe de Suporte {{site.data.keyword.Bluemix_notm}} pode solicitar que você colete informações de diagnóstico.

Antes de coletar informações de diagnóstico, conclua as etapas a seguir:

1. Assegure-se de que tenha instalado a interface da linha de comandos cf mais recente. Para obter mais informações, veja [Instalando a interface da linha de comandos cf](/docs/starters/install_cli.html).
>**Nota:** Se você não tiver a interface de linha de comandos cf mais recente instalada, após a linha de comandos cf ser conectada ao {{site.data.keyword.Bluemix_notm}}, o comando `cf logs` pode não retornar saída.
2. Assegure-se de que esteja conectado à interface da linha de comandos cf para onde o {{site.data.keyword.Bluemix_notm}} será executado usando o comando `cf api`.

Use um dos scripts a seguir para coletar informações de diagnóstico:

  * Para sistemas operacionais Windows, faça download do arquivo [bmdiag-general.bat ![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo")](http://bluemix-mustgather.mybluemix.net/mustgather/general/bmdiag-general.bat){: new_window} e execute-o.
  * Para sistemas operacionais Linux e Mac, faça download do arquivo [bmdiag-general.sh ![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo")](http://bluemix-mustgather.mybluemix.net/mustgather/general/bmdiag-general.sh){: new_window} e execute-o.

Os scripts usam a interface de linha de comandos cf para extrair as informações a seguir do ambiente de aplicativo:
  * Logs do aplicativo
  * Metadados do aplicativo
  * Rotas configuradas
  * Eventos
  * Serviços provisionados

## Posso escalar um chamado de suporte?
{: #escalation}

Com o suporte premium ou padrão, se você não tiver recebido uma resposta no prazo para um chamado de suporte ou se sentir que um chamado de suporte não está sendo tratado de forma apropriada, será possível escalar o chamado de suporte.  
{:shortdesc}

Consulte [Tipos de suporte](/docs/get-support/getstarttssup.html#typesofsupport) para obter informações adicionais sobre suporte premium e padrão.

Por meio do processo de encaminhamento do chamado de suporte, a gerência da IBM revisa suas preocupações e trabalha com você para melhorar a experiência de suporte.

Para enviar uma solicitação de escalada, execute as etapas a seguir:
  1. Abra um novo chamado de suporte com o resumo **Solicitação de escalada**.
  2. Para assegurar que sua solicitação de escalada possa ser correspondida ao chamado de suporte original, inclua as informações a seguir no corpo do chamado:
      * O número do chamado de suporte aberto que precisa ser escalado.
      * Um breve resumo das razões para a necessidade da escalada.

## Horas de operação
{: #support-hours-operation}

Os problemas de severidade 1 são monitorados 24 horas por dia, 7 dias por semana. Os envios de formulário para problemas com todos os outros níveis de severidade são monitorados de domingo às 21h30 UTC a sexta-feira às 23h59 UTC (excluindo feriados).

Para obter assistência na conversão dessas horas de suporte para o seu fuso horário local, veja [Timeanddate.com ![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo")](https://www.timeanddate.com). Para obter mais informações sobre o planejamento de feriado, veja [Feriados de suporte do {{site.data.keyword.Bluemix_notm}} ![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo")](http://ibm.biz/bluemixholidays).
