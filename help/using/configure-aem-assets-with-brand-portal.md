---
title: Configurar o Experience Manager Assets com o Brand Portal
seo-title: Configure Experience Manager Assets with Brand Portal
description: Obtenha informações sobre a configuração do Experience Manager Assets com o Brand Portal.
seo-description: Get an insight into configuring Experience Manager Assets with Brand Portal.
uuid: null
content-type: reference
contentOwner: Vishabh Gupta
topic-tags: brand-portal
products: SG_EXPERIENCEMANAGER/Brand_Portal
discoiquuid: null
role: Admin
exl-id: 261c0e84-6b3d-459c-b6b9-a9af106d6943
source-git-commit: 454b05c05359a2068cc29124f826d5bd25a1bad1
workflow-type: tm+mt
source-wordcount: '357'
ht-degree: 2%

---

# Configurar o Experience Manager Assets com o Brand Portal {#configure-integration}

A configuração do Adobe Experience Manager Assets com Brand Portal habilita a publicação de ativos, a distribuição de ativos e os recursos de contribuição de ativos para os usuários do Brand Portal. Ele permite que os usuários do Experience Manager Assets publiquem e distribuam ativos com os usuários do Brand Portal. Os usuários do Brand Portal podem acessar os ativos compartilhados e contribuir carregando novos ativos nas pastas de contribuição de ativos e publicando-os de volta no Experience Manager Assets.

A configuração do Experience Manager Assets com Brand Portal é compatível com:

* Experience Manager Assets as a Cloud Service
* Experience Manager Assets (no local e managed service) 6.5 e superior

O Experience Manager Assets as a Cloud Service é configurado automaticamente com o Brand Portal ao ativar o Brand Portal na Cloud Manager. O fluxo de trabalho de ativação cria as configurações necessárias no backend e ativa o Brand Portal na mesma organização IMS da instância as a Cloud Service do Experience Manager Assets.

Enquanto o Experience Manager Assets (no local e managed service) é configurado manualmente com o Brand Portal usando o Adobe Developer Console, que obtém um token Adobe Identity Management Services (IMS) para autorização do locatário do Brand Portal.

>[!NOTE]
>
>***Para o Experience Manager Assets 6.5 e posterior***
>
>Anteriormente, o Brand Portal era configurado na interface clássica por meio do Gateway OAuth herdado, que usa a troca de token da Web JSON (JWT) para obter um token IMS para autorização.
>
>A configuração pelo OAuth herdado não é mais compatível a partir de 6 de abril de 2020 e foi alterada para configuração pelo Adobe Developer Console.


>[!TIP]
>
>***Somente para clientes existentes (no local e managed service)***
>
>A configuração do Gateway OAuth herdado continuará funcionando para os clientes existentes.
>
>Caso encontre problemas com a configuração do gateway OAuth herdada, exclua a configuração existente e crie uma nova configuração por meio do Adobe Developer Console.

As etapas para configurar o AEM Assets com Brand Portal são diferentes, dependendo da versão do AEM e se você estiver configurando pela primeira vez ou atualizando as configurações existentes:

| **Versão do AEM** | **Nova configuração** | **Atualizar Configuração** |
|---|---|---|
| **AEM Assets as a Cloud Service** | [Ativar Brand Portal](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/brand-portal/configure-aem-assets-with-brand-portal.html) | - |
| **AEM 6.5 (6.5.4.0 e posterior)** | [Criar configuração](https://experienceleague.adobe.com/docs/experience-manager-65/assets/brandportal/configure-aem-assets-with-brand-portal.html?lang=pt-BR) | [Configuração de atualização](https://experienceleague.adobe.com/docs/experience-manager-65/assets/brandportal/configure-aem-assets-with-brand-portal.html?lang=pt-BR#upgrade-integration-65) |
