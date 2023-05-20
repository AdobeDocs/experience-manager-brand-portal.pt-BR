---
title: Aplicar predefinições de imagens ou representações dinâmicas
seo-title: Apply image presets or dynamic renditions
description: Como uma macro, uma predefinição de imagem é uma coleção predefinida de comandos de dimensionamento e formatação salvos com um nome. As predefinições de imagem permitem que o Experience Manager Assets Brand Portal forneça imagens de diferentes tamanhos, formatos e propriedades de forma dinâmica.
seo-description: Like a macro, an image preset is a predefined collection of sizing and formatting commands saved under a name. Image presets enable Experience Manager Assets Brand Portal to dynamically deliver images of different sizes, formats, and properties.
uuid: a3c8705c-5fbd-472c-8b61-f65b3e552c1b
content-type: reference
topic-tags: administration
products: SG_EXPERIENCEMANAGER/Brand_Portal
discoiquuid: a512dfa0-fef3-4c3f-a389-a0a3a7415bac
role: Admin
exl-id: 212a1b3a-686f-4250-be06-b679b6039887
source-git-commit: 955cd8afe939ff47e9f08f312505e230e2f38495
workflow-type: tm+mt
source-wordcount: '814'
ht-degree: 3%

---

# Aplicar predefinições de imagens ou representações dinâmicas {#apply-image-presets-or-dynamic-renditions}

Como uma macro, uma predefinição de imagem é uma coleção predefinida de comandos de dimensionamento e formatação salvos com um nome. As predefinições de imagem permitem que o Experience Manager Assets Brand Portal forneça imagens de diferentes tamanhos, formatos e propriedades de forma dinâmica.

Uma predefinição de imagem é usada para gerar representações dinâmicas de imagens que podem ser visualizadas e baixadas. Ao visualizar imagens e suas representações, você pode escolher uma predefinição para reformatar imagens de acordo com as especificações definidas pelo administrador.

(*Se a instância do autor do Experience Manager Assets estiver em execução em **Modo híbrido do Dynamic Media***) Para visualizar representações dinâmicas de um ativo no Brand Portal, verifique se a representação tiff da Pirâmide existe na instância do autor do Experience Manager Assets de onde você publica no Brand Portal. Ao publicar o ativo, sua representação PTIFF também é publicada no Brand Portal.

>[!NOTE]
>
>Ao baixar imagens e suas representações, não há opção para escolher entre as predefinições existentes. Em vez disso, especifique as propriedades de uma predefinição de imagem personalizada. Para obter mais informações, consulte [Aplicar predefinições de imagens ao baixar imagens](../using/brand-portal-image-presets.md#main-pars-text-1403412644).


Para obter mais informações sobre os parâmetros necessários ao criar predefinições de imagens, consulte [Gerenciamento de predefinições da imagem](../using/brand-portal-image-presets.md).

## Criar uma predefinição de imagem {#create-an-image-preset}

Os administradores do Experience Manager Assets podem criar predefinições de imagens que aparecem como representações dinâmicas na página Detalhes do ativo. É possível criar uma predefinição de imagem do zero ou salvar uma existente com um novo nome. Ao criar uma predefinição de imagem, escolha um tamanho para a entrega da imagem e os comandos de formatação. Quando uma imagem é entregue para visualização, sua aparência é otimizada de acordo com os comandos escolhidos.

>[!NOTE]
>
>As representações dinâmicas de uma imagem são criadas usando sua TIFF de Pirâmide. Se o TIFF de pirâmide não estiver disponível para nenhum ativo, as representações dinâmicas desse ativo não poderão ser buscadas no Brand Portal.
>
>Se a instância do autor do Experience Manager Assets estiver em execução em **Modo híbrido do Dynamic Media**, as representações em Pyramid TIFF de ativos de imagem são criadas e salvas no repositório do Experience Manager Assets.
>
>Enquanto que, se a instância do autor do Experience Manager Assets estiver em execução em **Modo Dynamic Media Scene7**, as representações em Pyramid TIFF de ativos de imagem existem no servidor do Scene 7.
>
>Quando esses ativos são publicados no brand portal, as predefinições de imagem são aplicadas e as representações dinâmicas são exibidas.


1. Na barra de ferramentas na parte superior, clique no logotipo do Experience Manager para acessar as ferramentas administrativas.

1. No painel de ferramentas administrativas, clique em **[!UICONTROL Predefinições da imagem]**.

   ![](assets/admin-tools-panel-4.png)

1. Na página de predefinições da imagem, clique em **[!UICONTROL Criar]**.

   ![](assets/image_preset_homepage.png)

1. No **[!UICONTROL Editar predefinição de imagem]** insira os valores na variável **[!UICONTROL Básico]** e **[!UICONTROL Avançado]** guias conforme apropriado, incluindo um nome. As predefinições aparecem no painel à esquerda e podem ser usadas junto com outros ativos.

   ![](assets/image_preset_create.png)

   >[!NOTE]
   >
   >Você também pode usar a variável **[!UICONTROL Editar predefinição de imagem]** para editar as propriedades de uma predefinição de imagem existente. Para editar uma predefinição de imagem, selecione-a na página de predefinições de imagens e clique em **[!UICONTROL Editar]**.

1. Clique em **[!UICONTROL Salvar]**. A predefinição de imagem é criada e exibida na página de predefinições de imagem.
1. Para excluir uma predefinição de imagem, selecione-a na página de predefinições de imagens e clique em **[!UICONTROL Excluir]**. Na página de confirmação, clique em **[!UICONTROL Excluir]** para confirmar a exclusão. A predefinição de imagem é removida da página de predefinições de imagem.

## Aplicar predefinições de imagens ao visualizar imagens  {#apply-image-presets-when-previewing-images}

Ao visualizar imagens e suas representações, escolha entre as predefinições existentes para reformatar imagens de acordo com as especificações definidas pelo administrador.

1. Na interface do Brand Portal, clique em uma imagem para abri-la.
1. Clique no ícone de sobreposição à esquerda e escolha **[!UICONTROL Representações]**.

   ![](assets/image-preset-previewrenditions.png)

1. No **[!UICONTROL Representações]** selecione a representação dinâmica apropriada, por exemplo, **[!UICONTROL Miniatura]**. A imagem de pré-visualização é renderizada com base na sua escolha da representação.

   ![](assets/image-preset-previewrenditionthumbnail.png)

## Aplicar predefinições de imagens ao baixar imagens {#apply-image-presets-when-downloading-images}

Ao baixar imagens e suas representações do Brand Portal, não é possível escolher entre as predefinições de imagens existentes. Entretanto, é possível personalizar as propriedades de predefinição de imagem com base nas quais você deseja reformatar as imagens.

1. Na interface do Brand Portal, execute um dos procedimentos a seguir:

   * Passe o ponteiro sobre a imagem que você deseja baixar. Nas miniaturas de ação rápida disponíveis, clique no botão **[!UICONTROL Baixar]** ícone.

   ![](assets/downloadsingleasset.png)

   * Selecione a imagem que deseja baixar. Na barra de ferramentas na parte superior, clique no botão **[!UICONTROL Baixar]** ícone.

   ![](assets/downloadassets.png)

1. No **[!UICONTROL Baixar]** , selecione as opções necessárias, dependendo se você deseja baixar o ativo com ou sem suas representações.

   ![](assets/donload-assets-dialog.png)

1. Para baixar representações dinâmicas do ativo, selecione a variável **[!UICONTROL Representação(ões) dinâmica(s)]** opção.
1. Personalize as propriedades da predefinição de imagem com base nas quais você deseja reformatar dinamicamente a imagem e suas representações durante o download. Especifique o tamanho, o formato, o espaço de cor, a resolução e o modificador da imagem.

   ![](assets/dynamicrenditions.png)

1. Clique em **[!UICONTROL Baixar]**. As representações dinâmicas personalizadas são baixadas em um arquivo ZIP juntamente com a imagem e as representações que você optou por baixar. No entanto, nenhum arquivo zip é criado se um único ativo for baixado, o que garante um download rápido.
