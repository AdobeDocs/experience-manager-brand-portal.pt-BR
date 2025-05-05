---
title: Baixar ativos
description: Todos os usuários podem baixar ativos e pastas acessíveis ao mesmo tempo, garantindo que os ativos de marca aprovados sejam distribuídos com segurança para uso offline.
content-type: reference
contentOwner: Vishabh Gupta
products: SG_EXPERIENCEMANAGER/Brand_Portal
topic-tags: download, download-install, download assets
exl-id: be264b1c-38d9-4075-b56a-113f34a2c6bf
source-git-commit: f483ac280a5e89ca25305eae09380d70ad661752
workflow-type: tm+mt
source-wordcount: '1909'
ht-degree: 5%

---

# Baixar ativos {#download-assets-from-bp}

O Adobe Experience Manager Assets Brand Portal melhora a experiência de download ao permitir que os usuários baixem simultaneamente ativos e pastas acessíveis a eles do Brand Portal. Este método significa que os recursos de marca aprovados podem ser distribuídos com segurança para uso offline. Leia para saber como baixar ativos (ativos aprovados) da Brand Portal e o que esperar do [desempenho de download](#expected-download-performance).


>[!NOTE]
>
>No Brand Portal 2020.10.0 (e posterior), a configuração **[!UICONTROL Download Rápido]** está habilitada por padrão, que usa o IBM® Aspera Connect para acelerar o download dos ativos. Instale o IBM® Aspera Connect 3.9.9 (`https://www.ibm.com/docs/en/aspera-connect/3.9.9`) na extensão de seu navegador antes de baixar os ativos da Brand Portal. Consulte o [guia para acelerar downloads do Brand Portal](../using/accelerated-download.md).
>
>Se você não quiser usar o IBM® Aspera Connect e continuar com o processo normal de download, contate o administrador do Brand Portal para desativar a configuração **[!UICONTROL Download Rápido]**.

## Configurar o download de ativos {#configure-download}

Os administradores do Brand Portal podem definir o download de ativos e as configurações de grupo de usuários para usuários do Brand Portal. Esse recurso permite que os usuários acessem e baixem representações de ativos na interface da Brand Portal.

>[!NOTE]
>
>As configurações de download na interface do usuário fornecem uma experiência de autoatendimento para usuários do Brand Portal, permitindo que eles configurem e baixem representações de ativos facilmente. Isso não restringe o download de ativos na camada do aplicativo. Por exemplo, os usuários ainda podem acessar e baixar representações de ativos com o caminho completo do URL.

As seguintes configurações definem como você acessa e baixa as representações de ativos na interface da Brand Portal:

* Ativar configurações de download
* Definir configurações do grupo de usuários

### Ativar configurações de download {#enable-download-settings}

Os administradores podem habilitar as **[!UICONTROL Configurações de Download]** para definir o conjunto de representações acessível aos usuários do Brand Portal para download.

As configurações disponíveis são:

* **[!UICONTROL Download Rápido]**

  Ele fornece download acelerado dos recursos usando o IBM® Aspera Connect. Por padrão, a configuração **[!UICONTROL Download Rápido]** está habilitada nas **[!UICONTROL Configurações de Download]**.

* **[!UICONTROL Representações Personalizadas]**

  Permite o download de representações personalizadas e (ou) dinâmicas dos ativos.

  Todas as representações de ativos que não sejam o ativo original e as representações geradas pelo sistema são chamadas de representações personalizadas. Inclui representações estáticas e dinâmicas disponíveis para o ativo. Qualquer usuário pode criar uma representação estática personalizada no Experience Manager Assets, enquanto apenas o administrador pode criar representações dinâmicas personalizadas. Consulte [como aplicar predefinições de imagem ou representações dinâmicas](../using/brand-portal-image-presets.md).

* **[!UICONTROL Representações do Sistema]**

  Permite o download de representações geradas pelo sistema dos ativos.

  Esses ativos são miniaturas geradas automaticamente no Experience Manager Assets com base no fluxo de trabalho &quot;Atualizar ativo DAM&quot;.

* **[!UICONTROL Download de ativos]**

  As representações são baixadas em pastas separadas para cada ativo. Essa configuração se aplica a pastas, coleções e downloads em massa de mais de 20 ativos.


Faça logon no seu locatário do Brand Portal como administrador e navegue até **[!UICONTROL Ferramentas]** > **[!UICONTROL Download]**.

Os administradores podem ativar qualquer combinação de configurações para que os usuários do Brand Portal acessem e baixem representações de ativos.

![](assets/download-settings-new.png)


>[!NOTE]
>
>Somente os administradores podem baixar os ativos expirados. Para obter mais informações sobre ativos expirados, consulte [gerenciar direitos digitais de ativos](../using/manage-digital-rights-of-assets.md).

### Definir configurações do grupo de usuários {#configure-user-group-settings}

Além das **[!UICONTROL Configurações de Download]**, os administradores do Brand Portal podem definir configurações adicionais para diferentes grupos de usuários para exibir e (ou) baixar os ativos originais e suas representações.

Faça logon no seu locatário do Brand Portal como administrador e navegue até **[!UICONTROL Ferramentas]** > **[!UICONTROL Usuários]**. Na página **[!UICONTROL Funções de usuário]**, navegue até a guia **[!UICONTROL Grupos]** para definir as configurações de exibição e/ou download para os grupos de usuários.

![view-download-permission](assets/download-permissions.png)

>[!NOTE]
>
>Se um usuário for adicionado a vários grupos e se um desses grupos tiver restrições, as restrições se aplicam ao usuário.

Com base na configuração, o fluxo de trabalho de download permanece constante para ativos independentes, vários ativos, pastas que contêm ativos, ativos licenciados ou não licenciados e o download de ativos usando o link de compartilhamento.

A matriz a seguir define se um usuário terá acesso às representações dependendo das [configurações de download](#configure-download):

| **Configurações de Download: Representações Personalizadas** | **Configurações de Download: Representações do Sistema** | **Configurações do Grupo de Usuários: Baixar Original** | **Configurações do Grupo de Usuários: Baixar Representações** | **Resultado** |
|---|---|---|---|---|
| LIGADO | LIGADO | LIGADO | LIGADO | Exibir e baixar todas as representações |
| LIGADO | LIGADO | DESLIGADO | DESLIGADO | Exibir ativo original |
| DESLIGADO | DESLIGADO | LIGADO | LIGADO | Exibir e baixar o ativo original |
| LIGADO | DESLIGADO | LIGADO | LIGADO | Exibir e baixar o ativo original e as representações personalizadas |
| DESLIGADO | LIGADO | LIGADO | LIGADO | Exibir e baixar representações do ativo e do sistema originais |
| LIGADO | DESLIGADO | DESLIGADO | DESLIGADO | Exibir ativo original |
| DESLIGADO | LIGADO | DESLIGADO | DESLIGADO | Exibir ativo original |
| DESLIGADO | DESLIGADO | DESLIGADO | LIGADO | Exibir ativo original |
| DESLIGADO | DESLIGADO | LIGADO | DESLIGADO | Exibir e baixar o ativo original |
| DESLIGADO | DESLIGADO | DESLIGADO | DESLIGADO | Exibir ativo original |



## Baixar ativos {#download-assets}

Os usuários do Brand Portal podem baixar vários ativos, pastas contendo ativos e coleções na interface da Brand Portal.

>[!NOTE]
>
>Entre em contato com o administrador do Brand Portal se não tiver permissão para acessar ou baixar as representações do ativo.

Se o usuário tiver acesso às representações, ele receberá a caixa de diálogo **[!UICONTROL Download]** aprimorada com os seguintes recursos:

* Visualize todas as representações disponíveis de qualquer ativo na lista de downloads.
* Exclua representações de ativos que não são necessários para o download.
* Aplique o mesmo conjunto de representações a todos os tipos de ativos semelhantes com um só clique.
* Aplique um conjunto diferente de representações para tipos de ativos diferentes.
* Crie uma pasta separada para cada ativo.
* Baixar ativos selecionados e suas representações.

![caixa de diálogo de download](assets/download-dialog-box.png)

>[!NOTE]
>
>A caixa de diálogo **[!UICONTROL Download]** será exibida somente se **[!UICONTROL Representações Personalizadas]** e (ou) **[!UICONTROL Representações do Sistema]** estiverem habilitadas nas **[!UICONTROL Configurações de Download]**.


### Etapas para baixar ativos {#bulk-download}

Veja a seguir as etapas para baixar ativos ou pastas que contêm ativos na interface do Brand Portal:

1. Faça logon no seu locatário do Brand Portal. Por padrão, a exibição **[!UICONTROL Arquivos]** é aberta, contendo todos os ativos e pastas publicados.

   Siga uma das seguintes opções:

   * Selecione os ativos ou pastas que deseja baixar. Na barra de ferramentas na parte superior, clique no ícone **[!UICONTROL Download]**.

     ![selecionar vários ativos](assets/select-assets-new.png)

   * Para baixar representações de ativos específicas de um ativo, passe o ponteiro sobre o ativo e clique no ícone **[!UICONTROL Download]** disponível nas miniaturas de ação rápida.

     ![selecionar-ativo](assets/select-asset.png)


     >[!NOTE]
     >
     >Se você estiver baixando os ativos pela primeira vez e não tiver o IBM® Aspera Connect instalado no navegador, ele solicitará que você instale o acelerador de download Aspera (`https://www.ibm.com/docs/en/aspera-connect/3.9.9`).


     >[!NOTE]
     >
     >Se os ativos baixados também incluírem ativos licenciados, você será redirecionado para a página **[!UICONTROL Gerenciamento de Copyright]**. Nesta página, selecione os ativos, clique em **[!UICONTROL Concordar]** e em **[!UICONTROL Baixar]**. Se você optar por discordar, os ativos licenciados não serão baixados.
     > 
     >Os ativos protegidos por licença têm um [contrato de licença anexado](https://experienceleague.adobe.com/pt-br/docs/experience-manager-65/content/assets/administer/drm) a eles, o que é feito com a configuração da [propriedade de metadados](https://experienceleague.adobe.com/pt-br/docs/experience-manager-65/content/assets/administer/drm) do ativo no Experience Manager Assets.


     ![ativo licenciado](assets/licensed-asset-new.png)

1. A caixa de diálogo **[!UICONTROL Download]** listando todos os ativos selecionados é aberta.

   Clique em qualquer ativo para exibir as representações disponíveis e marque as caixas de seleção correspondentes às representações que deseja baixar.

   Você pode selecionar ou excluir manualmente as representações de ativos individuais ou clicar no ícone **Aplicar** para selecionar o mesmo conjunto de representações para baixar para tipos de ativos semelhantes (todos os arquivos de imagem neste exemplo). Na caixa de diálogo **[!UICONTROL Aplicar tudo]**, clique em **[!UICONTROL Concluído]** para aplicar a regra a todos os ativos semelhantes.

   ![aplicar-tudo](assets/apply.png)

   Você também pode remover um ativo da lista de download (se necessário) clicando no ícone **Remover**.

   ![remover](assets/remove.png)

   Para manter a estrutura de pastas do Brand Portal ao baixar ativos, marque a caixa de seleção **[!UICONTROL `Create separate folder for each asset`]**.

   O botão de download reflete a contagem dos itens selecionados. Quando terminar de aplicar as regras, clique em **[!UICONTROL Baixar itens]**.

   ![caixa de diálogo de download](assets/download-dialog-box-new.png)

1. Por padrão, a configuração **[!UICONTROL Download Rápido]** está habilitada nas **[!UICONTROL Configurações de Download]**. Portanto, aparece uma caixa de confirmação para permitir o download acelerado usando o IBM® Aspera Connect.

   Para continuar usando o **[!UICONTROL Download Rápido]**, clique em **[!UICONTROL Permitir]**. Todas as representações selecionadas são baixadas em uma pasta zip usando o IBM® Aspera Connect.

   Se não quiser usar o IBM® Aspera Connect, clique em **[!UICONTROL Negar]**. Se o **[!UICONTROL Download Rápido]** for negado ou falhar, o sistema preencherá uma mensagem de Erro. Clique no botão **[!UICONTROL Download Normal]** para continuar baixando os ativos.

<!-- removed the known issue from step 2 as it is fixed in 2022.02.0 release.
   >[!CAUTION]
   >
   >(**Experience Manager Assets as a Cloud Service** only) The following known issue will be fixed in the upcoming release:
   >
   >The download dialog lists the smart crop renditions of the selected asset, however, the user cannot download the smart crop renditions.
-->

>[!NOTE]
>
>Se a configuração **[!UICONTROL Download Rápido]** for desativada pelo administrador, as representações selecionadas serão baixadas diretamente em uma pasta zip sem usar o IBM® Aspera Connect.

>[!NOTE]
>
>Se a configuração **[!UICONTROL Download de ativos]** estiver habilitada nas **[!UICONTROL Configurações de Download]**, as representações de ativos serão baixadas em uma pasta separada para cada ativo dentro da pasta zip.
>  
>Se o download dos ativos for feito a partir de um link compartilhado, as representações do ativo serão baixadas em uma pasta separada para cada ativo dentro da pasta zip.
>
>Quando você seleciona uma pasta, coleção ou mais de 20 ativos para download, a caixa de diálogo **[!UICONTROL Download]** é ignorada. Em vez disso, todas as representações de ativos acessíveis, exceto as representações dinâmicas, são baixadas em uma pasta zip.

>[!NOTE]
>
>O Brand Portal é compatível com a configuração do Dynamic Media nos modos Híbrido e Scene7.
>
>(*Se a instância do autor do Experience Manager Assets estiver em execução no **Modo Híbrido do Dynamic Media***)
>
>Para visualizar ou baixar representações dinâmicas, ative a mídia dinâmica. Verifique se a representação TIFF da Pirâmide do ativo existe na instância do autor do Experience Manager Assets em que os ativos foram publicados. Quando um ativo é publicado do Experience Manager Assets para o Brand Portal, sua representação em Pyramid tiff também é publicada.

Se o [administrador não tiver autorizado você a acessar as representações originais](../using/brand-portal-adding-users.md#main-pars-procedure-202029708), você não poderá baixar as representações originais dos ativos selecionados.

![mensagem-sem-acesso](assets/no-access-message.png)

<!-- This issue has been resolved, check with engineering.
>[!NOTE]
>
>Once you have downloaded the asset renditions, the **[!UICONTROL Download]** button is disabled to avoid creating duplicate copies of the renditions. To download more (missing or another copy of renditions), refresh the browser to re-enable the download button.
-->

### Baixar ativos na página de detalhes do ativo {#download-assets-from-asset-details-page}

Além do fluxo de trabalho de download, há outro método para baixar as representações de ativos individuais diretamente da página de detalhes do ativo.

Os usuários podem visualizar diferentes representações de ativos, selecionar representações específicas e baixar diretamente representações de ativos no painel **[!UICONTROL Representações]** na página de detalhes do ativo sem precisar abrir a caixa de diálogo **[!UICONTROL Download]**.


Veja a seguir as etapas para baixar representações de ativos na página de detalhes do ativo:

1. Faça logon no locatário do Brand Portal e clique no ativo para abrir a página de detalhes do ativo.
1. Clique no ícone de sobreposição à esquerda e, em seguida, clique em **[!UICONTROL Representações]**.

   ![navegação de representação](assets/rendition-navigation.png)

1. O painel **[!UICONTROL Representações]** lista todas as representações de ativos acessíveis com base nas [configurações de download](#configure-download) do ativo.

   Selecione representações específicas que você deseja baixar e clique em **[!UICONTROL Baixar itens]**.

   ![painel de representações](assets/renditions-panel.png)


1. Por padrão, a configuração **[!UICONTROL Download Rápido]** está habilitada nas **[!UICONTROL Configurações de Download]**. Portanto, aparece uma caixa de confirmação para permitir o download acelerado usando o IBM® Aspera Connect.

   Para continuar usando o **[!UICONTROL Download Rápido]**, clique em **[!UICONTROL Permitir]**. Todas as representações selecionadas são baixadas em uma pasta zip usando o IBM® Aspera Connect.

   Se você negar o uso do **[!UICONTROL Download Rápido]**, o sistema preencherá uma mensagem de Erro. Clique no botão **[!UICONTROL Download Normal]** para continuar baixando os ativos.

<!-- removed the known issue from step 3 as it is fixed in 2022.02.0 release.
   >[!CAUTION]
   >
   >(**Experience Manager Assets as a Cloud Service** only) The following known issues will be fixed in the upcoming release:
   >
   >The **[!UICONTROL Renditions]** panel does not list all the static renditions of the assets that are published to Brand Portal after December 16, 2021.
   >
   >The **[!UICONTROL Renditions]** panel lists the smart crop renditions of the asset, however, the user cannot preview or download the smart crop renditions.
-->

>[!NOTE]
>
>Se a configuração **[!UICONTROL Download Rápido]** for desativada pelo administrador, as representações selecionadas serão baixadas diretamente em uma pasta zip sem usar o IBM® Aspera Connect.


>[!NOTE]
>
>As Assets baixadas individualmente estão visíveis no relatório de download de ativos. No entanto, se uma pasta que contém ativos for baixada, a pasta e os ativos não serão exibidos no relatório de download de ativos.

<!--
>[!NOTE]
>
>Assets that are individually downloaded are visible in the assets download report. However, if a folder containing assets is downloaded, the folder and assets are not displayed in the assets download report.
-->

<!-- Backup of content before updating the new feature docs.
## Configure asset download {#configure-download}

The download configuration allows the Brand Portal administrators to define the set of renditions available to the Brand Portal users for downloading the assets. The administrator can configure the asset **[!UICONTROL Download]** settings from the Brand Portal interface. 

The available configurations are:

* **[!UICONTROL Fast Download]** 

  Enables high-speed download of the assets. To know more, see [guide to accelerate downloads from Brand Portal](../using/accelerated-download.md).

* **[!UICONTROL Custom Renditions]** 
  
  Download custom and (or) dynamic renditions of the assets. 
  All the asset renditions other than the original asset and system-generated renditions are called as custom renditions. It includes static as well as dynamic renditions available for the asset. Any user can create a custom static rendition in AEM Assets, whereas, only the AEM administrator can create custom dynamic renditions. To know more, see [how to apply image presets or dynamic renditions](../using/brand-portal-image-presets.md)

* **[!UICONTROL System Renditions]** 

  Download system-generated renditions of the assets. These are the thumbnails which are automatically generated in AEM Assets based on the "DAM update asset" workflow. 

Log in to your Brand Portal tenant as an administrator and navigate to **[!UICONTROL Tools]** > **[!UICONTROL Download]**. By default, the **[!UICONTROL Fast Download]** configuration is enabled in the **[!UICONTROL Download Settings]**. 

The administrators can enable any combination to configure the asset download process.

![](assets/download-configuration.png)


Based on the configuration, the download workflow remains constant for stand-alone assets, multiple assets, folders containing assets, licensed or unlicensed assets, and downloading assets using share link. 


* If both **[!UICONTROL Custom Renditions]** and **[!UICONTROL System Renditions]** configurations are turned-off, the original renditions of the assets are downloaded without any additional dialog being presented to the users.    


* If any of the **[!UICONTROL Custom Renditions]** or **[!UICONTROL System Renditions]** configuration is enabled, an additional **[!UICONTROL Download]** dialog box appears wherein you can choose whether to download the original asset along with its renditions, or download only specific renditions. 

>[!NOTE]
>
>Only the administrators can download the expired assets. For more information about expired assets, see [manage digital rights of assets](../using/manage-digital-rights-of-assets.md).

## Steps to download assets {#steps-to-download-assets}

Following are the steps to download assets or folders containing assets from Brand Portal:

1. From the Brand Portal interface, do one of the following:

   * Select the folders or assets you want to download. From the toolbar at the top, click the **[!UICONTROL Download]** icon.

     ![](assets/downloadassets-1.png)

   * To download a specific asset or folder, hover the pointer over the asset or folder and click the **[!UICONTROL Download]** icon available in the quick action thumbnails.

     ![](assets/downloadsingleasset-1.png)


     >[!NOTE]
     >
     >If you are downloading the assets for the first time and do not have IBM Aspera Connect installed in your browser, it will prompt you to install the Aspera download accelerator. 


     >[!NOTE]
     >
     >If the assets you are downloading also include licensed assets, you are redirected to the **[!UICONTROL Copyright Management]** page. In this page, select the assets, click **[!UICONTROL Agree]**, and then click **[!UICONTROL Download]**. If you choose to disagree, licensed assets are not downloaded. 
     > 
     >License-protected assets have [license agreement attached]() to them, which is done by setting asset's [metadata property]() in Experience Manager Assets.


     ![](assets/licensed-asset-download-1.png)

     
     >[!NOTE]
     >
     >Ensure to select all the required asset renditions while downloading them from the asset details page, and click **[!UICONTROL Download]**. The selected renditions are downloaded to your local machine.
     > 
     >Once you download, the **[!UICONTROL Download]** button is disabled to avoid creating duplicate copies of the downloaded renditions. To download more (missing or another copy of renditions), refresh the browser to re-enable the download button.

     If any of the **[!UICONTROL Custom Renditions]** or **[!UICONTROL System Renditions]** configuration is enabled in the **[!UICONTROL Download Settings]**, the **[!UICONTROL Download]** dialog appears with the **[!UICONTROL Asset(s)]** check box selected by default. If the **[!UICONTROL Fast Download]** configuration is enabled, the **[!UICONTROL Enable download acceleration]** check box is selected by default.

     ![](assets/download-dialog.png)

     >[!NOTE]
     >
     >If the downloading assets are image files, and you select only the **[!UICONTROL Asset(s)]** check box in the **[!UICONTROL Download]** dialog but are not [authorized by the administrator to have access to the original renditions of image files](../using/brand-portal-adding-users.md#main-pars-procedure-202029708) then no image files are downloaded and a notification appears, stating that you have been restricted by the administrator to access original renditions.

     ![](assets/restrictaccess-note.png)

1. To download the renditions in addition to the original assets, select the **[!UICONTROL Rendition(s)]** check box. However, if you want to download the system-generated renditions along with the custom renditions, clear the **[!UICONTROL Exclude System Renditions]** check box.

   ![](assets/download-system-rendition.png)

   * To download only the renditions, clear the **[!UICONTROL Asset(s)]** check box.

     >[!NOTE]
     >
     >By default, only the assets are downloaded. However, original renditions of image files are not downloaded if you are not [authorized by the administrator to have access to the original renditions of image files](../using/brand-portal-adding-users.md#main-pars-procedure-202029708).

    * To share the selected assets with other users through a link, select the **[!UICONTROL Email]** check box. An email notification is sent to the users with the download link. To know how to download assets from shared links, see [downloading assets from shared links](../using/brand-portal-link-share.md#main-pars-header-1703469193).  

      ![](assets/download-link.png)

      >[!NOTE]
      >
      >The download link on email notification expires after 45 days.
      >
      >The administrators can customize email messages, that is, logo, description, and footer, using the [Branding](../using/brand-portal-branding.md) feature.


    * You can select a predefined image preset or create a custom dynamic rendition from the **[!UICONTROL Download]** dialog box. 

      To apply a [custom image preset to the asset and its renditions](../using/brand-portal-image-presets.md#applyimagepresetswhendownloadingimages), select the **[!UICONTROL Dynamic Rendition(s)]** check box. Specify the image preset properties (such as size, format, color space, resolution, and image modifier) to apply the custom image preset while downloading the asset and its renditions. To download only the dynamic renditions, clear the **[!UICONTROL Asset(s)]** check box.

      ![](assets/dynamic-rendition.png)

      >[!NOTE]
      >
      >Brand Portal supports configuring Dynamic Media in both - Hybird and Scene 7 mode. 
      >
      >(*If AEM author instance is running on **Dynamic Media Hybrid mode***)
      >
      >To preview or download dynamic renditions of an asset, ensure that the dynamic media is enabled and the asset's Pyramid tiff rendition exists at the AEM Assets author instance from where the assets have been published. When an asset is published to Brand Portal, its Pyramid tiff rendition is also published.
      
  
    * To preserve the Brand Portal folder hierarchy while downloading assets, select the **[!UICONTROL Create separate folder for each asset]** check box. By default, the Brand Portal folder hierarchy is ignored and all the assets are downloaded in one folder in your local system.

1. Click **[!UICONTROL Download]**.

   The assets (and renditions if selected) are downloaded as a zip file to your local folder. However, no zip file is created if a single asset is downloaded without any of the renditions. 

   If you are not [authorized by the administrator to have access to the original renditions](../using/brand-portal-adding-users.md#main-pars-procedure-202029708), the original renditions of the selected assets are not downloaded. 

   >[!NOTE]
   >
   >Assets that are individually downloaded are visible in the assets download report. However, if a folder containing assets is downloaded, the folder and assets are not displayed in the assets download report.
-->

## Desempenho de download esperado {#expected-download-performance}

A experiência de download de arquivos pode variar para usuários em locais de clientes diferentes, dependendo de fatores como conectividade local com a Internet e latência do servidor. O desempenho de download esperado para arquivos de 2 GB observado em locais de clientes diferentes é o seguinte, com o servidor Brand Portal em Oregon, nos Estados Unidos:

| Local do cliente | Latência entre cliente e servidor | Velocidade de download esperada | Tempo necessário para baixar um arquivo de 2 GB |
|-------------------------|-----------------------------------|-------------------------|------------------------------------|
| Oeste dos EUA (N. Califórnia) | 18 milissegundos | 7,68 MB/s | 4 minutos |
| Oeste dos EUA (Oregon) | 42 milissegundos | 3,84 MB/s | 9 minutos |
| Leste dos EUA (N. Virgínia) | 85 milissegundos | 1,61 MB/s | 21 minutos |
| APAC (Tóquio) | 124 milissegundos | 1,13 MB/s | 30 minutos |
| Noida | 275 milissegundos | 0,5 MB/s | 68 minutos |
| Sydney | 175 milissegundos | 0,49 MB/s | 69 minutos |
| Londres | 179 milissegundos | 0,32 MB/s | 106 minutos |
| Singapura | 196 milissegundos | 0,5 MB/s | 68 minutos |


>[!NOTE]
>
>Os dados citados são observados em condições de teste, que podem variar para usuários em locais diferentes que testemunham latência e largura de banda variadas.
