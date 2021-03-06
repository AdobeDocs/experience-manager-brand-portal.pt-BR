---
title: Solucionar problemas na publicação paralela no Brand Portal
seo-title: Troubleshoot issues in parallel publishing to Brand Portal
description: Solucione problemas de publicação paralela.
seo-description: Troubleshoot parallel publishing.
uuid: 51e45cca-8c96-4c69-84ef-2ef34f3bcde2
products: SG_EXPERIENCEMANAGER/Brand_Portal
content-type: reference
topic-tags: brand-portal
discoiquuid: a4801024-b509-4c51-afd8-e337417e658b
role: Admin
exl-id: 631beabc-b145-49ba-a8e4-f301497be6da
source-git-commit: 72cd0ebbf05067287d94e1dc4e1b68f5fb6c2888
workflow-type: tm+mt
source-wordcount: '953'
ht-degree: 1%

---

# Solucionar problemas na publicação paralela no Brand Portal {#troubleshoot-issues-in-parallel-publishing-to-brand-portal}

O Brand Portal é configurado com o Experience Manager Assets para ter ativos de marca aprovados assimilados (ou publicados) sem interrupções da instância de criação do Experience Manager Assets. Uma vez [configurado](../using/configure-aem-assets-with-brand-portal.md), o Experience Manager Author usa um agente de replicação para replicar os ativos selecionados no serviço de nuvem da Brand Portal para uso aprovado pelos usuários do Brand Portal. Vários agentes de replicação são usados no Experience Manager 6.2 SP1-CFP5, Experience Manager CFP 6.3.0.2 e em diante para permitir a publicação paralela de alta velocidade.

>[!NOTE]
>
>O Adobe recomenda atualizar para o Experience Manager 6.4.1.0 para garantir que o Experience Manager Assets Brand Portal seja configurado com êxito com o Experience Manager Assets. Uma limitação no Experience Manager 6.4 dá um erro ao configurar o Experience Manager Assets com o Brand Portal e a replicação falha.

Ao configurar o serviço em nuvem para o Brand Portal em **[!UICONTROL /etc/cloudservice]**, todos os usuários e token necessários são gerados automaticamente e salvos no repositório. A configuração do Cloud Service é criada, os usuários de serviço necessários para os agentes de replicação e replicação replicarem conteúdo também são criados. Ele cria quatro agentes de replicação. Assim, ao publicar vários ativos do Experience Manager para o Brand Portal, eles são enfileirados e distribuídos entre os agentes de replicação por meio da Round Robin.

No entanto, a publicação pode falhar intermitentemente devido a grandes trabalhos do sling, maior rede e **[!UICONTROL E/S de disco]** na instância Experience Manager Author ou desempenho lento da instância Experience Manager Author. Portanto, é recomendável testar a conexão com os agentes de replicação antes de começar a publicar.

![](assets/test-connection.png)

## Solucionar problemas de falhas na primeira publicação: como validar sua configuração de publicação {#troubleshoot-failures-in-first-time-publishing-validating-your-publish-configuration}

Para validar suas configurações de publicação:

1. Verifique os registros de erros
1. Verifique se o agente de replicação foi criado
1. Testar conexão

**Registros finais ao criar o Cloud Service**

Verifique os logs de cauda. Verifique se o agente de replicação foi criado ou não. Se a criação do agente de replicação falhar, edite o serviço de nuvem fazendo pequenas alterações no serviço de nuvem. Valide e verifique novamente se o agente de replicação foi criado ou não. Caso contrário, edite novamente o serviço.

Se, ao editar repetidamente o serviço de nuvem, ele não estiver configurado corretamente, relate um tíquete de creche.

**Testar conexão com agentes de replicação**

Exibir log, se forem encontrados erros no log de replicação:

1. Entre em contato com o Suporte ao cliente.

1. Tentar novamente [limpeza](../using/troubleshoot-parallel-publishing.md#clean-up-existing-config) e crie a configuração de publicação novamente.

<!--
Comment Type: remark
Last Modified By: Mini Gulati (mgulati)
Last Modified Date: 2018-06-21T22:56:21.256-0400
<p>?? check and compare public key. At times public key is different</p>
<p>?? another thing to check in /useradmin</p>
-->

## Limpar configurações de publicação existentes do Brand Portal {#clean-up-existing-config}

Na maioria das vezes, quando a publicação não está funcionando, o motivo pode ser o usuário que está publicando (por exemplo: `mac-<tenantid>-replication` não tem a chave privada mais recente e, portanto, a publicação falha com o erro &quot;401 unauthorized&quot; e nenhum outro erro é relatado em logs do agente de replicação. Talvez você queira evitar a solução de problemas e criar uma configuração. Para que a nova configuração funcione corretamente, limpe o seguinte da configuração de Experience Manager author :

1. Ir para `localhost:4502/crx/de/` (considerando que você está executando a instância do autor no localhost:4502:\
   i. excluir `/etc/replication/agents.author/mp_replication`
ii. delete 
`/etc/cloudservices/mediaportal/<config_name>`

1. Vá para localhost:4502/useradmin:\
   i. pesquisar usuário `mac-<tenantid>replication`
ii. excluir este usuário

Agora o sistema está tudo limpo. Agora você pode tentar criar uma configuração de serviço de nuvem e ainda usar o aplicativo JWT existente. Não há necessidade de criar um aplicativo, em vez de atualizar a chave pública da configuração de nuvem recém-criada.

>[!NOTE]
>
>Não modifique configurações geradas automaticamente.


## Problema de visibilidade do locatário do aplicativo JWT do Developer Connection {#developer-connection-jwt-application-tenant-visibility-issue}

Se ativado `https://legacy-oauth.cloud.adobe.io/`, todas as organizações (locatários) para as quais os usuários atuais têm o administrador do sistema são listadas. Se você não encontrar o nome da organização aqui ou não puder criar um aplicativo para um locatário necessário aqui, verifique se você tem direitos suficientes (administrador do sistema).

Há um problema conhecido nessa interface do usuário que para qualquer locatário, somente dez aplicativos principais estão visíveis. Ao criar o aplicativo, mantenha-se nessa página e marque o URL. Não é necessário acessar a página de listagem do aplicativo e encontrar o aplicativo que você criou. Você pode pressionar este URL marcado diretamente e atualizar/excluir o aplicativo, sempre que necessário.

O aplicativo JWT pode não estar listado adequadamente. Portanto, é recomendável anotar/marcar o URL ao criar o aplicativo JWT.

## A execução da configuração para de funcionar {#running-configuration-stops-working}

<!--
Comment Type: draft

<p>If the running configuration stops working, either of the following two possibilities
<g class="gr_ gr_15 gr-alert gr_gramm gr_inline_cards gr_run_anim Grammar multiReplace" data-gr-id="15" id="15" style="font-size: 12px;">
are
</g> there:</p>
<p>1.
<g class="gr_ gr_14 gr-alert gr_gramm gr_inline_cards gr_run_anim Grammar only-ins doubleReplace replaceWithoutSep" data-gr-id="14" id="14">
Connection
</g> has failed, or</p>
<p>2. Publish has failed with permission to dam-replication-service denied, while connection has passed </p>
<p>If the connection has failed [1], the
<g class="gr_ gr_10 gr-alert gr_spell gr_inline_cards gr_run_anim ContextualSpelling ins-del multiReplace" data-gr-id="10" id="10">
fail safe
</g> way to fix it is to <a href="../using/troubleshoot-parallel-publishing.md#main-pars-header-1664955658">clean up</a> the existing Brand Portal publish configuration and recreate a publish configuration. </p>
<p>However, if the
<g class="gr_ gr_18 gr-alert gr_spell gr_inline_cards gr_run_anim ContextualSpelling" data-gr-id="18" id="18">
publish
</g> has failed with
<g class="gr_ gr_16 gr-alert gr_gramm gr_inline_cards gr_run_anim Grammar only-ins doubleReplace replaceWithoutSep" data-gr-id="16" id="16">
permission
</g> denied to dam-replication-service, raise a support ticket.</p>
-->

Se um agente de replicação (que estava publicando no Brand Portal muito bem) parar de processar trabalhos de publicação, verifique os logs de replicação. O Experience Manager tem nova tentativa automática incorporada, portanto, se uma publicação de ativo específica falhar, ela será repetida automaticamente. Se houver algum problema intermitente como erro de rede, ele poderá ser bem-sucedido durante a tentativa.

Se houver falhas de publicação contínuas e a fila estiver bloqueada, você deverá verificar **[!UICONTROL testar conexão]** e tentar resolver os erros que estão sendo relatados.

Com base nos erros, é recomendável registrar um tíquete de suporte para que a equipe de engenharia da Brand Portal possa ajudá-lo a resolver os problemas.

## Token de configuração do Brand Portal IMS expirado {#token-expired}

Se o ambiente do Brand Portal para abruptamente, há a possibilidade de as configurações do IMS não funcionarem corretamente. O sistema mostra uma configuração IMS não íntegro e reflete uma mensagem de erro (semelhante à seguinte) de que seu token de acesso expirou.

`com.adobe.granite.auth.oauth.AccessTokenProvider failed to get access token from authorization server status: 400 response: Unknown macro: {"error"}`

Para resolver esse problema, é recomendável salvar e fechar manualmente a configuração do IMS e verificar o status de integridade novamente. Se as configurações não funcionarem, exclua as configurações existentes e crie uma nova.


## Configure os agentes de replicação para evitar o erro de tempo limite de conexão {#connection-timeout}

Geralmente, o trabalho de publicação falha com um erro de tempo limite se houver várias solicitações pendentes na fila de replicação. Para resolver esse problema, verifique se os agentes de replicação estão configurados para evitar o tempo limite.

Para configurar os agentes de replicação:

1. Faça logon na instância do autor do AEM Assets.
1. No **Ferramentas** , navegue até **[!UICONTROL Implantação]** > **[!UICONTROL Replicação]**.
1. Na página Replicação , clique em **[!UICONTROL Agentes do autor]**. Você pode ver os quatro agentes de replicação do seu locatário do Brand Portal.
1. Clique no URL do agente de replicação e clique em **[!UICONTROL Editar]**.
1. Em Configurações do agente , clique no botão **[!UICONTROL Estendido]** guia .
1. Selecione o **[!UICONTROL Fechar Conexão]** caixa de seleção.
1. Repita as etapas 4 a 7 para configurar todos os quatro agentes de replicação.
1. Reinicie o servidor.
