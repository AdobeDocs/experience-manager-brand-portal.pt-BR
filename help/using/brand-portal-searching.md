---
title: Pesquisar ativos no Brand Portal
description: O recurso de pesquisa do Brand Portal permite pesquisar rapidamente ativos relevantes usando o Omnisearch, e os filtros de pesquisa ajudam a restringir ainda mais sua pesquisa. Salve suas pesquisas como coleções inteligentes para o futuro.
contentOwner: bdhar
content-type: reference
products: SG_EXPERIENCEMANAGER/Brand_Portal
topic-tags: SearchandPromote
exl-id: 7297bbe5-df8c-4d0b-8204-218a9fdc2292
source-git-commit: 32a67abf466dd3bf635b851b02377ed23591915e
workflow-type: tm+mt
source-wordcount: '1343'
ht-degree: 0%

---

# Pesquisar ativos no Brand Portal {#search-assets-on-brand-portal}

O recurso de pesquisa do Brand Portal permite pesquisar rapidamente ativos relevantes usando o Omnisearch e a pesquisa facetada que usa filtros para ajudá-lo a restringir ainda mais sua pesquisa. Você pode pesquisar ativos no nível de arquivos ou pastas e salvar os resultados da pesquisa como coleções inteligentes.

>[!NOTE]
>
>O Brand Portal não oferece suporte à pesquisa de coleção usando o Omnisearch.
>
>No entanto, você pode usar [filtros de pesquisa para obter a lista de coleções relevantes](#search-collection).

## Pesquisar ativos usando o Omnisearch {#search-assets-using-omnisearch}

Para pesquisar ativos no Brand Portal:

1. Na barra de ferramentas, clique no ícone **[!UICONTROL Pesquisar]** ou pressione a tecla **[!UICONTROL /]** (barra) para iniciar o Omnisearch.

   ![](assets/omnisearchicon-1.png)

1. Na caixa de pesquisa, digite uma palavra-chave para os ativos que deseja pesquisar.

   ![](assets/omnisearch.png)

   >[!NOTE]
   >
   >* Pelo menos 3 caracteres são necessários no Omnisearch para que as sugestões de pesquisa sejam exibidas.
   >* Quando você pesquisa por `mountain biking`, o Omnisearch retorna todos os ativos nos resultados da pesquisa que têm `mountain` e `biking` disponíveis nos campos de metadados. Por exemplo, `mountain` no campo `Title` e `biking` no campo `Description`. Ambos os termos devem estar disponíveis nos campos de metadados para serem exibidos nos resultados da pesquisa. No entanto, o Omnisearch retorna o ativo nos resultados da pesquisa mesmo se apenas um dos dois termos estiver disponível no campo de metadados Tags inteligentes. Por exemplo, suponha que um ativo tenha `mountain` como uma Marca Inteligente, mas não tenha `biking` em nenhum outro campo de metadados. Em seguida, procure por `mountain biking`. O Omnisearch ainda retorna o ativo nos resultados da pesquisa. Esse fluxo de trabalho garante que os ativos com tags relevantes não sejam perdidos.

1. Selecione entre as sugestões relacionadas que aparecem na lista suspensa para acessar ativos relevantes rapidamente.

   ![](assets/assets-search-result.png)

   *Pesquisa de ativos usando o Omnisearch*

Para saber mais sobre o comportamento da pesquisa com ativos com tags inteligentes, acesse [entender os resultados e o comportamento da pesquisa](https://experienceleague.adobe.com/br/docs/experience-manager-65/content/assets/using/search-assets).

## Pesquisar usando aspectos no painel Filtros {#search-using-facets-in-filters-panel}

Os aspectos de pesquisa no painel Filtros adicionam granularidade à experiência de pesquisa e tornam a funcionalidade de pesquisa mais eficiente. Os aspectos de pesquisa usam várias dimensões (predicados) que permitem realizar pesquisas complexas. Você pode facilmente detalhar o nível desejado de detalhes para uma pesquisa mais focada.

Por exemplo, se estiver procurando uma imagem, você pode escolher se deseja uma imagem de bitmap ou de vetor. Você pode restringir ainda mais o escopo de pesquisa especificando o tipo MIME da imagem na faceta de pesquisa Tipo de arquivo. Da mesma forma, ao pesquisar documentos, você pode especificar o formato, por exemplo, formato PDF ou MS® Word.

![Painel Filtros no painel Brand Portal](assets/file-type-search.png "Filtros no Brand Portal")

O painel **[!UICONTROL Filtros]** inclui algumas facetas padrão, como:- **[!UICONTROL Navegador de Caminho]**, **[!UICONTROL Tipo de Arquivo]**, **[!UICONTROL Tamanho de Arquivo]**, **[!UICONTROL Status]** e **[!UICONTROL Orientação]**.
No entanto, você pode [adicionar aspectos de pesquisa personalizados](../using/brand-portal-search-facets.md) ou remover aspectos específicos do painel **[!UICONTROL Filtros]**. Basta editar os predicados no Formulário de pesquisa subjacente. Consulte a lista dos [predicados de pesquisa disponíveis e utilizáveis no Brand Portal](../using/brand-portal-search-facets.md#list-of-search-predicates).

Para aplicar filtros à sua pesquisa, usando as [facetas de pesquisa](../using/brand-portal-search-facets.md) disponíveis:

1. Clique no ícone de sobreposição e selecione **[!UICONTROL Filtro]**.

   ![](assets/selectorrail.png)

1. No painel **[!UICONTROL Filtros]** à esquerda, selecione as opções apropriadas para aplicar os filtros relevantes.
Por exemplo, use os seguintes filtros padrão:

   * **[!UICONTROL Navegador de caminhos]** para pesquisar ativos em um diretório específico. O caminho de pesquisa padrão do predicado para o Navegador de Caminho é `/content/dam/mac/<tenant-id>/`, que pode ser configurado ao editar o Formulário de Pesquisa padrão.

   >[!NOTE]
   >
   >Para usuários não administradores, o [!UICONTROL Navegador de Caminhos] do painel [!UICONTROL Filtro] mostra somente a estrutura de conteúdo das pastas (e suas pastas ancestrais) compartilhadas com eles.\
   >Para usuários administradores, o Navegador de caminhos permite navegar até qualquer pasta no Brand Portal.

   * **[!UICONTROL Tipo de arquivo]** para especificar o tipo (imagem, documento, multimídia, arquivo morto) de arquivo de ativo que você está procurando. Além disso, é possível restringir o escopo da pesquisa. Por exemplo, especifique o tipo MIME (Tiff, Bitmap, Imagens GIMP) para imagem ou formato (PDF ou MS® Word) para os documentos.
   * **[!UICONTROL Tamanho do arquivo]** para procurar ativos com base em seu tamanho. Você pode especificar os limites inferiores e superiores para o intervalo de tamanho para restringir sua pesquisa e especificar a unidade de medida a ser pesquisada.
   * **[!UICONTROL Status]** para procurar ativos com base no status dos ativos, como Aprovação (Aprovado, Alterações Solicitadas, Rejeitado, Pendente) e Expiração.
   * **[!UICONTROL Classificação média]** para procurar ativos com base na classificação dos ativos.
   * **[!UICONTROL Orientação]** para procurar ativos com base na orientação (horizontal, vertical, quadrada) dos ativos.
   * **[!UICONTROL Estilo]** para procurar ativos com base no estilo (colorido, monocromático) dos ativos.
   * **[!UICONTROL Formato de vídeo]** para procurar ativos de vídeo com base em seu formato (DVI, Flash, MPEG4, MPEG, OGG Theora, QuickTime, Windows Media, WebM).

   Você pode usar [aspectos de pesquisa personalizados](../using/brand-portal-search-facets.md) no painel Filtros editando o Formulário de Pesquisa subjacente.

   * O **[!UICONTROL Predicado da propriedade]**, se usado no Formulário de pesquisa, permite procurar ativos que correspondam a uma propriedade de metadados para a qual o predicado está mapeado.\
     Por exemplo, se o Predicado da propriedade estiver mapeado para `jcr:content/metadata/dc:title`, você poderá pesquisar ativos com base no título.\
     O [!UICONTROL Predicado de Propriedade] dá suporte a pesquisas de texto para:

     **Frases parciais**
Para permitir a pesquisa de ativos usando frases parciais no Predicado de propriedade, habilite a caixa de seleção **[!UICONTROL Pesquisa parcial]** no Formulário de pesquisa. Esse método permite pesquisar pelos ativos desejados mesmo se você não especificar as palavras ou frases exatas usadas nos metadados do ativo.

     >[!NOTE]
     >
     > O Brand Portal oferece suporte aos seguintes campos para Pesquisa parcial:
     >
     >* `jcr:content/metadata/dc:title`
     >* `jcr:content/jcr:title`
     >* `jcr:content/metadata/dc:format`

     É possível:
      * No painel Filtros, especifique uma palavra que ocorre na frase pesquisada na faceta. Por exemplo, se você pesquisar pelo termo **climb** (e o Predicado de Propriedade for mapeado para a propriedade `dc:title`), todos os ativos com a palavra **climb** na frase de título são retornados.
      * Especifique uma parte da palavra que ocorre na frase pesquisada, juntamente com um caractere curinga (&#42;) para preencher as lacunas.
Por exemplo, pesquisando por:
         * **climb&#42;** retorna todos os ativos que têm palavras que começam com os caracteres &quot;climb&quot; na frase de título.
         * **&#42;climb** retorna todos os ativos com palavras que terminam com caracteres &quot;climb&quot; na frase de título.
         * **&#42;climb&#42;** retorna todos os ativos que contêm palavras que compõem os caracteres &quot;climb&quot; na frase de título.

     **Texto sem diferenciação de maiúsculas e minúsculas**
Você pode permitir pesquisas que não diferenciam maiúsculas de minúsculas no Predicado de propriedades. Basta habilitar a caixa de seleção **[!UICONTROL Ignorar maiúsculas e minúsculas]** no Formulário de Pesquisa. Por padrão, a pesquisa de texto no Predicado de propriedade diferencia maiúsculas de minúsculas.

   >[!NOTE]
   >
   >Ao marcar a caixa de seleção **[!UICONTROL Pesquisa parcial]**, **[!UICONTROL Ignorar maiúsculas e minúsculas]** é selecionado por padrão.

   ![](assets/wildcard-prop-1.png)

   Os resultados da pesquisa são exibidos de acordo com os filtros aplicados, juntamente com a contagem de resultados da pesquisa.

   ![](assets/omnisearch-with-filters.png)

   Resultado da pesquisa de ativos com contagem de resultados da pesquisa.

1. Você pode navegar facilmente para um item do resultado da pesquisa e retornar ao mesmo resultado usando o botão Voltar no navegador sem precisar executar a consulta novamente.

## Salvar suas pesquisas como coleção inteligente {#save-your-searches-as-smart-collection}

Você pode salvar as configurações de pesquisa como uma coleção inteligente para poder repetir a mesma pesquisa rapidamente sem precisar refazer as mesmas configurações posteriormente. No entanto, não é possível aplicar filtros de pesquisa em uma coleção.

Para salvar as configurações de pesquisa como uma coleção inteligente:

1. Clique em **[!UICONTROL Salvar coleção inteligente]** e forneça um nome para a coleção inteligente.

   Para tornar a coleção inteligente acessível a todos os usuários, selecione **[!UICONTROL Público]**. Uma mensagem confirma que a coleção inteligente foi criada e adicionada à lista de pesquisas salvas.

   >[!NOTE]
   >
   >Você pode impedir que usuários não administradores tornem as coleções inteligentes públicas para evitar que um grande número de coleções inteligentes públicas sejam criadas por usuários não administradores no Brand Portal da organização. As organizações podem desabilitar a configuração **[!UICONTROL Permitir criação de coleções públicas inteligentes]** das configurações **[!UICONTROL Geral]** disponíveis no painel Ferramentas administrativas.

   ![](assets/save_smartcollectionui.png)

1. Para salvar a coleção inteligente com outro nome e marcar ou desmarcar a caixa de seleção **[!UICONTROL Pública]**, clique em **[!UICONTROL Editar Coleção Inteligente]**.

   ![](assets/edit_smartcollection.png)

1. Na caixa de diálogo **[!UICONTROL Editar coleção inteligente]**, selecione **[!UICONTROL Salvar como]** e digite um nome para a coleção inteligente. Clique em **[!UICONTROL Salvar]**.

   ![](assets/saveas_smartsearch.png)


## Pesquisar coleção {#search-collection}

O Omnisearch não é compatível com coleções. No entanto, você pode aplicar filtros de pesquisa para listar as coleções relevantes na interface [!UICONTROL Coleções].

Na interface [!UICONTROL Coleções], clique no ícone de sobreposição para abrir o painel de filtro no painel esquerdo. Aplique um ou vários filtros de pesquisa a partir dos filtros disponíveis (`modified date`, `access type` e `tags`). Ele lista o conjunto de coleções mais relevante com base nos filtros aplicados.

![](assets/collection-search.png)
