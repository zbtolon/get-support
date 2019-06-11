---

copyright:

  years: 1994, 2019

lastupdated: "2019-06-06"

keywords: data centers, data center support, dal01 pod, wdc01 pod 

subcollection: get-support

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}

# Retirada de suporte para alguns data centers dos EUA
{: #dc-migrate}

A IBM está retirando o suporte para os seguintes data centers nos Estados Unidos: 

* Pods 1, 4 e 5 de dal01
{:shortdesc}

##  Por que a mudança para outro data center é necessária?
{: #required-data}

Para continuar a trazer o melhor serviço, hardware e conectividade, todos os sites são continuamente avaliados para assegurar que atendam aos padrões de rede, elétricos e outros padrões de infraestrutura. Mesmo que esses sites sejam adequados, eles não atendem mais aos padrões atuais.

## A migração deve estar totalmente concluída até a data listada?
{: #data-list}

Sim. Para assegurar que você não tenha nenhuma interrupção no serviço, estamos tentando permitir o máximo de tempo de avanço para facilitar a transição. Comunicamos o movimento desse site em maio de 2018.

## Será necessário mudar para outro data center de novo?
{: #move-data}

Avaliamos constantemente a qualidade de nossos sites para proporcionar a você o melhor e mais confiável serviço. É possível que tenhamos outros movimentos à medida que continuamos a avaliar alguns dos sites mais antigos.

## Posso escolher qualquer data center do {{site.data.keyword.Bluemix_notm}} nos Estados Unidos?
{: #us-data}

Sim, é possível escolher qualquer site da IBM dos EUA que atenda às suas necessidades de localização.

## Como seleciono em qual data center implementar?
{: #deploy-data}

A IBM tem mais de 60 data centers em localizações no mundo todo. Visualize o mapa de data center em nossa página de data centers globais para ver em quais deles é possível implementar. 

Os fatores a seguir podem influenciar a sua seleção de data center:
* Proximidade com os usuários dos sistemas
* Proximidade com quaisquer outros sistemas com os quais esse servidor precisa se comunicar
* Quaisquer políticas de dados ou regulamentações que requerem que os dados sejam armazenados em uma localização específica

## Também será necessário usar os sites dos EUA durante o período de transição?
{: #transition}

É possível usar qualquer site do {{site.data.keyword.cloud_notm}} em todo o mundo durante o período de transição, que durará até 60 dias.

## Os dois meses grátis de recursos do período de transição são adicionados ao meu tempo de servidor existente?
{: #free}

Sim. É possível entrar em contato com um representante de suporte apropriado que possa ajudá-lo a passar pelo processo de aquisição de seus servidores de período de transição.

## Como determino minha configuração de hardware atual?
{: #current-hardware}

Efetue login no portal do cliente. Na **Lista de dispositivos**, selecione o servidor no qual está interessado e localize os detalhes de configuração do sistema. A partir daí, é possível visualizar o tipo
de processador, por exemplo, Single Intel Xeon E3-1270 (4 núcleos, 3,50 GHz). Também é possível visualizar a quantidade
de memória (RAM), armazenamento e outros dados.

## Como determino a utilização do meu hardware atual?
{: #utilization} 

A maioria dos sistemas operacionais fornece ferramentas que podem ser usadas para entender a utilização do
sistema, por exemplo, vmstat e iostat no Linux ou o Windows System Performance Monitor. Também existem muitas outras
ferramentas de monitoramento de desempenho que podem ser disponibilizadas para você. O monitoramento e o ajuste de desempenho são algo em que você pode investir tempo e esforço significativos. Em geral, é necessário entender se há recursos específicos dentro do sistema (processador, memória, disco, rede) que são intensamente usados ou não usados. Ter essas informações pode ajudá-lo a dimensionar melhor o novo sistema. Por exemplo, um
sistema no qual a capacidade de memória frequentemente tem comprometimento excessivo, provavelmente se beneficiará de tamanhos de
memória maiores no sistema de destino para o qual você migrar.

## Como comparar os processadores antigos e os novos?
{: #old-new}

Para comparar as especificações de processadores Intel novos e antigos, acesse [https://ark.intel.com/#@Processors](https://ark.intel.com/#@Processors){: new_window} ![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo"). Se você souber o tipo de processador, será possível navegar pelos menus. Como alternativa, é possível usar a opção de
procura para localizar as especificações dos dois processadores. Os processadores mais novos tendem a ter mais núcleos
do processador e geralmente são executados em velocidades de clock mais lentas que as variantes mais antigas. Se você
tiver uma carga de trabalho ligada ao processador (seu desempenho é limitado pela velocidade do processador),
aconselhamos a escolha de um processador com menos núcleos e uma velocidade de clock mais alta.  Se você executar muitas cargas de trabalho não restritas pela velocidade do processador, a escolha de um processador com mais núcleos e uma velocidade de clock semelhante ou mais lenta poderá ser um melhor curso de ação.

## Como escolher o novo sistema operacional?
{: #operating-system}

Se o servidor estiver em uso por muitos anos e não tiver sido mantido atualizado, é provável que você esteja executando uma versão mais antiga do sistema operacional. Isso pode apresentar desafios com a migração. É possível que você não tenha a mídia de instalação do sistema operacional antigo do qual instalar.  Ou é possível que o hardware do servidor mais novo para o qual você está migrando não seja suportado pela versão mais antiga do sistema operacional. Talvez seja necessário escolher um sistema operacional diferente para o qual mover.

A escolha do sistema operacional pode ser prescrita pelos aplicativos que você está executando. Como parte da migração,
talvez seja necessário executar o aplicativo em uma versão mais recente do sistema operacional. Assegure-se de que ele funcione na versão mais recente.

O conhecimento técnico disponível de um sistema operacional específico também podem influenciar a escolha. Se você
tiver o código-fonte para o aplicativo, assegure-se de que as ferramentas de desenvolvimento necessárias e o sistema
operacional de suporte ou as funções de middleware estejam disponíveis na nova plataforma. Em geral, os sistemas do tipo Linux são melhores em suportar aplicativos mais antigos em versões mais recentes do sistema operacional do que o Windows.

## Qual largura da banda eu terei com a nova configuração e ela terá a mesma taxa que atualmente?
{: #bandwidth}

Você recebe um pacote de largura da banda atual mais fortemente relacionado ao pacote que você tem atualmente. A
taxa para esse pacote será a que sua taxa ou pacote atual incluir.

## Como copiar dados do meu servidor antigo para o novo?
{: #old-server}

Depois de estabelecer a conectividade entre os servidores antigo e novo, é necessário considerar como
mover os dados entre eles.  Supondo que você tenha armazenamento suficiente no novo servidor para acomodar o volume de
dados, uma cópia direta de servidor para servidor é a maneira mais simples de fazer isso.  Há muitas ferramentas
disponíveis que podem ser usadas.  

* O SCP é uma boa opção para copiar com segurança um arquivo da origem para o destino. Ele executa uma cópia
linear simples. 
* Se você precisa copiar vários arquivos, rsync por ssh é muito mais rápido que scp. O rsync também copia estruturas de diretório e preserva permissões de arquivo.

Em geral, é necessário copiar apenas os aplicativos e os dados do aplicativo entre os sistemas. Copiar versões
mais antigas de arquivos de sistema operacional para uma versão mais nova pode causar problemas.

Encerre os bancos de dados antes de copiá-los entre os sistemas para assegurar que os dados sejam consistentes. Ao
migrar os dados do banco de dados, certifique-se de que eles sejam migrados de tal forma que não limitem as opções
para importá-los para o novo sistema. Em vez de copiar dados do banco de dados de sistema para sistema, considere exportá-los para um formato para que seja possível importar para um banco de dados mais novo. Arquivos de texto simples, arquivos CSV e outros arquivos, fornecem mais opções do que usar formatos de arquivo proprietários ou fechados quando se trata de mover dados entre os sistemas. Sempre teste as abordagens de migração de dados em um pequeno conjunto de dados
de teste antes de executar a cópia oficial.

## É necessário configurar minha rede novamente no novo site?
{: #networking}

Provavelmente a sua rede precisará de mudanças para funcionar com os servidores e o site novos. Se você
precisar de ajuda com esse processo, entre em contato com a equipe de suporte por telefone ou bate-papo.

## O que eu faço se não tiver conhecimento técnico para realizar a migração?
{: #migrate-skills}

A migração do aplicativo pode ser uma tarefa complexa. Não menos importante são as qualificações necessárias para fazer isso. Se forem necessárias mudanças de código para o aplicativo, certifique-se de que você tenha as qualificações de programação necessárias. Esse é o caso com os sistemas mais antigos em que qualificações podem estar em falta ou em que há uma falta de documentação ou conhecimento sobre o próprio sistema. Se houver um esforço significativo e o sistema for crítico para o negócio, considere investir em serviços pagos ou em outros serviços de migração para ajudá-lo.

## Como obtenho ajuda geral com a migração?
{: #gen-migration}

Dependendo do nível de ajuda que você precisar, é possível entrar em contato com o suporte por telefone ou
bate-papo. Ou é possível entrar em contato com a equipe de serviços gerenciados para obter assistência.

## Quem eu contato se não tiver um gerente de contas?
{: #account-contact}

É possível entrar em contato com o suporte por telefone ou bate-papo para qualquer pergunta de migração que tiver.
