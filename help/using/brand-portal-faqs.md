---
title: Perguntas frequentes
seo-title: null
description: Obtenha um insight sobre as perguntas frequentes no Adobe Experience Manager Assets Brand Portal.
seo-description: null
uuid: null
content-type: reference
contentOwner: Vishabh Gupta
topic-tags: frequently-asked-questions
products: SG_EXPERIENCEMANAGER/Brand_Portal
discoiquuid: null
exl-id: 4a8f7fbd-7485-421d-a8db-755324d2dbef
source-git-commit: 4caa4263bd74b51af7504295161c421524e51f0c
workflow-type: tm+mt
source-wordcount: '1529'
ht-degree: 0%

---

# Perguntas frequentes {#frequently-asked-questions}

As Perguntas frequentes do Brand Portal se concentram nas consultas e problemas que os usuários finais podem encontrar ao trabalhar com a versão mais recente do Experience Manager Assets Brand Portal 6.4.6 ou versões anteriores.


## Perguntas frequentes sobre o Brand Portal 6.4.6  {#faqs-bp646}

**Consultas. O ponto de extremidade OAuth herdado existente (`https://legacy-oauth.cloud.adobe.io/login`) não está funcionando. Qual pode ser o motivo possível?**

**Ans** A configuração OAuth herdada está obsoleta. Atualize as instâncias do autor do Experience Manager Assets para o service pack mais recente e configure-o pelo Adobe Developer Console. Consulte [Configurar o Experience Manager Assets com o Brand Portal](configure-aem-assets-with-brand-portal.md) para obter detalhes. No entanto, para que a configuração OAuth herdada funcione até você atualizar, atualize o ponto de extremidade OAuth herdado para `https://hypnosisprod.ethos11-prod-or1.ethos.adobe.net/`.

<!--
**Ques. I have created a collection using the asset link shared by the administrator. But I am unable to create a share link for my collection. Do I need special permissions to do this?**

**Ans.** The functionality is by design, the viewer users are not permitted to share link for collections as they have limited privileges due to which they cannot add users to create a share link. It is a known issue that the share link for collections is currently visible to the viewer users. This issue will be fixed in the upcoming release, the option to share link for the collections will not be available to the viewer users.    
-->

**Consultas. Não consigo publicar os ativos da pasta de contribuição do Brand Portal para o Experience Manager Assets depois de atualizar para o Adobe Developer Console. Minha instância de autor está no Experience Manager Assets 6.5.4. Qual pode ser o motivo possível?**

**Ans** Sim, há um problema conhecido ao publicar os ativos da pasta de contribuição no Experience Manager Assets 6.5.4 via Adobe Developer Console.

O problema é corrigido no Experience Manager Assets 6.5.5. Você pode atualizar sua instância do Experience Manager Assets para o service pack mais recente e [atualizar suas configurações](https://experienceleague.adobe.com/docs/experience-manager-65/assets/brandportal/configure-aem-assets-with-brand-portal.html?lang=pt-BR#upgrade-integration-65) no Adobe Developer Console.

<!--
Broken link of download hotfix, comment out this section until we have the latest URL.

For immediate fix on AEM 6.5.4, it is recommended to [download the hotfix](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq650/hotfix/cq-6.5.0-hotfix-33041) and install on your AEM author instance.
-->

**Consultas. Não vejo o conteúdo da pasta de contribuição publicado do Brand Portal no Experience Manager Assets. Qual pode ser o motivo possível?**

**Ans** Entre em contato com o administrador do Experience Manager Assets para verificar as configurações e garantir que seu locatário do Brand Portal esteja configurado com apenas uma instância de autor do Experience Manager Assets.

Esse problema pode ocorrer quando você configura um locatário do Brand Portal em várias instâncias de autor do Experience Manager Assets. Por exemplo, o administrador configura o mesmo locatário do Brand Portal na instância de autor do Experience Manager Assets do ambiente de preparo e produção. Nesse caso, a publicação de ativos é acionada no Brand Portal, mas a instância do autor do Experience Manager Assets não pode importar o ativo porque o agente de replicação não recebe o token de solicitação.


**Consultas. Não consigo publicar ativos do Experience Manager Assets no Brand Portal. O log de replicação indica que a conexão atingiu o tempo limite. Há uma correção rápida?**

**Ans** Geralmente, a publicação falha com um erro de tempo limite se houver várias solicitações pendentes na fila de replicação. Para resolver esse problema, verifique se os agentes de replicação estão configurados para evitar o tempo limite.

Execute as seguintes etapas para configurar o agente de replicação:

1. Faça logon na instância de autor do Experience Manager Assets.
1. No painel **Ferramentas**, navegue até **[!UICONTROL Implantação]** > **[!UICONTROL Replicação]**.
1. Na página Replicação, clique em **[!UICONTROL Agentes no autor]**. Você pode ver os quatro agentes de replicação do seu locatário do Brand Portal.
1. Clique no URL do agente de replicação para abrir os detalhes do agente.
1. Clique em **[!UICONTROL Editar]** para modificar as configurações do agente de replicação.
1. Em Configurações do Agente, clique na guia **[!UICONTROL Estendido]**.
1. Marque a caixa de seleção **[!UICONTROL Fechar Conexão]**.
1. Repita as etapas de 4 a 7 para configurar todos os quatro agentes de replicação.
1. Reinicie o servidor e verifique a conexão.


## Perguntas frequentes sobre o Brand Portal 6.4.5  {#faqs-bp645}

**Consultas. Qual é a principal alteração na versão 6.4.5 do Brand Portal?**

**AnsO** Experience Manager Assets Brand Portal 6.4.5 é uma versão de recurso que permite aos usuários do Brand Portal carregar conteúdo de dentro da instância do Brand Portal e publicar a pasta Contribuição de volta no Experience Manager Assets sem precisar de direitos de administrador.
Para obter mais informações, consulte [Origem de ativos no Brand Portal](brand-portal-asset-sourcing.md).



**Consultas. Perderei o acesso a todos os ativos, recursos ou configurações existentes que criei?**

**Ans** Todos os recursos e configurações existentes permanecem intactos. Os usuários finais não serão afetados e o conteúdo permanecerá intacto.



**Consultas. Quando estou migrando para a nova versão do Brand Portal?**

**AnsO** Brand Portal 6.4.5 foi lançado para produção em outubro de 2019. E a próxima versão do Brand Portal deve ser lançada no terceiro trimestre de 2020.
Para atualizações e alterações de versão, é recomendável acompanhar as [Notas de Versão](brand-portal-release-notes.md) e as [Novidades no Brand Portal](whats-new.md).



**Consultas. Meus usuários serão afetados?**

**Ans** A versão do Brand Portal 6.4.5 é exclusivamente da Brand Portal, portanto, não há impacto para os usuários finais.



**Consultas. Há alguma ação necessária da minha parte como usuário do Brand Portal?**

**AnsA versão** do Brand Portal 6.4.5 vem com um novo recurso chamado Origem de ativos. O administrador precisa configurar o recurso Origem de ativos no Experience Manager Assets para habilitar o recurso para os usuários do Brand Portal. Para obter mais informações, consulte [Habilitar a origem do ativo](brand-portal-asset-sourcing.md).



**Consultas. Quem pode criar uma pasta de Contribuição?**

**Ans** Qualquer usuário do Experience Manager Assets com permissões para criar uma nova pasta no Experience Manager Assets pode criar uma pasta de **Contribuição**. Para criar uma pasta de **Contribuição**, crie uma nova pasta do tipo **Contribuição de ativos**.
Esta pasta é compartilhada com os usuários ativos do Brand Portal para contribuição.



**Consultas. O que contém uma pasta Contribuição?**

**AnsA pasta** **Contribuição** contém duas subpastas **NOVA** e **COMPARTILHADA**. Inicialmente, a NOVA pasta fica em branco e a pasta COMPARTILHADA contém o conteúdo de referência (ativos reutilizáveis) para os usuários do Brand Portal.
Os usuários do Brand Portal acessam a pasta **Contribuição** e fazem o upload do conteúdo na pasta **NOVA**.



**Consultas.  Posso modificar o nome de uma pasta de Contribuição existente?**

**Ans** **Não**, você não pode modificar o nome de uma pasta **Contribuição** existente.



**Consultas. O que é a contribuição w.r.t de requisitos de ativos?**

**Ans** O documento **Resumo** anexado à pasta **Contribuição** e o conteúdo de referência (ativos reutilizáveis) carregado na pasta **COMPARTILHADOS** ajudam o usuário do Brand Portal a entender a necessidade de contribuição e as expectativas como colaborador e são chamados coletivamente de requisitos de ativos.



**Consultas. É possível carregar ativos para qualquer pasta permitida?**

**Ans** Nem todas as pastas permitidas. Um usuário do Brand Portal pode carregar conteúdo somente para a pasta **Contribuição**, que é compartilhada pelo administrador do Experience Manager Assets ou do Brand Portal.



**Consultas. Como obter acesso a uma pasta de Contribuição?**

**Ans** Você pode acessar uma pasta de **Contribuição** somente se ela tiver sido compartilhada com você. Você receberá uma notificação por email/pulso sempre que uma pasta de Contribuição for compartilhada com você. Você pode acessar a pasta Contribuição por meio do link compartilhado no email ou fazer logon na sua instância do Brand Portal e navegar até o ícone de sino para receber uma notificação para acessar a pasta Contribuição.

>[!NOTE]
>
>Se você não for um usuário do Brand Portal, solicite que o administrador do Experience Manager Assets crie seu usuário no Admin Console e adicione seu perfil ao arquivo de configuração de usuário na lista de usuários do Brand Portal.

**Consultas. Qual é o Formato do arquivo CSV para importação do usuário?**

**Ans** O formato é igual ao que é suportado pelo Admin Console para importação de usuários em massa. Email, nome e sobrenome são obrigatórios.



**Consultas. O que preenche a lista de usuários (colaboradores do Brand Portal) no menu suspenso de usuários da Contribuição de ativos?**

**Ans** Os usuários na lista suspensa são preenchidos com o arquivo de configuração de usuário do Brand Portal (.csv) carregado no Experience Manager Assets.



**Consultas. Onde posso ver o status dos trabalhos de importação e publicação?**

**Ans** No Experience Manager Assets, você pode ver o status de uma importação na página de trabalho **async**. No Brand Portal, você pode ver o status de um trabalho de publicação em **[!UICONTROL Ferramentas > Status de contribuição do ativo]**.



**Consultas. Qual é a frequência de um trabalho de importação que é executado periodicamente no Experience Manager?**

**Ans** No Experience Manager Assets, a sondagem é executada a cada 5 minutos.



**Consultas. Há algum limite para o número de vezes que uma pasta pode ser publicada do Brand Portal para o Experience Manager Assets?**

**Ans** Não, todos os ativos na pasta **NOVO** são publicados no Experience Manager Assets, independentemente do fato de terem sido publicados anteriormente. Toda vez que uma pasta de **Contribuição** é publicada do Brand Portal para o Experience Manager Assets, ela substitui o conteúdo da pasta **NOVA**.



**Consultas. Como carregar novos ativos em uma pasta de Contribuição?**

**Ans** Consulte a documentação detalhada para [Carregar ativos para a pasta de Contribuição](brand-portal-publish-contribution-folder-to-brand-portal.md).



**Consultas. Não vejo miniaturas/visualizações nos ativos carregados para a NOVA pasta por um usuário do Brand Portal?**

**Ans** Está de acordo com o design, visto que não há nenhum fluxo de trabalho sendo executado no final do Brand Portal.



**Consultas. O que acontece se uma pasta for publicada do Experience Manager Assets para o Brand Portal em fluxo?**

**Ans** No Experience Manager Assets, os logs são mantidos para cada vez que uma pasta é publicada no Brand Portal. No momento da publicação, todos os ativos que não são publicados no Brand Portal são colocados em uma fila de replicação. Nenhum ativo adicionado à pasta após o acionamento do trabalho de publicação é publicado no Brand Portal. Quando o usuário do Experience Manager Assets publica a pasta novamente, somente os ativos que não foram publicados anteriormente (existentes na fila de replicação) são publicados no Brand Portal.
Isso se aplica a qualquer pasta publicada do Experience Manager Assets para o Brand Portal e a qualquer pasta COMPARTILHADA em uma pasta de Contribuição.

**Consultas. Com quem devo entrar em contato para tirar dúvidas?**

**Ans** Entre em contato com o Gerente de conta do Adobe ou com o Suporte ao cliente.

>[!NOTE]
>
>A programação de lançamento é provisória e está sujeita a alterações. Entre em contato com o Gerente de conta do Adobe ou com o Suporte ao cliente para obter o cronograma atualizado de lançamentos.


## Acesso e suporte do produto (sites restritos) {#product-access-and-support-restricted-sites}

Esses sites só estão disponíveis para clientes do. Se você for um cliente do e precisar de acesso, entre em contato com o gerente de conta da Adobe.

<!--
* [](https://daycare.day.com) [Product Access](https://login.marketing.adobe.com)

* [Adobe Customer Support]()
-->
