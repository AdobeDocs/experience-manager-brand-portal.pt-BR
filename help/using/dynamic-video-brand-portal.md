---
title: Suporte a vídeo dinâmico no Brand Portal
description: Suporte a vídeo dinâmico no Brand Portal
contentOwner: mgulati
products: SG_EXPERIENCEMANAGER/Brand_Portal
content-type: reference
topic-tags: download-install
exl-id: 08d6a0fb-061e-4bef-b8e2-bb8522e7482e
source-git-commit: e2e007550b557e790533204d49271c90b3b8647d
workflow-type: tm+mt
source-wordcount: '1194'
ht-degree: 0%

---

# Suporte a vídeo dinâmico no Brand Portal {#dynamic-video-support-on-brand-portal}

Pré-visualize e reproduza vídeos de forma adaptável no Brand Portal com suporte ao Dynamic Media. Baixe também as representações dinâmicas do portal e os links compartilhados.
Os usuários do Brand Portal podem:

* Visualize vídeos na página Detalhes do ativo, na Exibição de cartão e na página de visualização do compartilhamento de link.
* Reproduzir códigos de vídeo na página Detalhes do ativo.
* Exiba representações dinâmicas na guia Representações da página Detalhes do ativo.
* Baixe códigos de vídeo e pastas que contêm vídeos.

>[!NOTE]
>
>Para trabalhar com vídeos e publicá-los no Brand Portal, verifique se a instância do Experience Manager Author está configurada no modo Híbrido do Dynamic Media ou no modo **[!DNL Scene7]** do Dynamic Media.

Para visualizar, reproduzir e baixar vídeos, o Brand Portal expõe as duas configurações a seguir para os administradores:

* [Configuração híbrida do Dynamic Media](#configure-dm-hybrid-settings)
Se a instância do autor do Experience Manager estiver sendo executada no Dynamic Media - modo híbrido.
* [Dynamic Media [!DNL Scene7] configuração](#configure-dm-scene7-settings)
Se a instância do Autor do Experience Manager estiver em execução no Dynamic Media - modo **[!DNL Scene7]**.
Defina qualquer uma dessas configurações com base nas configurações definidas na instância do autor do Experience Manager com a qual o locatário do Brand Portal é replicado.

>[!NOTE]
>
>Os locatários do Brand Portal configurados com o Experience Manager Author em execução no modo de execução **[!UICONTROL Scene7 Connect]** não oferecem suporte para vídeos dinâmicos.

## Como os vídeos dinâmicos são reproduzidos? {#how-are-dynamic-videos-played}

![Os códigos de vídeo foram obtidos da nuvem](assets/VideoEncodes.png)

Se as configurações do Dynamic Media ([Híbrido](../using/dynamic-video-brand-portal.md#configure-dm-hybrid-settings) ou [[!DNL Scene7]](../using/dynamic-video-brand-portal.md#configure-dm-scene7-settings) configurações) estiverem definidas no Brand Portal, as representações dinâmicas serão buscadas no servidor **[!DNL Scene7]**. As codificações de vídeo são, portanto, visualizadas e reproduzidas sem atraso e distorção na qualidade.

O repositório do Brand Portal não armazena códigos de vídeo e os busca no servidor **[!DNL Scene7]**. Verifique se as configurações do Dynamic Media na Instância do autor do Adobe Experience Manager e no Brand Portal são iguais.

>[!NOTE]
>
>Visualizadores de vídeo e predefinições do visualizador não são compatíveis com o Brand Portal. Os vídeos são visualizados e reproduzidos nos visualizadores padrão no Brand Portal.

## Pré-requisitos {#prerequisites}

Para trabalhar com vídeos dinâmicos no Brand Portal, certifique-se de:

* **Iniciar o Autor do Experience Manager no modo Dynamic Media**

  Inicie a instância do Autor do Experience Manager (com a qual o Brand Portal está configurado) no [Dynamic Media - [!DNL Scene7] modo](https://experienceleague.adobe.com/pt-br/docs/experience-manager-65/content/assets/dynamic/config-dms7#enabling-dynamic-media-in-scene-mode) ou no [Dynamic Media - modo híbrido](https://experienceleague.adobe.com/pt-br/docs/experience-manager-65/content/assets/dynamic/config-dynamic) ou

* **Configurar o Dynamic Media Cloud Service na instância do Experience Manager Author**

  Com base no modo Dynamic Media (modo Scene7 ou modo Híbrido) em que o Experience Manager Author está sendo executado, defina [Cloud Service do Dynamic Media ([!DNL Scene7] modo)](https://experienceleague.adobe.com/pt-br/docs/experience-manager-65/content/assets/dynamic/config-dms7#configuring-dynamic-media-cloud-services) ou [Cloud Service do Dynamic Media (modo Híbrido)](https://experienceleague.adobe.com/pt-br/docs/experience-manager-65/content/assets/dynamic/config-dms7#configuring-dynamic-media-cloud-services) no Experience Manager Author em **Tools** | **Cloud Service** | **Dynamic Media**.

* **Configurar o Dynamic Media no Brand Portal**

  Com base nas configurações da Dynamic Media Cloud no Autor do Experience Manager, defina as [configurações do Dynamic Media](#configure-dm-hybrid-settings) ou as [[!DNL Scene7] configurações](#configure-dm-scene7-settings) com base nas ferramentas administrativas do Brand Portal.

  Verifique se [locatários separados do Brand Portal](#separate-tenants) são usados para instâncias de Autor do Experience Manager configuradas no modo Dynamic Media - **[!UICONTROL Scene7]** e Dynamic Media - Híbrido. Se você usar as funcionalidades do Dynamic Media **[!UICONTROL S7]** e do Dynamic Media Hybrid, essa abordagem será particularmente importante.

* **pastas do Publish com códigos de vídeo aplicados ao Brand Portal**

  Aplique [codificações de vídeo](https://experienceleague.adobe.com/pt-br/docs/experience-manager-65/content/assets/dynamic/video-profiles) e publique a pasta que contém ativos de mídia avançada da instância do Autor do Experience Manager no Brand Portal.

* **Incluir na lista de permissões IPs de saída no SPS se a visualização segura estiver habilitada**

  Se estiver usando o Dynamic Media incluir na lista de permissões-**[!DNL Scene7]** (com a [visualização segura habilitada](https://experienceleague.adobe.com/pt-br/docs/dynamic-media-classic/using/upload-publish/testing-assets-making-them-public) para uma empresa), recomenda-se que o **[!DNL Scene7]** administrador da empresa [resolva os IPs de saída públicos](https://experienceleague.adobe.com/pt-br/docs/dynamic-media-classic/using/upload-publish/testing-assets-making-them-public#testing-the-secure-testing-service) para as respectivas regiões usando a interface do usuário flash do SPS (**[!UICONTROL Scene7]** Publishing System).

  Os IPs de saída são os seguintes:

  | **Região** | **IP de saída** |
  |--- |--- |
  | ND | 130 248 160 68 20 94 203 130 |
  | EMEA | 185.34.189.3, 51.132.146.75 |
  | APAC | 63.140.44.54 |

  Incluir na lista de permissões Para pesquisar qualquer um desses IPs de saída, consulte [Preparar sua conta para um serviço de teste seguro](https://experienceleague.adobe.com/pt-br/docs/dynamic-media-classic/using/upload-publish/testing-assets-making-them-public#testing-the-secure-testing-service).

## Práticas recomendadas

Verifique se os ativos de vídeo dinâmico foram visualizados, reproduzidos e baixados com êxito da Brand Portal (e links compartilhados) e siga estas práticas:

### Locatários separados para Dynamic Media - Scene7 e Dynamic Media - Modos híbridos {#separate-tenants}

Se você usar os recursos do modo Dynamic Media - **[!DNL Scene7]** e do modo Dynamic Media - Híbrido, use locatários diferentes do Brand Portal para instâncias do Experience Manager Author configuradas com os modos Dynamic Media - **[!DNL Scene7]** e Dynamic Media - Híbrido.


![Mapeamento de um para um do autor e BP](assets/BPDynamicMedia.png)

### Mesmos detalhes de configuração na instância do autor do Experience Manager e no Brand Portal

Verifique se os detalhes da configuração são os mesmos na Brand Portal e na **[!UICONTROL Configuração da nuvem do Experience Manager]**. Os mesmos detalhes de configuração incluem o seguinte:

* **[!UICONTROL Título]**
* **[!UICONTROL ID de Registro]**
* **[!UICONTROL URL do Serviço de Vídeo]** em **[!UICONTROL Dynamic Media - Modo híbrido]**
* **[!UICONTROL Título]**
* Credenciais (**[!UICONTROL Email]** e Senha)
* **[!UICONTROL Região]**
* **[!UICONTROL Empresa]** na Dynamic Media - modo **[!DNL Scene7]**

### Incluir na lista de permissões Pesquisar IPs de saída pública para o modo Dynamic Media Scene7

Se o Dynamic Media **[!UICONTROL Scene7]** - com a [visualização segura habilitada](https://experienceleague.adobe.com/pt-br/docs/dynamic-media-classic/using/upload-publish/testing-assets-making-them-public) - for usado para fornecer ativos de vídeo ao Brand Portal, o **[!UICONTROL Scene7]** estabelecerá um servidor de imagens dedicado para ambientes de preparo ou aplicativos internos. Qualquer solicitação a esse servidor verifica o endereço IP de origem. Se a solicitação recebida não estiver na lista aprovada de endereços IP, uma resposta de falha será retornada.
O administrador da empresa **[!UICONTROL Scene7]** configura, portanto, uma lista aprovada de endereços IP para o ambiente **[!UICONTROL Teste Seguro]** da empresa, por meio da interface do usuário flash do **[!UICONTROL SPS]** (Scene7 Publishing System). Verifique se o IP de saída da sua respectiva região (a seguir) foi adicionado a essa lista aprovada.
Incluir na lista de permissões Para pesquisar qualquer um desses IPs de saída, consulte [Preparar sua conta para um serviço de teste seguro](https://experienceleague.adobe.com/pt-br/docs/dynamic-media-classic/using/upload-publish/testing-assets-making-them-public#testing-the-secure-testing-service).
Os IPs de saída são os seguintes:

| **Região** | **IP de saída** |
|--- |--- |
| ND | 130 248 160 68 20 94 203 130 |
| EMEA | 51.132.146.75, 130.248.244.202, 130.248.244.203, 130.248.244.204, 130.248.244.210, 130.248.244.211, 130.248.244.212 |
| APAC | 63.140.44.54 |

## Definir configurações do Dynamic Media (híbrido) {#configure-dm-hybrid-settings}

Se a instância do Autor do Experience Manager estiver sendo executada no modo híbrido de mídia dinâmica, use o bloco **[!UICONTROL Vídeo]** do painel de ferramentas administrativas para definir as configurações do gateway do Dynamic Media.

>[!NOTE]
>
>Os [perfis de codificação de vídeo](https://experienceleague.adobe.com/pt-br/docs/experience-manager-65/content/assets/dynamic/video-profiles) não foram publicados no Brand Portal. Em vez disso, eles são obtidos do servidor **[!UICONTROL Scene7]**. Portanto, para que os códigos de vídeo sejam reproduzidos com êxito no Brand Portal, verifique se os detalhes da configuração são iguais aos [Cloud Service do Dynamic Media ([!DNL Scene7] modo)](https://experienceleague.adobe.com/pt-br/docs/experience-manager-65/content/assets/dynamic/config-dms7#configuring-dynamic-media-cloud-services) na instância do autor do Experience Manager.

Para definir as configurações do Dynamic Media nos locatários do Brand Portal:

1. Selecione o logotipo Experience Manager para acessar as ferramentas administrativas na barra de ferramentas na parte superior do Brand Portal.
1. No painel de ferramentas administrativas, selecione o bloco **[!UICONTROL Vídeo]**.

   ![Configuração híbrida do Dynamic Media no Brand Portal](assets/DMHybrid-Video.png)

   A página **[!UICONTROL Editar configuração do Dynamic Media]** é aberta.

   ![Configuração Híbrida do Dynamic Media no Brand Portal](assets/edit-dynamic-media-config.png)

1. Especifique a **[!UICONTROL ID de Registro]** e a **[!UICONTROL URL do Serviço de Vídeo]** (URL do Gateway DM). Verifique se esses detalhes são iguais aos detalhes em **[!UICONTROL Ferramentas > Cloud Service]** na instância do Experience Manager Author.
1. Selecione **Salvar** para salvar a configuração.

## Definir configurações do Dynamic Media Scene7 {#configure-dm-scene7-settings}

Se a instância do Autor do Experience Manager estiver sendo executada no modo Dynamic Media- **[!UICONTROL Scene7]**, use o bloco **[!UICONTROL Configuração do Dynamic Media]** do painel de ferramentas administrativas para definir as configurações do servidor **[!UICONTROL Scene7]**.

Para definir as configurações do Dynamic Media **[!UICONTROL Scene7]** nos locatários do Brand Portal:

1. Selecione o logotipo Experience Manager para acessar as ferramentas administrativas na barra de ferramentas na parte superior do Brand Portal.

2. No painel de ferramentas administrativas, selecione o bloco **[!UICONTROL Configuração do Dynamic Media]**.

   Configuração ![DM [!UICONTROL Scene 7] no Brand Portal](assets/DMS7-Tile.png)

   A página **[!UICONTROL Editar configuração do Dynamic Media]** é aberta.

   ![Configuração do Scene7 no Brand Portal](assets/S7Config.png)

3. Fornecer:

   * **[!UICONTROL Título]**
   * Credenciais (**[!UICONTROL ID de email]** e **[!UICONTROL Senha]**) para acessar o servidor do Scene7
   * **[!UICONTROL Região]**

   Verifique se esses valores são os mesmos que os valores encontrados na instância do autor do Experience Manager.

4. Selecione **[!UICONTROL Conectar ao Dynamic Media]**.

5. Forneça o **[!UICONTROL Nome da empresa]** e **[!UICONTROL Salve]** a configuração.
