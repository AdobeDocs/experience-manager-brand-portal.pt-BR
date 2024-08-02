---
title: Usar o formulário de esquema de metadados
description: Um esquema de metadados descreve o layout da página Propriedades e as propriedades de metadados exibidas para ativos que usam o esquema específico. O esquema aplicado a um ativo determina os campos de metadados que aparecem na página Propriedades.
content-type: reference
products: SG_EXPERIENCEMANAGER/Brand_Portal
topic-tags: administration
role: Admin
exl-id: fbedff90-a6cb-4175-8308-817cc9f5b450
source-git-commit: 32a67abf466dd3bf635b851b02377ed23591915e
workflow-type: tm+mt
source-wordcount: '1622'
ht-degree: 5%

---

# Usar o formulário de esquema de metadados {#use-the-metadata-schema-form}

Um esquema de metadados descreve o layout da página Propriedades e as propriedades de metadados exibidas para ativos que usam o esquema específico. O esquema aplicado a um ativo determina os campos de metadados que aparecem na página Propriedades.

A página **[!UICONTROL Propriedades]** de cada ativo inclui propriedades de metadados padrão, dependendo do tipo MIME do ativo. Os administradores podem usar o Editor de esquema de metadados para modificar esquemas existentes ou adicionar esquemas de metadados personalizados. O Experience Manager Assets Brand Portal fornece formulários padrão para ativos de vários tipos MIME. No entanto, também é possível adicionar formulários personalizados para esses ativos.

## Adicionar um formulário de esquema de metadados {#add-a-metadata-schema-form}

Para criar um novo formulário de esquema de metadados, faça o seguinte:

1. Na barra de ferramentas na parte superior, clique no logotipo do Experience Manager para acessar as ferramentas administrativas.

   ![](assets/aemlogo.png)

1. No painel de ferramentas administrativas, clique em **[!UICONTROL Esquemas de metadados]**.

   ![](assets/navigation-panel.png)

1. Na página **[!UICONTROL Forms de esquema de metadados]**, clique em **[!UICONTROL Criar]**.

   ![](assets/create-metadata-schema-form.png)

1. Na caixa de diálogo **[!UICONTROL Criar Formulário de Esquema]**, especifique o título do formulário de Esquema e clique em **[!UICONTROL Criar]** para concluir o processo de criação do formulário.

   ![](assets/create-schema-form.png)

## Editar um formulário de esquema de metadados {#edit-a-metadata-schema-form}

Qualquer formulário de esquema de metadados adicionado ou existente pode ser editado. O formulário de esquema de metadados contém conteúdo derivado de seu pai, incluindo guias e itens de formulário dentro de guias. Você pode mapear ou configurar esses itens de formulário para um campo em um nó de metadados.

Você pode adicionar novas guias ou itens de formulário ao formulário de esquema de metadados. As guias e os itens de formulário derivados (do pai) estão no estado bloqueado. Não é possível alterá-los no nível secundário.

Para editar um formulário de esquema de metadados, faça o seguinte:

1. Na barra de ferramentas na parte superior, clique no logotipo do Experience Manager para acessar as ferramentas administrativas.

   ![](assets/aemlogo.png)

1. No painel de ferramentas administrativas, clique em **[!UICONTROL Esquemas de metadados]**.
1. Na página **[!UICONTROL Forms de esquema de metadados]**, selecione um formulário de esquema para editar suas propriedades, por exemplo, **[!UICONTROL coleção]**.

   ![](assets/metadata-schema-forms.png)

   >[!NOTE]
   >
   >Modelos não editados exibem um símbolo de bloqueio antes deles. Se você personalizar qualquer um dos modelos, o símbolo Bloquear antes que o modelo desapareça.

1. Na barra de ferramentas na parte superior, clique em **[!UICONTROL Editar]**.

   A página **[!UICONTROL Editor de Esquema de Metadados]** é aberta com a guia **[!UICONTROL Básico]** aberta à esquerda. À direita, a guia **[!UICONTROL Criar Formulário]** está aberta.

1. Na página **[!UICONTROL Editor de esquema de metadados]**, personalize a página **[!UICONTROL Propriedades]** do ativo. Basta arrastar um ou mais componentes de uma lista de tipos de componentes na guia **[!UICONTROL Criar Formulário]**. Arraste-os para a guia **[!UICONTROL Básico]**.

   ![](assets/metadata-schemaeditor-page.png)

1. Para configurar um componente, selecione-o e modifique suas propriedades na guia **[!UICONTROL Configurações]**.

### Componentes na guia Criar formulário {#components-in-the-build-form-tab}

A guia **[!UICONTROL Criar Formulário]** lista itens que você pode usar no formulário de esquema. A guia **[!UICONTROL Configurações]** fornece os atributos de cada item selecionado na guia **[!UICONTROL Formulário de compilação]**. A tabela a seguir lista os itens de formulário disponíveis na guia **[!UICONTROL Criar Formulário]**:

| Nome do componente | Descrição |
|---------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **[!UICONTROL Cabeçalho da seção]** | Adicione um cabeçalho de seção para obter uma lista de componentes comuns. |
| **[!UICONTROL Texto em linha única]** | Adicione uma propriedade de texto de linha única. Ele é armazenado como uma string. |
| **[!UICONTROL TextoDeVáriosValores]** | Adicione uma propriedade de texto de vários valores. Ele é armazenado como uma matriz de sequência. |
| **[!UICONTROL Número]** | Adiciona um componente de número. |
| **[!UICONTROL Data]** | Adiciona um componente de data. |
| **[!UICONTROL Lista suspensa]** | Adicione uma lista suspensa. |
| **[!UICONTROL Marcas Padrão]** | Adicione uma tag. Talvez os administradores precisem alterar o valor do caminho. Por exemplo, `/etc/tags/mac/<tenant_id>/<custom_tag_namespace>`, se eles publicarem o formulário de esquema de metadados do Experience Manager Assets, onde o caminho não inclui informações do locatário, por exemplo, `/etc/tags/<custom_tag_namespace>`. |
| **[!UICONTROL Tags inteligentes]** | Tags detectadas automaticamente se você tiver comprado e configurado o complemento tags inteligentes da Experience Manager Assets. |
| **[!UICONTROL Campo oculto]** | Adicione um campo oculto. Ele é enviado como um parâmetro POST quando o ativo é salvo. |
| **[!UICONTROL Ativo Referenciado Por]** | Adicione este componente para exibir uma lista de ativos referenciados pelo ativo. |
| **[!UICONTROL Referenciando Ativo]** | Adicionar para exibir uma lista de ativos que fazem referência ao ativo. |
| **[!UICONTROL Classificação de ativos]** | Classificação média de um ativo adicionado do Experience Manager Assets antes de ele ser publicado no Brand Portal. |
| **[!UICONTROL Metadados contextuais]** | Adicione para controlar a exibição de outras guias de metadados na página Propriedades dos ativos. |

>[!NOTE]
>
>Não use as **[!UICONTROL Referências do produto]**, pois elas não são funcionais.

#### Editar o componente de metadados {#edit-the-metadata-component}

Para editar as propriedades de um componente de metadados no formulário, clique no componente e edite suas propriedades na guia **[!UICONTROL Configurações]**.

* **[!UICONTROL Rótulo do campo]**: o nome da propriedade de metadados que é exibida na página Propriedades do ativo.

* **[!UICONTROL Mapear para a Propriedade]**: o valor dessa propriedade fornece o caminho/nome relativo para o nó do ativo onde ele é salvo no repositório do CRX. Ele começa com &quot;**./**&quot; porque indica que o caminho está sob o nó do ativo.

A seguir estão os valores válidos para essa propriedade:

— `./jcr:content/metadata/dc:title`: armazena o valor no nó de metadados do ativo como a propriedade `dc:title`.

— `./jcr:created`: exibe a propriedade jcr no nó do ativo. Se você configurou essas propriedades nas propriedades de exibição, o Adobe recomenda que você as marque como Desativar edição, pois elas estão protegidas. Caso contrário, o erro &quot;Falha ao modificar o Assets&quot; ocorre ao salvar as propriedades do ativo.

* **[!UICONTROL Espaço reservado]**: use esta propriedade para fornecer ao usuário todas as informações relevantes sobre a propriedade de metadados.
* **[!UICONTROL Obrigatório]**: use esta propriedade para marcar uma propriedade de metadados como obrigatória na página Propriedades.
* **[!UICONTROL Desabilitar Edição]**: use essa propriedade para tornar uma propriedade de metadados não editável na página Propriedades.
* **[!UICONTROL Mostrar Campo Vazio em Somente Leitura]**: marque esta propriedade para exibir uma propriedade de metadados na página Propriedades, mesmo que ela não tenha valor. Por padrão, quando uma propriedade de metadados não tem valor, ela não é listada na página Propriedades.
* **[!UICONTROL Descrição]**: use essa propriedade para adicionar uma descrição curta para o componente de metadados.
* **[!UICONTROL Ícone Excluir]**: clique neste ícone para excluir um componente do formulário de esquema.

![](assets/delete_icon_editmetadataschemaform.png)

>[!NOTE]
>
>Todos os campos de metadados são somente leitura no formulário do editor de metadados de um ativo. Como os metadados do ativo devem ser editados no Experience Manager Assets antes que um ativo seja publicado no Brand Portal.

#### Adicionar ou excluir uma guia no formulário de esquema {#add-or-delete-a-tab-in-the-schema-form}

O formulário de esquema padrão inclui as guias **[!UICONTROL Básico]** e **[!UICONTROL Avançado]**. O editor de esquema permite adicionar ou excluir uma guia.

![](assets/add_delete_tabs_metadataschemaform.png)

* Para adicionar uma nova guia em um formulário de esquema, clique em **[!UICONTROL +]**. Por padrão, a nova guia tem o nome &quot;Sem nome-1&quot;. Você pode modificar o nome na guia **[!UICONTROL Configurações]**.

![](assets/add-tab-metadata-form.png)

* Para excluir uma guia, clique em **[!UICONTROL x]**. Clique em **[!UICONTROL Salvar]** para salvar as alterações.

## Aplicar um esquema de metadados a uma pasta {#apply-a-metadata-schema-to-a-folder}

O Brand Portal permite personalizar e controlar o esquema de metadados para que a página **[!UICONTROL Propriedades]** de um ativo exiba apenas as informações específicas que você escolher revelar. Para controlar os metadados exibidos na página **[!UICONTROL Propriedades]**, remova os metadados necessários do formulário de esquema de metadados e aplique-os à pasta específica.

Para aplicar um formulário de esquema de metadados a uma pasta, faça o seguinte:

1. Na barra de ferramentas na parte superior, clique no logotipo do Experience Manager para acessar as ferramentas administrativas.

   ![](assets/aemlogo.png)

1. No painel de ferramentas administrativas, clique em **[!UICONTROL Esquemas de metadados]**.

1. Na página **[!UICONTROL Forms de esquema de metadados]**, selecione o formulário de esquema que deseja aplicar a um ativo, por exemplo, **[!UICONTROL roupas]**.

   ![](assets/apply-metadata-schema-form-to-folder.png)

1. Na barra de ferramentas na parte superior, clique em **[!UICONTROL Aplicar às Pastas]**.

1. Na página **[!UICONTROL Selecionar Pastas]**, navegue até a pasta à qual deseja aplicar o esquema de metadados **[!UICONTROL roupas]**, por exemplo, **[!UICONTROL Luvas]**.

   ![](assets/apply_metadata_schemaformtofoldergloves.png)

1. Clique em **[!UICONTROL Aplicar]** para aplicar o formulário de esquema de metadados à pasta.

   Os metadados disponíveis no formulário de esquema de metadados **[!UICONTROL roupas]** são aplicados à pasta **[!UICONTROL Luvas]** e estão visíveis na página **[!UICONTROL Propriedades]** da pasta.

   ![](assets/folder_metadata_properties.png)

>[!NOTE]
>
>Se você aplicar um esquema que inclui esquemas aninhados a uma pasta contendo arquivos de vídeo, as propriedades de metadados dos arquivos de vídeo podem não ser renderizadas corretamente. Para garantir que as propriedades de metadados sejam renderizadas corretamente, remova os esquemas aninhados e aplique somente o esquema principal à pasta.

## Excluir um formulário de esquema de metadados {#delete-a-metadata-schema-form}

O Brand Portal permite excluir somente formulários de esquema personalizados. Isso não permite excluir os formulários/modelos de esquema padrão. No entanto, você pode excluir qualquer alteração personalizada nesses formulários.

Para excluir um formulário, selecione-o e clique no ícone **[!UICONTROL Excluir]**.

![](assets/delete_icon_metadataschemaeditorform.png)

>[!NOTE]
>
>Depois de excluir as alterações personalizadas feitas em um formulário padrão, o símbolo **[!UICONTROL Bloquear]** reaparece antes do nome do formulário na interface do Esquema de Metadados para indicar que o formulário está revertido para seu estado padrão.

## Formulários de esquema para TIPOS MIME {#schema-forms-for-mime-types}

### Adição de novos formulários para tipos MIME {#adding-new-forms-for-mime-types}

Além dos formulários padrão, é possível adicionar formulários personalizados para ativos de vários tipos MIME ou criar um novo formulário em um tipo de formulário apropriado. Por exemplo, para adicionar um novo modelo para o subtipo **[!UICONTROL image/png]**, crie o formulário nos formulários &quot;image&quot;. O título do formulário de esquema é o nome do subtipo. Nesse caso, o título é &quot;png&quot;.

#### Uso de um modelo de esquema existente para vários tipos MIME {#using-an-existing-schema-template-for-various-mime-types}

Você pode usar um modelo existente para um tipo MIME diferente. Por exemplo, use o formulário **image/jpeg** para ativos do tipo MIME **image/png**.

Nesse caso, crie um novo nó em [!UICONTROL `/etc/dam/metadataeditor/mimetypemappings`] no repositório do CRX. Especifique um nome para o nó e defina as seguintes propriedades:

| **Nome** | **Tipo** | **Valor** |
|---|---|---|
| exposedmimetype | String | image/jpeg |
| tipos mime | Cadeia de caracteres[] | image/png |

* **exposedmimetype**: nome do formulário existente a ser mapeado
* **tipos MIME**: lista de tipos MIME que usam o formulário definido no atributo **exposedmimetype**

O Brand Portal mapeia os seguintes tipos MIME e formulários de esquema:

| **Formulário de esquema** | **Tipos MIME** |
|---|---|
| image/jpeg | image/pjpeg |
| image/tiff | image/x-tiff |
| application/pdf | application/postscript |
| application/x-ImageSet | Multipart/Related; type=application/x-ImageSet |
| application/x-SpinSet | Multipart/Related; type=application/x-SpinSet |
| application/x-MixedMediaSet | Multipart/Related; type=application/x-MixedMediaSet |
| video/quicktime | video/x-quicktime |
| video/mpeg4 | video/mp4 |
| video/avi | video/avi, video/msvideo, video/x-msvideo |
| video/wmv | `video/x-ms-wmv` |
| video/flv | video/x-flv |

Esta é uma lista de propriedades de metadados padrão:

* `jcr:content/metadata/cq:tags`
* `jcr:content/metadata/dc:format`
* `jcr:content/metadata/dam:status`
* `jcr:content/metadata/videoCodec`
* `jcr:content/metadata/audioCodec`
* `jcr:content/metadata/dc:title`
* `jcr:content/metadata/dc:description`
* `jcr:content/metadata/xmpMM:InstanceID`
* `jcr:content/metadata/xmpMM:DocumentID`
* `jcr:content/metadata/dam:sha1`
* `jcr:content/metadata/dam:solutionContext`
* `jcr:content/metadata/videoBitrate`
* `jcr:content/metadata/audioBitrate`
* `jcr:content/usages/usedBy`
* `jcr:content/jcr:lastModified`
* `jcr:content/metadata/prism:expirationDate`
* `jcr:content/onTime`
* `jcr:content/offTime`
* `jcr:content/metadata/dam:size`
* `jcr:content/metadata/tiff:ImageWidth`
* `jcr:content/metadata/tiff:ImageLength`
