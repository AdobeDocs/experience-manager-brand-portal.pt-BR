---
title: Origem de ativos no Brand Portal
seo-title: Asset Sourcing in Brand Portal
description: Obtenha um insight sobre o recurso de origem de ativos lançado no Adobe Experience Manager Assets Brand Portal.
seo-description: Get an insight into the asset sourcing feature released in the Adobe Experience Manager Assets Brand Portal.
uuid: null
content-type: reference
contentOwner: Vishabh Gupta
topic-tags: brand-portal
products: SG_EXPERIENCEMANAGER/Brand_Portal
discoiquuid: null
sub-product: assets
topics: collaboration, content-velocity, sharing
doc-type: feature-video
activity: use
audience: author, marketer
version: 6.5
kt: 3838
exl-id: 2c132a7a-ed10-4856-8378-67939167ea60
source-git-commit: 955cd8afe939ff47e9f08f312505e230e2f38495
workflow-type: tm+mt
source-wordcount: '647'
ht-degree: 1%

---

# Visão geral da origem do ativo {#overview-asset-sourcing-in-bp}

A **Origem de ativos** permite que os usuários do Experience Manager Assets (administradores/usuários não administradores) criem novas pastas com uma propriedade adicional de **Contribuição de ativos**, garantindo que a nova pasta criada seja aberta para o envio de ativos pelos usuários do Brand Portal. Isso dispara automaticamente um fluxo de trabalho que cria duas subpastas adicionais, chamadas **COMPARTILHADAS** e **NOVAS**, na pasta **Contribuição** recém-criada. Em seguida, o administrador define o requisito carregando um resumo sobre os tipos de ativos que devem ser adicionados à pasta de contribuição, bem como um conjunto de ativos de linha de base, na pasta **SHARED** para garantir que os usuários do BP tenham as informações de referência de que precisam. O administrador pode conceder aos usuários ativos do Brand Portal acesso à pasta de contribuição antes de publicar a pasta **Contribuição** recém-criada na Brand Portal. Quando o usuário terminar de adicionar conteúdo à pasta **NEW**, ele poderá publicar a pasta de contribuição de volta no ambiente do autor do Experience Manager. Observe que pode levar alguns minutos para concluir a importação e refletir o conteúdo recém-publicado no Experience Manager Assets.

Além disso, toda a funcionalidade existente permanece inalterada. Os usuários do Brand Portal podem exibir, pesquisar e baixar ativos da pasta contribuição e de outras pastas permitidas. Além disso, os administradores podem compartilhar a pasta de contribuição, modificar propriedades e adicionar ativos a coleções.

![Origem de ativos do Brand Portal](assets/asset-sourcing.png)

>[!VIDEO](https://video.tv.adobe.com/v/29365/?quality=12)

## Pré-requisitos {#prerequisites}

* Experience Manager Assets as a Cloud Service, Experience Manager Assets 6.5.2 ou superior.
* Verifique se a instância do Experience Manager Assets está configurada com o Brand Portal. Consulte [Configurar Experience Manager Assets com Brand Portal](../using/configure-aem-assets-with-brand-portal.md).

<!--
* Ensure that your Brand Portal tenant is configured with one AEM Assets author instance.
-->

>[!NOTE]
>
>Por padrão, o recurso Origem de ativos está habilitado no Experience Manager Assets as a Cloud Service, Experience Manager Assets 6.5.9 e versões posteriores.
>
>As configurações existentes continuarão a funcionar nas versões anteriores.

>[!NOTE]
>
>Há um problema conhecido no Experience Manager Assets 6.5.4. Os usuários do Brand Portal não podem publicar ativos da pasta de contribuição para o Experience Manager Assets ao atualizar para o Adobe Developer Console.
>
>O problema é corrigido no Experience Manager Assets 6.5.5. Você pode atualizar sua instância do Experience Manager Assets para o service pack mais recente e [atualizar suas configurações](https://experienceleague.adobe.com/docs/experience-manager-65/assets/brandportal/configure-aem-assets-with-brand-portal.html?lang=pt-BR#upgrade-integration-65) no Adobe Developer Console.

<!--

>For immediate fix on AEM 6.5.4, it is recommended to [download the hotfix](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq650/hotfix/cq-6.5.0-hotfix-33041) and install on your author instance.
-->

<!--
## Configure Asset Sourcing {#configure-asset-sourcing}

**Asset Sourcing** is configured from within the AEM Assets author instance. The administrators can enable the Asset Sourcing feature flag configuration from the **AEM Web Console Configuration** and upload the active Brand Portal users list in **AEM Assets**.

>[!NOTE]
>
>Asset Sourcing is by default enabled on AEM Assets as a Cloud Service. The AEM administrator can directly upload the active Brand Portal users to allow them access to the Asset Sourcing feature.

>[!NOTE]
>
>Before you begin with the configuration, ensure that your AEM Assets instance is configured with Brand Portal. See, [Configure AEM Assets with Brand Portal](../using/configure-aem-assets-with-brand-portal.md). 

The following video demonstrates, how to configure Asset Sourcing on your AEM Assets author instance:

>[!VIDEO](https://video.tv.adobe.com/v/29771)
-->

<!--
### Enable Asset Sourcing {#enable-asset-sourcing}

AEM administrators can enable the Asset Sourcing feature flag from within the AEM Web Console Configuration (a.k.a Configuration Manager).

>[!NOTE]
>
>This step is not applicable for AEM Assets as a Cloud Service.


**To enable Asset Sourcing:**
1. Log in to your AEM Assets author instance and open Configuration Manager. 
Default URL: http:// localhost:4502/system/console/configMgr.
1. Search using the keyword **Asset Sourcing** to locate **[!UICONTROL Asset Sourcing Feature Flag Config]**.
1. Click **[!UICONTROL Asset Sourcing Feature Flag Config]** to open the configuration window.
1. Select the **[!UICONTROL feature.flag.active.status]** check box.
1. Click **[!UICONTROL Save]**.

![](assets/enable-asset-sourcing.png)
-->


### Fazer upload da lista de usuários do Brand Portal {#upload-bp-user-list}

Os administradores do Experience Manager Assets podem fazer upload do arquivo de configuração de usuário (.csv) do Brand Portal que contém a lista de usuários ativos do Brand Portal no Experience Manager Assets para permitir que eles acessem o recurso Origem de ativos.

Uma pasta de contribuição só pode ser compartilhada com os usuários ativos do Brand Portal definidos na lista de usuários. O administrador também pode adicionar novos usuários no arquivo de configuração e fazer upload da lista de usuários modificada.

>[!NOTE]
>
>Verifique se a instância do Experience Manager Assets está configurada com o Brand Portal. Consulte [Configurar Experience Manager Assets com Brand Portal](../using/configure-aem-assets-with-brand-portal.md).

>[!NOTE]
>
>O formato do arquivo CSV é igual ao formato compatível no Admin Console para importação de usuários em massa. Email, nome e sobrenome são obrigatórios.

Os administradores podem adicionar novos usuários ao Admin Console. Consulte [Gerenciar usuários](brand-portal-adding-users.md) para obter informações detalhadas. Depois de adicionar usuários ao Admin Console, esses usuários podem ser adicionados ao arquivo de configuração de usuário do Brand Portal e, em seguida, receber permissão para acessar a pasta de contribuição.

**Para carregar a lista de usuários do Brand Portal:**

1. Faça logon na sua instância do Experience Manager Assets.
1. No painel **Ferramentas**, navegue até **[!UICONTROL Assets]** > **[!UICONTROL Usuários do Brand Portal]**.

1. A janela Brand Portal Upload Contributors é aberta.
Procure no computador local e carregue o **arquivo de configuração (.csv)** contendo a lista de usuários ativos do Brand Portal.
1. Clique em **[!UICONTROL Salvar]**.

   ![](assets/upload-user-list2.png)


Os administradores podem fornecer acesso a usuários específicos nesta lista de usuários enquanto configuram uma pasta de contribuição. Somente os usuários atribuídos a uma pasta de contribuição terão acesso à pasta de contribuição e publicarão ativos do Brand Portal na Experience Manager Assets.

## Consulte também: {#reference-articles}

* [Configurar e publicar pasta de contribuição no Brand Portal](brand-portal-publish-contribution-folder-to-brand-portal.md)

* [Pasta de contribuição do Publish para o Experience Manager Assets](brand-portal-publish-contribution-folder-to-aem-assets.md)
