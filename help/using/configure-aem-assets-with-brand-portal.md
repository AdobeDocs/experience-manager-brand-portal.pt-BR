---
title: Configurar o Experience Manager Assets com o Brand Portal
description: Coloque uma insight na configuração do Experience Manager Assets com o Brand Portal.
content-type: reference
contentOwner: Vishabh Gupta
topic-tags: brand-portal
products: SG_EXPERIENCEMANAGER/Brand_Portal
role: Admin
exl-id: 261c0e84-6b3d-459c-b6b9-a9af106d6943
TQID: https://experienceleague.adobe.com/-FF6IXLHoYo485vkZVBaYMrVlZZYys0shOr9OChBlao
product_v2:
  - id: d09181b5-a36a-43de-ba01-36641440bc43
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: da0dfbce-df02-4f8b-b32d-a4e3b1d05085
subfeature_v2:
  - id: e00c7c12-7035-41fe-ad76-1ec82c8c3f01
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
source-git-commit: e48edcb1ed5d76686794f7a7ed6389c7f4ab1ed3
workflow-type: tm+mt
source-wordcount: 413
ht-degree: 28%

---

# Configurar o Experience Manager Assets com o Brand Portal {#configure-integration}

A configuração do Adobe Experience Manager Assets com Brand Portal habilita a publicação de ativos, a distribuição de ativos e os recursos de contribuição de ativos para os usuários do Brand Portal. Ele permite que os usuários do Experience Manager Assets publiquem e distribuam ativos com os usuários do Brand Portal. Os usuários do Brand Portal podem acessar os ativos compartilhados e contribuir carregando novos ativos nas pastas de contribuição de ativos e publicando-os de volta no Experience Manager Assets.

A configuração do Experience Manager Assets com Brand Portal é compatível com:

* Experience Manager Assets as a Cloud Service
* Experience Manager Assets (no local e managed service) 6.5 e superior

O Experience Manager Assets as a Cloud Service é configurado automaticamente com o Brand Portal ao ativar o Brand Portal na Cloud Manager. O fluxo de trabalho de ativação cria as configurações necessárias no backend e ativa o Brand Portal na mesma organização IMS da instância do Experience Manager Assets as a Cloud Service.

Enquanto o Experience Manager Assets (no local e managed service) é configurado manualmente com o Brand Portal usando o Adobe Developer Console, que obtém um token do Adobe Identity Management Services (IMS) para autorização do locatário do Brand Portal.

>[!NOTE]
>
>***Para Experience Manager Assets, 6.5 e posterior***
>
>Anteriormente, a interface clássica configurava o Brand Portal usando o Gateway OAuth herdado, que emprega a troca JSON Web Token (JWT) para obter um token IMS para autorização.
>
>A configuração por meio do OAuth herdado não é mais compatível a partir de 6 de abril de 2020 e foi alterada para configurar por meio do Adobe Developer Console.


>[!TIP]
>
>***Somente para clientes existentes (no local e managed service)***
>
>A configuração herdada do Gateway OAuth continua funcionando para os clientes existentes.
>
>Caso encontre problemas com a configuração do Gateway OAuth herdado, exclua a configuração existente e crie uma nova configuração por meio do Adobe Developer Console.

As etapas para configurar o AEM Assets com o Brand Portal são diferentes dependendo da sua versão do AEM e se você está configurando pela primeira vez ou atualizando as configurações existentes:

| **Versão do AEM** | **Nova configuração** | **Atualizar configuração** |
|---|---|---|
| **AEM Assets as a Cloud Service** | [Ativar Brand Portal](https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/assets/brand-portal/configure-aem-assets-with-brand-portal) | - |
| **AEM 6.5 (6.5.4.0 e superior)** | [Criar configuração](https://experienceleague.adobe.com/pt-br/docs/experience-manager-65/content/assets/brandportal/configure-aem-assets-with-brand-portal) | [Atualizar configuração](https://experienceleague.adobe.com/pt-br/docs/experience-manager-65/content/assets/brandportal/configure-aem-assets-with-brand-portal#upgrade-integration-65) |
