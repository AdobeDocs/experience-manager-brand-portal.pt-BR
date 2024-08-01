---
title: Perguntas frequentes
description: Obtenha um insight sobre as perguntas frequentes no Adobe Experience Manager Assets Brand Portal.
content-type: reference
contentOwner: Vishabh Gupta
topic-tags: frequently-asked-questions
products: SG_EXPERIENCEMANAGER/Brand_Portal
discoiquuid: null
exl-id: 4a8f7fbd-7485-421d-a8db-755324d2dbef
source-git-commit: 4c701781e7dc62b9d2b018fd13b1ae9616bbb840
workflow-type: tm+mt
source-wordcount: '1495'
ht-degree: 0%

---

# Perguntas frequentes {#frequently-asked-questions}

As Perguntas frequentes do Brand Portal se concentram nas consultas e problemas dos usuários finais que podem ser encontrados ao trabalhar com a versão mais recente do Experience Manager Assets Brand Portal 6.4.6 ou versões anteriores.


## Perguntas frequentes sobre o Brand Portal 6.4.6 {#faqs-bp646}

**Pergunta: o ponto de extremidade OAuth herdado existente (`https://legacy-oauth.cloud.adobe.io/login`) não está funcionando. Qual pode ser o motivo possível?**

**Resposta:** A configuração OAuth herdada está obsoleta. Atualize as instâncias do autor do Experience Manager Assets para o pacote de serviços mais recente e configure-o por meio do Adobe Developer Console. Consulte [Configurar o Experience Manager Assets com o Brand Portal](configure-aem-assets-with-brand-portal.md) para obter detalhes. No entanto, para que a configuração OAuth herdada funcione até você atualizar, atualize o ponto de extremidade OAuth herdado para `https://hypnosisprod.ethos11-prod-or1.ethos.adobe.net/`.

**Pergunta: não consigo publicar os ativos da pasta de contribuição do Brand Portal para o Experience Manager Assets depois de atualizar para o Adobe Developer Console. Minha instância de autor está no Experience Manager Assets 6.5.4. Qual pode ser o motivo possível?**

**Resposta:** Sim, há um problema conhecido ao publicar os ativos da pasta de contribuição no Experience Manager Assets 6.5.4 via Adobe Developer Console.

O problema é corrigido no Experience Manager Assets 6.5.5. Você pode atualizar sua instância do Experience Manager Assets para o service pack mais recente e [atualizar suas configurações](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/assets/brandportal/configure-aem-assets-with-brand-portal#upgrade-integration-65) no Adobe Developer Console.


**Pergunta: não vejo o conteúdo da pasta de contribuição publicado do Brand Portal no Experience Manager Assets. Qual pode ser o motivo possível?**

**Resposta:** Entre em contato com o administrador do Experience Manager Assets para verificar as configurações e garantir que seu locatário do Brand Portal esteja configurado com apenas uma instância de autor do Experience Manager Assets.

Esse problema pode ocorrer quando você configura um locatário do Brand Portal em várias instâncias de autor do Experience Manager Assets. Por exemplo, o administrador configura o mesmo locatário do Brand Portal na instância de autor do Experience Manager Assets de um ambiente de preparo e produção. Nesse caso, a publicação de ativos é acionada no Brand Portal, mas a instância do autor do Experience Manager Assets falha ao importar o ativo porque o agente de replicação não recebe o token solicitado.


**Pergunta: não consigo publicar ativos do Experience Manager Assets no Brand Portal. O log de replicação indica que a conexão atingiu o tempo limite. Há uma correção rápida?**

**Resposta:** Geralmente, a publicação falha com um erro de tempo limite se houver várias solicitações pendentes na fila de replicação. Para resolver esse problema, verifique se os agentes de replicação estão configurados para evitar o tempo limite.

Execute as seguintes etapas para configurar o agente de replicação:

1. Faça logon na instância de autor do Experience Manager Assets.
1. No painel **Ferramentas**, navegue até **[!UICONTROL Implantação]** > **[!UICONTROL Replicação]**.
1. Na página Replicação, clique em **[!UICONTROL `Agents on author`]**. Você pode ver os quatro agentes de replicação do seu locatário do Brand Portal.
1. Clique no URL do agente de replicação para abrir os detalhes do agente.
1. Clique em **[!UICONTROL Editar]** para editar as configurações do agente de replicação.
1. Nas configurações do agente, clique na guia **[!UICONTROL Extended]**.
1. Marque a caixa de seleção **[!UICONTROL Fechar Conexão]**.
1. Repita as etapas de 4 a 7 para configurar todos os quatro agentes de replicação.
1. Reinicie o servidor e verifique a conexão.


## Perguntas frequentes sobre o Brand Portal 6.4.5 {#faqs-bp645}

**Pergunta: Qual é a principal alteração na versão 6.4.5 do Brand Portal?**

**Resposta:** o Experience Manager Assets Brand Portal 6.4.5 permite que os usuários carreguem conteúdo e publiquem a pasta Contribuição de volta no Experience Manager Assets diretamente da Brand Portal, sem exigir direitos de administrador. Para obter mais informações, consulte [Origem de ativos no Brand Portal](brand-portal-asset-sourcing.md).



**Pergunta: perdi o acesso a algum ativo, recurso ou configuração existente que eu tenha criado?**

**Resposta:** todos os recursos e configurações existentes permanecem intactos. Os usuários finais não serão afetados e o conteúdo permanecerá intacto.



**Pergunta: Quando estou migrando para a nova versão do Brand Portal?**

**Resposta:** o Brand Portal 6.4.5 foi lançado para produção em outubro de 2019. E a próxima versão do Brand Portal está prevista para março de 2020.
Para atualizações e alterações de versão, a Adobe recomenda que você acompanhe as [Notas de versão](brand-portal-release-notes.md) e as [Novidades da Brand Portal](whats-new.md).



**Pergunta: meus usuários foram afetados?**

**Resposta:** A versão do Brand Portal 6.4.5 é exclusivamente da Brand Portal, portanto, não há impacto para os usuários finais.



**Pergunta: Há alguma ação necessária da minha parte como usuário do Brand Portal?**

**Resposta:** a versão Brand Portal 6.4.5 vem com um novo recurso chamado Origem de ativos. O administrador precisa configurar o recurso Origem de ativos no Experience Manager Assets para habilitar o recurso para os usuários do Brand Portal. Para obter mais informações, consulte [Habilitar a origem do ativo](brand-portal-asset-sourcing.md).



**Pergunta: Quem pode criar uma pasta de Contribuição?**

**Resposta:** Qualquer usuário do Experience Manager Assets que tenha permissões para criar uma pasta no Experience Manager Assets pode criar uma pasta de **Contribuição**. Para criar uma pasta de **Contribuição**, crie uma pasta do tipo **Contribuição de ativos**.
Esta pasta é compartilhada com os usuários ativos do Brand Portal para contribuição.



**Pergunta: O que contém uma pasta Contribuição?**

A pasta **Resposta:** **Contribuição** contém duas subpastas **NOVA** e **COMPARTILHADA**. Inicialmente, a NOVA pasta fica em branco e a pasta COMPARTILHADA contém o conteúdo de referência (ativos reutilizáveis) para os usuários do Brand Portal.
Os usuários do Brand Portal acessam a pasta **Contribuição** e fazem o upload do conteúdo na pasta **NOVA**.



**Pergunta: Posso modificar o nome de uma pasta de Contribuição existente?**

**Resposta:** **Não**, você não pode modificar o nome de uma pasta de **Contribuição** existente.



**Pergunta: O que é a contribuição w.r.t de requisitos de ativos?**

**Resposta:** O documento **Resumo** da pasta **Contribuição** e o conteúdo de referência na pasta **COMPARTILHADOS** ajudam os usuários da Brand Portal a entender as necessidades e expectativas de contribuição. Juntos, eles são conhecidos como requisitos de ativos.

**Pergunta: posso carregar ativos para qualquer pasta permitida?**

**Resposta:** Nem todas as pastas permitidas. Um usuário do Brand Portal pode carregar conteúdo somente para a pasta **Contribuição** que o administrador do Experience Manager Assets ou do Brand Portal compartilha.



**Pergunta: Como faço para obter acesso a uma pasta de Contribuição?**

**Resposta:** você só poderá acessar uma pasta de **Contribuição** se ela tiver sido compartilhada com você. Você recebe uma notificação por email/pulso sempre que uma pasta de Contribuição é compartilhada com você. É possível acessar a pasta Contribuição por meio do link compartilhado no email. Ou você pode fazer logon na instância do Brand Portal e navegar até o ícone de sino para receber notificações para acessar a pasta Contribuição.

>[!NOTE]
>
>Se você não for um usuário do Brand Portal, solicite que o administrador do Experience Manager Assets crie seu usuário no Admin Console. Em seguida, adicione seu perfil ao arquivo de configuração do usuário na lista de usuários do Brand Portal.


**Pergunta: Qual é o formato do arquivo CSV para importação de usuário?**

**Resposta:** o formato corresponde ao Admin Console que suporta a importação de usuários em massa. Email, nome e sobrenome são obrigatórios.



**Pergunta: O que preenche a lista de usuários (colaboradores do Brand Portal) no menu suspenso de usuários da Contribuição de ativos?**

**Resposta:** os usuários do menu suspenso são preenchidos a partir do arquivo de configuração de usuário do Brand Portal (.csv) carregado no Experience Manager Assets.



**Pergunta: Onde posso ver o status dos trabalhos de importação e publicação?**

**Resposta:** no Experience Manager Assets, você pode ver o status de uma importação na página de trabalho **assíncrono**. No Brand Portal, você pode ver o status de um trabalho de publicação em **[!UICONTROL Ferramentas > Status de contribuição do ativo]**.



**Pergunta: Qual é a frequência de um trabalho de importação que é executado periodicamente no Experience Manager?**

**Resposta:** no Experience Manager Assets, a sondagem é executada a cada cinco minutos.



**Pergunta: Há um limite para o número de vezes que uma pasta pode ser publicada do Brand Portal para o Experience Manager Assets?**

**Resposta:** Não, todos os ativos na pasta **NOVO** são publicados na Experience Manager Assets, independentemente do fato de terem sido publicados anteriormente. Toda vez que uma pasta de **Contribuição** é publicada do Brand Portal para o Experience Manager Assets, ela substitui o conteúdo da pasta **NOVA**.



**Pergunta: como fazer upload de novos ativos em uma pasta de Contribuição?**

**Resposta:** Consulte a documentação detalhada para [Carregar ativos para a pasta de Contribuição](brand-portal-publish-contribution-folder-to-brand-portal.md).



**Pergunta: não consigo ver miniaturas ou visualizações dos ativos carregados na NOVA pasta.**

**Resposta:** está conforme projetado, pois não há fluxo de trabalho executado no final do Brand Portal.



**Pergunta: O que acontece se uma pasta for publicada do Experience Manager Assets para o Brand Portal em fluxo?**

**Resposta:** no Experience Manager Assets, os logs são mantidos sempre que uma pasta é publicada no Brand Portal. No momento da publicação, todos os ativos que não são publicados no Brand Portal são adicionados a uma fila de replicação. Nenhum ativo adicionado à pasta após o acionamento do trabalho de publicação é publicado no Brand Portal. Quando um usuário do Experience Manager Assets publica a pasta novamente, somente os ativos que não foram publicados anteriormente (existentes na fila de replicação) são publicados no Brand Portal. Esse processo é verdadeiro para qualquer pasta publicada do Experience Manager Assets para o Brand Portal e para a pasta SHARED em uma pasta de Contribuição.

**Pergunta: com quem devo entrar em contato para fazer perguntas?**

**Resposta:** Entre em contato com o Gerente de Conta do Adobe ou com o Suporte ao Cliente.

>[!NOTE]
>
>A programação de lançamento é provisória e está sujeita a alterações. Entre em contato com o Gerente de conta do Adobe ou com o Suporte ao cliente para obter o cronograma atualizado de lançamentos.


## Acesso e suporte do produto (sites restritos) {#product-access-and-support-restricted-sites}

Esses sites só estão disponíveis para clientes do. Se você for um cliente do e precisar de acesso, entre em contato com o Gerente de conta do Adobe.

<!--
* [](https://daycare.day.com) [Product Access](https://login.marketing.adobe.com)

* [Adobe Customer Support]()
-->
