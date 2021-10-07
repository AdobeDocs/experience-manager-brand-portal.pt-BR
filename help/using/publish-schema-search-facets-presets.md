---
title: Publicar predefinições, esquema e aspectos no Brand Portal
seo-title: Publish presets, schema, and facets to Brand Portal
description: Saiba como publicar predefinições, esquema e aspectos no Brand Portal.
seo-description: Learn how to publish presets, schema, and facets to Brand Portal.
uuid: c836d9bb-074a-4113-9c91-b2bf7658b88d
topic-tags: publish
products: SG_EXPERIENCEMANAGER/Brand_Portal
content-type: reference
discoiquuid: bc305abc-9373-4d33-9179-0a5f3904b352
exl-id: 9b585606-6538-459b-87a9-2e68df0087b3
source-git-commit: 4caa4263bd74b51af7504295161c421524e51f0c
workflow-type: tm+mt
source-wordcount: '1141'
ht-degree: 2%

---

# Publicar predefinições, esquema e aspectos no Brand Portal {#publish-presets-schema-and-facets-to-brand-portal}

O artigo aborda a publicação de predefinições de imagens, esquemas de metadados e aspectos de pesquisa personalizados da instância do autor do AEM para o Brand Portal. O recurso de publicação permite que as organizações reutilizem predefinições de imagens, esquemas de metadados e aspectos de pesquisa criados/modificados na instância de autor do AEM, reduzindo assim os esforços duplicados.

>[!NOTE]
>
>A capacidade de publicar predefinições de imagens, esquema de metadados e aspectos de pesquisa da instância do autor do AEM para o Brand Portal está disponível AEM 6.2 SP1-CFP7 e AEM 6.3 SP 1-CFP 1 (6.3.1.1) em diante.

## Publicar predefinições de imagens no Brand Portal {#publish-image-presets-to-brand-portal}

As predefinições de imagens são um conjunto de comandos de dimensionamento e formatação aplicados à imagem no momento da entrega da imagem. As predefinições de imagens podem ser criadas e modificadas no Brand Portal. Como alternativa, se a instância do autor do AEM estiver em execução no modo de mídia dinâmica, os usuários poderão criar predefinições no autor do AEM e publicá-las no AEM Assets Brand Portal e evitar a recriação das mesmas predefinições no Brand Portal.\
Depois que a predefinição é criada, ela é listada como representação dinâmica no painel de representações de detalhes do ativo e na caixa de diálogo de download.

>[!NOTE]
>
>Se a instância do autor do AEM não estiver em execução no **[!UICONTROL Modo Dynamic Media]** (o cliente não comprou o Dynamic Media), a representação **[!UICONTROL TIFF de pirâmide]** dos ativos não será criada no momento do upload. As predefinições de imagem ou representações dinâmicas funcionam em **[!UICONTROL Pyramid TIFF]** de um ativo, portanto, se **[!UICONTROL Pyramid TIFF]** não estiver disponível na instância do autor do AEM, também não estará disponível no Brand Portal. Como resultado, nenhuma representação dinâmica está presente no painel de representações da página de detalhes do ativo e na caixa de diálogo de download.

Para publicar predefinições de imagens no Brand Portal:

1. Na instância do autor do AEM, toque/clique no logotipo do AEM para acessar o console de navegação global e toque/clique no ícone Ferramentas e navegue até **[!UICONTROL Ativos > Predefinições de imagem]**.
1. Selecione a predefinição de imagem ou várias predefinições de imagem da lista de predefinições de imagem e clique/ toque em **[!UICONTROL Publicar no Brand Portal]**.

![](assets/publishpreset.png)

>[!NOTE]
>
>Quando os usuários clicam em **[!UICONTROL Publicar no Brand Portal]**, as predefinições de imagem são enfileiradas para publicação. Os usuários são aconselhados a monitorar o log dos agentes de replicação para confirmar se a publicação foi bem-sucedida.

Para cancelar a publicação de uma predefinição de imagem do Brand Portal:

1. Na instância do autor do AEM, toque/clique no logotipo do AEM para acessar o console de navegação global e toque/clique no ícone **[!UICONTROL Ferramentas]** e navegue até **[!UICONTROL Ativos > Predefinições de imagem]**.
1. Selecione uma predefinição de imagem e selecione **[!UICONTROL Remover do Brand Portal]** a partir das opções disponíveis na parte superior.

## Publicar esquema de metadados no Brand Portal  {#publish-metadata-schema-to-brand-portal}

O esquema de metadados descreve o layout e as propriedades exibidas na página de propriedades do ativo/coleções.

![](assets/metadata-schema-editor.png) ![](assets/asset-properties-1.png)

Se os usuários tiverem editado o esquema padrão na instância do autor do AEM e estiverem dispostos a usar o mesmo esquema como esquema padrão no Brand Portal, eles poderão simplesmente publicar os formulários de esquema de metadados no Brand Portal. Nesse cenário, o esquema padrão no Brand Portal é substituído pelos esquemas padrão publicados na instância do autor do AEM.

Se os usuários criaram um esquema personalizado na instância do autor do AEM, eles podem publicar o esquema personalizado no Brand Portal em vez de recriar o mesmo esquema personalizado lá. Os usuários podem aplicar esse esquema personalizado a qualquer pasta/coleção no Brand Portal.

>[!NOTE]
>
>Os esquemas padrão não podem ser publicados na Brand Portal se estiverem bloqueados na instância de AEM (ou seja, se não estiverem editados).

![](assets/default-schema-form.png)

>[!NOTE]
>
>Se uma pasta tiver um schema aplicado na instância do autor do AEM, o mesmo schema também deverá existir no Brand Portal para manter a consistência na página de propriedades do ativo no AEM Author e Brand Portal.

Para publicar um esquema de metadados da instância do autor do AEM no Brand Portal:

1. Na instância do autor do AEM, toque/clique no logotipo do AEM para acessar o console de navegação global e toque/clique no ícone Ferramentas e navegue até **[!UICONTROL Ativos > Esquemas de metadados]**.
1. Selecione um esquema de metadados e selecione **[!UICONTROL Publicar no Brand Portal]** a partir das opções disponíveis na parte superior.

>[!NOTE]
>
>Quando os usuários clicam em **[!UICONTROL Publicar no Brand Portal]**, os esquemas de metadados são enfileirados para publicação. Os usuários são aconselhados a monitorar o log dos agentes de replicação para confirmar se a publicação foi bem-sucedida.

Para cancelar a publicação de um esquema de metadados do Brand Portal:

1. Na instância do autor do AEM, toque/clique no logotipo do AEM para acessar o console de navegação global e toque/clique no ícone Ferramentas e navegue até **[!UICONTROL Ativos > Esquemas de metadados]**.
1. Selecione um esquema de metadados e selecione **[!UICONTROL Remover do Brand Portal]** a partir das opções disponíveis na parte superior.

## Publicar aspectos de pesquisa no Brand Portal {#publish-search-facets-to-brand-portal}

Os formulários de pesquisa fornecem o recurso de [pesquisa facetada](../using/brand-portal-search-facets.md) para os usuários no Brand Portal. Os aspectos de pesquisa conferem maior granularidade às pesquisas no Brand Portal. Todos os [predicados adicionados](https://experienceleague.adobe.com/docs/experience-manager-65/assets/administer/search-facets.html) no formulário de pesquisa estão disponíveis para os usuários como facetas de pesquisa em filtros de pesquisa.

![](assets/property-predicate-removed.png)
![](assets/search-form.png)

Se você estiver disposto a usar o formulário de pesquisa personalizado **[!UICONTROL Painel de pesquisa do administrador de ativos]** da instância do autor do AEM, em vez de recriar o mesmo formulário no Brand Portal, poderá publicar o formulário de pesquisa personalizado da instância do autor do AEM para o Brand Portal.

>[!NOTE]
>
>O formulário de pesquisa bloqueado **[!UICONTROL Painel de pesquisa do administrador de ativos]** no AEM Assets não pode ser publicado no Brand Portal, a menos que seja editado. Depois de editado e publicado no Brand Portal, esse formulário de pesquisa substitui o formulário de pesquisa no Brand Portal.

Para publicar a faceta de pesquisa editada da instância do autor do AEM no Brand Portal:

1. Toque/clique no logotipo do AEM e acesse **[!UICONTROL Ferramentas > Geral > Pesquisar formulários]**.
1. Selecione o formulário de pesquisa editado e selecione **[!UICONTROL Publicar no Brand Portal]**.

   >[!NOTE]
   >
   >Quando os usuários clicam em **[!UICONTROL Publicar no Brand Portal]**, os aspectos de pesquisa são enfileirados para publicação. Os usuários são aconselhados a monitorar o log dos agentes de replicação para confirmar se a publicação foi bem-sucedida.

Para cancelar a publicação de formulários de pesquisa no Brand Portal:

1. Na instância do autor do AEM, toque/clique no logotipo do AEM para acessar o console de navegação global e toque/clique no ícone Ferramentas e navegue até **[!UICONTROL Geral > Pesquisar Forms]**.
1. Selecione o formulário de pesquisa e selecione **[!UICONTROL Remover do Brand Portal]** a partir das opções disponíveis na parte superior.

>[!NOTE]
>
>A ação **[!UICONTROL Cancelar publicação do Brand Portal]** deixa o formulário de pesquisa padrão no Brand Portal e não é restaurada para o último formulário de pesquisa usado antes da publicação.

### Limitações           {#limitations}

1. Poucos predicados de pesquisa não se aplicam a filtros de pesquisa na Brand Portal. Quando esses predicados de pesquisa são publicados como parte do formulário de pesquisa da instância do autor do AEM para o Brand Portal, eles são filtrados. Os usuários, portanto, veem menos predicados no formulário publicado na Brand Portal. Consulte [predicados de pesquisa aplicáveis a filtros no Brand Portal](../using/brand-portal-search-facets.md#list-of-search-predicates).

1. Para [!UICONTROL Predicado de opções], se um usuário estiver usando qualquer caminho personalizado para ler opções na instância do autor do AEM, ele não funcionará no Brand Portal. Esses caminhos e opções adicionais não são publicados no Brand Portal com o formulário de pesquisa. Nesse caso, os usuários podem selecionar a opção **[!UICONTROL Manual]** em **[!UICONTROL Adicionar opções]** em **[!UICONTROL Predicado de opções]** para adicionar essas opções manualmente no Brand Portal.

![](assets/options-predicate-manual.png)
