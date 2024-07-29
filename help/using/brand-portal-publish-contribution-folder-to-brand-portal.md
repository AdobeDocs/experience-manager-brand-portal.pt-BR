---
title: Configurar e publicar pasta de contribuição do Experience Manager Assets para o Brand Portal
description: Obtenha informações sobre como configurar e publicar uma pasta de contribuição do Experience Manager Assets para o Brand Portal.
content-type: reference
contentOwner: Vishabh Gupta
topic-tags: brand-portal
products: SG_EXPERIENCEMANAGER/Brand_Portal
exl-id: 9acad588-977a-45de-b544-f2cc8874ba12
source-git-commit: 9e51048d21c5b4a34696e668309657d2091a8b04
workflow-type: tm+mt
source-wordcount: '1033'
ht-degree: 0%

---

# Configurar pasta de contribuição no Experience Manager Assets {#configure-contribution-folder}

Para o fornecimento de ativos colaborativos, os usuários do Experience Manager Assets (administradores e usuários não administradores com permissão de acesso) podem criar pastas do tipo **Contribuição de ativos**, garantindo que a pasta criada esteja aberta para o envio de ativos por usuários do Brand Portal.  Este método aciona automaticamente um fluxo de trabalho que cria duas subpastas adicionais, chamadas **COMPARTILHADAS** e **NOVAS**, na pasta **Contribuição** recém-criada.

O usuário do Experience Manager Assets define os requisitos de ativos fazendo o upload de um resumo sobre os tipos de ativos que devem ser adicionados à pasta de contribuição. Eles também fazem upload de um conjunto de ativos da linha de base para a pasta COMPARTILHADO, garantindo que os usuários do Brand Portal tenham as informações necessárias. O administrador pode conceder aos usuários ativos do Brand Portal acesso à pasta de contribuição antes de publicar a pasta de contribuição recém-criada no Brand Portal.

O vídeo a seguir demonstra como configurar uma pasta de Contribuição no Experience Manager Assets:

>[!VIDEO](https://video.tv.adobe.com/v/30547)

O usuário do Experience Manager Assets executa as seguintes atividades ao configurar uma pasta de contribuição:

* [Criar uma pasta de contribuição](#create-contribution-folder)
* [Fazer upload de requisitos de ativos e atribuir colaboradores](#configure-contribution-folder-properties)
* [Fazer upload de ativos da linha de base](#uplad-new-assets-to-contribution-folder)
* [Pasta de contribuição do Publish do Experience Manager Assets para o Brand Portal](#publish-contribution-folder-to-brand-portal)

## Criar pasta de contribuição {#create-contribution-folder}

Administradores do Experience Manager Assets e usuários não administradores com permissão para criar uma nova pasta podem criar uma pasta de contribuição no Experience Manager Assets.
Para criar uma pasta de contribuição, crie uma pasta do tipo contribuição de ativo, garantindo que a pasta criada esteja aberta para o envio de ativos por usuários do Brand Portal. Esse método aciona automaticamente um fluxo de trabalho que cria duas subpastas adicionais, chamadas COMPARTILHADAS e NOVAS, na pasta de contribuição.

>[!NOTE]
>
>Os administradores podem criar várias pastas de contribuição de ativos em uma pasta.
>
>Uma pasta de contribuição de ativos contém as pastas NEW e SHARED para a distribuição e contribuição dos ativos. Não crie uma pasta de ativos ou de contribuições em uma pasta de contribuições.


É possível configurar as propriedades da pasta de contribuição separadamente, bem como ao criar a pasta de contribuição. Neste exemplo, as propriedades são configuradas separadamente.

**Para criar uma pasta de contribuição:**

1. Faça logon na sua instância do Experience Manager Assets.

1. Navegue até **[!UICONTROL Assets]** > **[!UICONTROL Arquivos]**. Ela lista todas as pastas existentes no repositório do Experience Manager Assets.

1. Clique em **[!UICONTROL Criar]** para criar uma nova pasta. A caixa de diálogo **[!UICONTROL Criar Pasta]** é aberta.

1. Insira o **[!UICONTROL Título]** e o **[!UICONTROL Nome]** da pasta e marque a caixa de seleção **[!UICONTROL Contribuição de ativos]**.
A Adobe recomenda que você use letras minúsculas sem nenhum espaço para nomear a pasta.

1. Clique em **[!UICONTROL Criar]**. Você pode ver a pasta de contribuição listada no repositório do Experience Manager Assets.

   >[!NOTE]
   >
   >Um usuário não administrador pode criar e compartilhar uma pasta de contribuição de ativos, mas não pode modificá-la ou excluí-la.


   ![](assets/create-contribution-folder.png)

1. Abra a pasta contribuição. Você pode ver duas subpastas-**[!UICONTROL SHARED]** e **[!UICONTROL NEW]**- que são criadas automaticamente dentro da pasta de contribuição.

   ![](assets/contribution-folder.png)


## Configurar propriedades da pasta de contribuição {#configure-contribution-folder-properties}

O administrador do Experience Manager Assets executa as seguintes atividades ao configurar as propriedades de uma pasta de contribuição.

* **Adicionar descrição**: forneça uma descrição de alto nível da pasta de contribuição.
* **Carregar resumo**: carregue um documento de requisito de ativo contendo informações relacionadas ao ativo.
* **Adicionar colaboradores**: adicione usuários do Brand Portal para conceder a eles acesso à pasta de contribuição.

O requisito de ativo refere-se aos detalhes fornecidos pelos administradores para ajudar os contribuidores (usuários do Brand Portal) a entender a necessidade e os requisitos da pasta de contribuição. O administrador carrega um documento de requisitos de ativos detalhando os tipos de ativos para a pasta de contribuição, incluindo finalidade, tipos de imagem e tamanho máximo.

**Para configurar as propriedades da pasta de contribuição:**

1. Faça logon na sua instância do Experience Manager Assets.

1. Navegue até **[!UICONTROL Assets > Arquivos]** e localize a pasta de contribuição.
1. Selecione a pasta de contribuição e clique em **[!UICONTROL Propriedades]** para abrir a janela Propriedades da pasta.

   ![](assets/properties.png)

   ![](assets/contribution-folder-property1.png)

1. Navegue até a guia **[!UICONTROL Contribuição de ativos]**.
1. Insira uma **[!UICONTROL Descrição]** de alto nível da pasta de contribuição.
1. Clique em **[!UICONTROL Carregar resumo]** para procurar no computador local e carregar um **Documento de requisitos de ativos**.

   ![](assets/upload.png)

1. No campo **[!UICONTROL Adicionar usuário]**, adicione usuários do Brand Portal com os quais deseja compartilhar a pasta de contribuição. Esses usuários podem acessar e fazer upload de conteúdo para a pasta de contribuição usando a interface do Brand Portal.
1. Clique em **[!UICONTROL Salvar]**.

   ![](assets/contribution-folder-property3.png)

>[!NOTE]
>
>Os resultados da pesquisa se baseiam na lista de usuários do Brand Portal configurada no Experience Manager Assets. Verifique se você tem a lista de usuários atualizada do Brand Portal.

Os administradores podem baixar o arquivo `user.csv` de [!DNL Admin Console] e usá-lo como modelo base para adicionar usuários do Brand Portal. Vá para [!UICONTROL Usuários] e clique na opção [!UICONTROL Exportar lista de usuários para csv] para baixar o arquivo `users.csv`. A lista de usuários de amostra a seguir detalha os atributos necessários para adicionar os usuários. O único atributo obrigatório para uma entrada de usuário é o `Email` e todos os outros atributos são opcionais.

[Obter arquivo](assets/users.csv)

## Fazer upload de ativos para a pasta de contribuição {#uplad-new-assets-to-contribution-folder}

O usuário do Experience Manager Assets carrega um conjunto de ativos da linha de base na pasta **SHARED** para garantir que os usuários do Brand Portal tenham as informações necessárias.

**Para carregar ativos de linha de base:**

1. Faça logon na sua instância do Experience Manager Assets.

1. Navegue até **[!UICONTROL Assets > Arquivos]** e localize a pasta de contribuição.

1. Selecione a pasta de contribuição e clique em para abri-la.

1. Clique na pasta **[!UICONTROL NOVO]**.

   ![](assets/upload-new-assets1.png)

1. Clique em **[!UICONTROL Criar]** > **[!UICONTROL Arquivos]** para carregar arquivos individuais ou pastas (.zip) contendo vários ativos.

   ![](assets/upload-new-assets2.png)

1. Procure e carregue ativos (arquivos ou pastas) na pasta **[!UICONTROL NOVO]**.

   ![](assets/upload-asset4.png)

Depois de fazer upload de todos os ativos ou pastas para a NOVA pasta, publique a pasta de contribuição para o Experience Manager Assets.


## Pasta de contribuição do Publish para o Brand Portal {#publish-contribution-folder-to-brand-portal}

Depois que a pasta de contribuição é configurada, o usuário do Experience Manager Assets (administrador/usuário não administrador) pode publicar a pasta de contribuição do Experience Manager Assets para o Brand Portal. Os usuários do Brand Portal que têm permissão para acessar a pasta de contribuição recebem uma notificação por email ou por pulso após a conclusão da ação de publicação.


**Para publicar uma pasta de contribuição:**

1. Faça logon na sua instância do Experience Manager Assets.

1. Navegue até **[!UICONTROL Assets > Arquivos]** e localize a pasta de contribuição na qual você deseja publicar no Brand Portal.
1. Selecione uma pasta de contribuição e clique em **[!UICONTROL Quick Publish]** > **[!UICONTROL Publish to Brand Portal]**.

   ![](assets/publish-contribution-folder-to-bp.png)

   Você receberá uma mensagem de sucesso depois que a pasta de contribuição for publicada no Brand Portal.

Uma notificação por email/pulso é enviada aos usuários do Brand Portal atribuídos à pasta de contribuição. Os usuários do Brand Portal podem acessar a pasta contribuição e iniciar uma contribuição. Consulte [Carregar ativos para a pasta de contribuição e publicar no Experience Manager Assets](brand-portal-publish-contribution-folder-to-aem-assets.md).
