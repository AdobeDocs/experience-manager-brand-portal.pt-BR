---
title: Usar facetas de busca personalizada
seo-title: Use custom search facets
description: Os administradores podem adicionar predicados de pesquisa ao painel Filtros para personalizar a pesquisa e tornar a funcionalidade de pesquisa versátil.
seo-description: Administrators can add search predicates to the Filters panel to customize search and make the search functionality versatile.
uuid: 986fba5a-fac5-4128-ac75-d04da5b52d45
content-type: reference
topic-tags: administration
products: SG_EXPERIENCEMANAGER/Brand_Portal
discoiquuid: 19faa028-246b-42c7-869f-97c95c7a1349
role: Admin
exl-id: c07e1268-2c83-40ba-8dcd-5dade3a10141
source-git-commit: 955cd8afe939ff47e9f08f312505e230e2f38495
workflow-type: tm+mt
source-wordcount: '1279'
ht-degree: 10%

---

# Usar facetas de busca personalizada {#use-custom-search-facets}

Os administradores podem adicionar predicados de pesquisa ao painel [!UICONTROL Filtros] para personalizar a pesquisa e tornar a funcionalidade de pesquisa versátil.

O Brand Portal suporta [pesquisa facetada](../using/brand-portal-searching.md#search-using-facets-in-filters-panel) para pesquisas granulares de ativos de marca aprovados, o que é possível devido a [**Filtros** painel](../using/brand-portal-searching.md#search-using-facets-in-filters-panel). Os aspectos de pesquisa são disponibilizados no painel Filtros por meio do **[!UICONTROL Formulário de pesquisa]** nas ferramentas administrativas. Um formulário de pesquisa padrão chamado Painel de pesquisa do administrador de ativos existe na página Pesquisar Forms nas ferramentas administrativas. No entanto, os administradores podem personalizar o painel Filtros padrão editando o Formulário de pesquisa padrão (Painel de pesquisa do administrador de ativos) adicionando, modificando ou removendo predicados de pesquisa, tornando assim a funcionalidade de pesquisa versátil.

Você pode usar vários predicados de pesquisa para personalizar o painel **[!UICONTROL Filters]**. Por exemplo, adicione o predicado de propriedade para procurar ativos que correspondem a uma única propriedade especificada neste predicado. Adicione o predicado de opções para procurar ativos que correspondam a um ou mais valores especificados para uma propriedade específica. Adicione o predicado de intervalo de datas para procurar ativos criados em um intervalo de datas especificado.

>[!NOTE]
>
>O Experience Manager Assets permite que as organizações [publiquem os formulários de pesquisa personalizados do AEM Author](../using/publish-schema-search-facets-presets.md#publish-search-facets-to-brand-portal) no Brand Portal, em vez de recriar o mesmo formulário no Brand Portal.

## Adicionar um predicado de pesquisa {#add-a-search-predicate}

Para adicionar um predicado de pesquisa ao painel **[!UICONTROL Filtros]**:

1. Para acessar ferramentas administrativas, clique no logotipo do Experience Manager na barra de ferramentas na parte superior.

   ![](assets/aemlogo.png)

1. No painel Ferramentas administrativas, clique em **[!UICONTROL Pesquisar Forms]**.

   ![](assets/navigation-panel-1.png)

1. Na página **[!UICONTROL Pesquisar Forms]**, selecione **[!UICONTROL Painel de pesquisa do administrador de ativos]**.

   ![](assets/search-forms-page.png)

1. Na barra de ferramentas que aparece na parte superior, clique em **[!UICONTROL Editar]** para abrir o formulário de pesquisa de edição.

   ![](assets/edit-search-form-1.png)

1. Na página [!UICONTROL Editar formulário de pesquisa], arraste um predicado da guia [!UICONTROL Selecionar predicado] para o painel principal. Por exemplo, arraste **[!UICONTROL Predicado de propriedade]**.

   O campo **[!UICONTROL Propriedade]** aparece no painel principal e a guia **[!UICONTROL Configurações]** à direita exibe os predicados de propriedade.

   ![](assets/partial-prop-predicate.png)

   >[!NOTE]
   >
   >O rótulo do cabeçalho na guia **[!UICONTROL Settings]** identifica o tipo de predicado selecionado.

1. Na guia **[!UICONTROL Settings]**, insira um rótulo, um texto de espaço reservado e uma descrição para o predicado da propriedade.

   * Selecione **[!UICONTROL Pesquisa parcial]**, se desejar permitir a pesquisa de frase parcial (e pesquisa curinga) de ativos com base no valor da propriedade especificada. Por padrão, o predicado suporta a pesquisa de texto completo.
   * Selecione **[!UICONTROL Ignorar maiúsculas e minúsculas]**, se desejar que a pesquisa de ativos baseada no valor da propriedade não diferencie maiúsculas e minúsculas. Por padrão, a pesquisa por valores de propriedade no Filtro de pesquisa diferencia maiúsculas de minúsculas.

   >[!NOTE]
   >
   >Ao marcar a caixa de seleção **[!UICONTROL Pesquisa parcial]**, **[!UICONTROL Ignorar maiúsculas e minúsculas]** é selecionado por padrão.

1. No campo **[!UICONTROL Nome da propriedade]**, abra o seletor de propriedades e selecione a propriedade com base na qual a pesquisa é realizada. Como alternativa, insira um nome para a propriedade. Por exemplo, insira `  jcr :content/metadata/dc:title` ou `./jcr:content/metadata/dc:title`.

   >[!NOTE]
   >
   >No Brand Portal, todas as propriedades (exceto aquelas que começam com `xmp`) em `jcrcontent/metadata` de `dam:asset` são indexadas por padrão.
   >
   >Qualquer propriedade indexada pode ser usada durante a criação de um predicado de propriedade. Se qualquer propriedade não indexada estiver configurada, a consulta de pesquisa em uma propriedade não indexada poderá não fornecer nenhum resultado de pesquisa.

   ![](assets/title-prop.png)

1. Clique em **[!UICONTROL Concluído]** para salvar as configurações.
1. Na interface do usuário [!UICONTROL Assets], clique no ícone de sobreposição e escolha **[!UICONTROL Filtro]** para navegar até o painel **[!UICONTROL Filtros]**. O predicado **[!UICONTROL Propriedade]** é adicionado ao painel.

   ![](assets/property-filter-panel.png)

1. Insira um título para o ativo a ser pesquisado na caixa de texto **[!UICONTROL Propriedade]**. Por exemplo, &quot;Adobe&quot;. Ao realizar uma pesquisa, os ativos com o título correspondente a &quot;Adobe&quot; são exibidos nos resultados da pesquisa.

## Lista de predicados de pesquisa {#list-of-search-predicates}

Semelhante à forma como você adiciona um predicado **[!UICONTROL Propriedade]**, você pode adicionar os seguintes predicados ao painel **[!UICONTROL Filtros]**:

| **Nome do predicado** | **Descrição** | **Propriedades** |
|-------|-------|----------|
| **[!UICONTROL Navegador de caminhos]** | Predicado de pesquisa para pesquisar ativos em um local específico. **Observação:** *para um usuário conectado, o navegador de caminho no Filtro mostra somente a estrutura de conteúdo das pastas (e seus ancestrais) compartilhadas com o usuário.* <br> Os usuários administradores podem pesquisar ativos em qualquer pasta navegando até essa pasta usando o Navegador de caminhos. <br> Enquanto isso, usuários não administradores podem pesquisar ativos em uma pasta (acessível a eles) navegando até essa pasta no Navegador de caminhos. | <ul><li>Rótulo do campo</li><li>Caminho</li><li>Descrição</li></ul> |
| **[!UICONTROL Propriedade]** | Pesquise ativos com base em uma propriedade de metadados específica. **Observação:** *ao selecionar Pesquisa parcial, a opção Ignorar maiúsculas e minúsculas é selecionada por padrão*. | <ul><li>Rótulo do campo</li><li>Espaço reservado</li><li>Nome da Propriedade</li><li>Pesquisa parcial</li><li>Ignorar diferença entre maiúsculas e minúsculas</li><li> Descrição</li></ul> |
| **[!UICONTROL Propriedade de vários valores]** | Semelhante ao predicado de propriedade, mas permite vários valores de entrada, separados por um delimitador (o padrão é COMMA[,]) os ativos correspondentes a qualquer um dos valores de entrada são retornados nos resultados. | <ul><li>Rótulo do campo</li><li>Espaço reservado</li><li>Nome da propriedade</li><li>Suporte do delimitador</li><li>Ignorar diferença entre maiúsculas e minúsculas</li><li>Descrição</li></ul> |
| **[!UICONTROL Tags]** | Predicado de pesquisa para pesquisar ativos com base em tags. Você pode configurar a propriedade Caminho para preencher várias tags na lista Tags. *Observação: Os administradores podem precisar alterar o valor do caminho, por exemplo, [!UICONTROL `/etc/tags/mac/<tenant_id>/<custom_tag_namespace>`], se publicarem o formulário de pesquisa de AEM, onde o caminho não inclui informações do locatário, por exemplo, [!UICONTROL `/etc/tags/<custom_tag_namespace>`]. | <ul><li>Rótulo do campo</li><li>Nome da propriedade</li><li>Caminho</li><li>Descrição</li></ul> |
| **[!UICONTROL Caminho]** | Predicado de pesquisa para pesquisar ativos em um local específico. | <ul><li>Rótulo do campo</li><li>Caminho</li><li>Descrição</li></ul> |  |
| **[!UICONTROL Data relativa]** | O predicado de pesquisa para pesquisar ativos com base na data relativa de sua criação. | <ul><li>Rótulo do campo</li><li>Nome da propriedade</li><li>Data relativa</li></ul> |
| **[!UICONTROL Intervalo]** | predicado de pesquisa para pesquisar ativos que estão dentro de um intervalo especificado de valores de propriedade. No painel Filtros , é possível especificar valores de propriedade mínimos e máximos para o intervalo. | <ul><li>Rótulo do campo</li><li>Nome da propriedade</li><li>Descrição</li></ul> |
| **[!UICONTROL Intervalo de datas]** | Procure por ativos criados em um intervalo especificado para uma propriedade date . No painel Filtros , é possível especificar as Datas de início e fim. | <ul><li>Rótulo do campo</li><li>Espaço reservado</li><li>Nome da propriedade</li><li>Texto do intervalo (de)</li><li>Texto do intervalo (até)</li><li>Descrição</li></ul> |
| **[!UICONTROL Data]** | Procure por um predicado com base em um controle deslizante de ativos com base em uma propriedade de data. | <ul><li>Rótulo do campo</li><li>Nome da propriedade</li><li>Descrição</li></ul> |
| **[!UICONTROL Tamanho do arquivo]** | Predicado de pesquisa para pesquisar ativos com base em seu tamanho. | <ul><li>Rótulo do campo</li><li>Nome da propriedade</li><li>Caminho</li><li>Descrição</li></ul> |
| **[!UICONTROL Última modificação do ativo]** | Pesquisar predicado para pesquisar ativos com base na data da última modificação. | <ul><li>Rótulo do campo</li><li>Nome da propriedade</li><li>Descrição</li></ul> |
| **[!UICONTROL Status de aprovação]** | Procure o predicado para pesquisar ativos com base na propriedade de metadados de aprovação. O nome padrão da propriedade é **dam:status**. | <ul><li>Rótulo do campo</li><li>Nome da propriedade</li><li>Descrição</li></ul> |
| **[!UICONTROL Status da retirada]** | Predicado de pesquisa para pesquisar ativos com base no status de check-out de um ativo quando ele foi publicado no AEM Assets. | <ul><li>Rótulo do campo</li><li>Nome da propriedade</li><li>Descrição</li></ul> |
| **[!UICONTROL Retirado por]** | Predicado de pesquisa para pesquisar ativos com base no usuário que fez check-out do ativo. | <ul><li>Rótulo do campo</li><li>Nome da propriedade</li><li>Descrição</li></ul> |
| **[!UICONTROL Status da expiração]** | Pesquisar predicado para pesquisar ativos com base no status de expiração. | <ul><li>Rótulo do campo</li><li>Nome da propriedade</li><li>Descrição</li></ul> |
| **[!UICONTROL Membro da coleção]** | predicado de pesquisa para pesquisar ativos com base em se um ativo faz parte de uma coleção. | Descrição |
| **[!UICONTROL Oculto]** | Esse predicado não é explicitamente visível para os usuários finais e é usado para quaisquer restrições ocultas normalmente para restringir o tipo de resultados da pesquisa a **dam:Asset**. | <ul><li>Rótulo do campo</li><li>Nome da propriedade</li><li>Descrição</li></ul> |

>[!NOTE]
>
>Não use o **[!UICONTROL Predicado de opções]**, **[!UICONTROL Predicado de status de publicação]** e **[!UICONTROL Predicado de classificação]**, pois esses predicados não estão funcionando no Brand Portal.

## Excluir um predicado de pesquisa {#delete-a-search-predicate}

Para excluir um predicado de pesquisa, siga estas etapas:

1. Clique no logotipo do Adobe para acessar as ferramentas administrativas.

   ![](assets/aemlogo.png)

1. No painel Ferramentas administrativas, clique em **[!UICONTROL Pesquisar Forms]**.

   ![](assets/navigation-panel-2.png)

1. Na página **[!UICONTROL Pesquisar Forms]**, selecione **[!UICONTROL Painel de pesquisa do administrador de ativos]**.

   ![](assets/search-forms-page.png)

1. Na barra de ferramentas que aparece na parte superior, clique em **[!UICONTROL Editar]** para abrir o formulário de pesquisa de edição.

   ![](assets/edit-search-form-2.png)

1. Na página [!UICONTROL Editar formulário de pesquisa], no painel principal, selecione o predicado que deseja excluir. Por exemplo, selecione **[!UICONTROL Predicado de propriedade]**.

   A guia **[!UICONTROL Settings]** à direita exibe os campos de predicado de propriedade.

1. Para excluir o predicado da propriedade, clique no ícone bin . Na caixa de diálogo **[!UICONTROL Excluir campo]**, clique em **[!UICONTROL Excluir]** para confirmar a ação de exclusão.

   O campo **[!UICONTROL Predicado de propriedade]** é removido do painel principal e a guia **[!UICONTROL Configurações]** fica vazia.

   ![](assets/search-form-delete-predicate.png)

1. Para salvar as alterações, clique em **[!UICONTROL Concluído]** na barra de ferramentas.
1. Na interface do usuário **[!UICONTROL Assets]**, clique no ícone de sobreposição e escolha **[!UICONTROL Filtro]** para navegar até o painel **[!UICONTROL Filtros]**. O predicado **[!UICONTROL Propriedade]** é removido do painel.

   ![](assets/property-predicate-removed.png)
