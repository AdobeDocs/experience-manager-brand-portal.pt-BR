---
title: Solucionar problemas na publicação paralela no Brand Portal
seo-title: Troubleshoot issues in parallel publishing to Brand Portal
description: Solucionar problemas de publicação paralela.
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
source-wordcount: '960'
ht-degree: 0%

---

# Solucionar problemas na publicação paralela no Brand Portal {#troubleshoot-issues-in-parallel-publishing-to-brand-portal}

O Brand Portal está configurado com o Experience Manager Assets para ter os ativos de marca aprovados assimilados (ou publicados) facilmente da instância de autor do Experience Manager Assets. Depois de [configurado](../using/configure-aem-assets-with-brand-portal.md), o Autor do Experience Manager usa um agente de replicação para replicar o(s) ativo(s) selecionado(s) no Brand Portal Cloud Service para uso aprovado pelos usuários do Brand Portal. Vários agentes de replicação são usados no Experience Manager 6.2 SP1-CFP5, Experience Manager CFP 6.3.0.2 e posteriores para permitir a publicação paralela de alta velocidade.

>[!NOTE]
>
>A Adobe recomenda o upgrade para o Experience Manager 6.4.1.0 a fim de garantir que o Experience Manager Assets Brand Portal seja configurado corretamente com o Experience Manager Assets. Uma limitação no Experience Manager 6.4 gera um erro ao configurar o Experience Manager Assets com o Brand Portal e a replicação falha.

Ao configurar o serviço de nuvem para o Brand Portal em **[!UICONTROL /etc/cloudservice]**, todos os usuários e tokens necessários são gerados automaticamente e salvos no repositório. A configuração do serviço em nuvem é criada, os usuários do serviço necessários para a replicação e os agentes de replicação para replicar o conteúdo também são criados. Ele cria quatro agentes de replicação. Portanto, ao publicar vários ativos do Experience Manager para o Brand Portal, os ativos são enfileirados e distribuídos entre os agentes de replicação por meio do Round Robin.

No entanto, a publicação pode falhar intermitentemente devido a: grandes trabalhos de sling, aumento da E/S de Rede e **[!UICONTROL Disco]** na instância do Autor do Experience Manager ou desempenho lento da instância do Autor do Experience Manager. Portanto, é recomendável testar a conexão com os agentes de replicação antes de começar a publicar.

![](assets/test-connection.png)

## Solucionar falhas na primeira publicação: validação da configuração de publicação {#troubleshoot-failures-in-first-time-publishing-validating-your-publish-configuration}

Para validar as configurações de publicação:

1. Verifique os logs de erro
1. Verifique se o agente de replicação foi criado
1. Testar conexão

**Registros finais ao criar o Cloud Service**

Verifique os logs finais. Verifique se o agente de replicação foi criado ou não. Se a criação do agente de replicação falhar, edite o Cloud Service fazendo pequenas alterações nele. Valide e verifique novamente se o agente de replicação foi criado ou não. Caso contrário, edite novamente o serviço.

Se, durante a edição repetida do serviço de nuvem, ele não estiver configurado corretamente, relate um tíquete de creche.

**Testar conexão com agentes de replicação**

Exibir log, se erros forem encontrados no log de replicação:

1. Entre em contato com o Suporte ao cliente.

1. Tente [limpar](../using/troubleshoot-parallel-publishing.md#clean-up-existing-config) novamente e crie a configuração de publicação novamente.

<!--
Comment Type: remark
Last Modified By: Mini Gulati (mgulati)
Last Modified Date: 2018-06-21T22:56:21.256-0400
<p>?? check and compare public key. At times public key is different</p>
<p>?? another thing to check in /useradmin</p>
-->

## Limpar configurações de publicação existentes do Brand Portal {#clean-up-existing-config}

Na maioria das vezes, quando a publicação não está funcionando, o motivo pode ser que o usuário que está publicando (por exemplo: `mac-<tenantid>-replication` não tem a chave privada mais recente e, portanto, a publicação falha com o erro &quot;401 não autorizado&quot; e nenhum outro erro é relatado nos logs do agente de replicação. Você pode evitar a solução de problemas e criar uma configuração. Para que a nova configuração funcione corretamente, limpe o seguinte da configuração do autor do Experience Manager:

1. Ir para `localhost:4502/crx/de/` (considerando que você está executando a instância do autor no host local:4502:\
   i. excluir `/etc/replication/agents.author/mp_replication`
ii) excluir `/etc/cloudservices/mediaportal/<config_name>`

1. Vá para localhost:4502/useradmin:\
   i. pesquisar usuário `mac-<tenantid>replication`
ii) excluir este usuário

Agora o sistema está totalmente limpo. Agora você pode tentar criar uma configuração de serviço em nuvem e ainda usar o aplicativo JWT existente. Não há necessidade de criar um aplicativo, mas de atualizar a chave pública da configuração de nuvem recém-criada.

>[!NOTE]
>
>Não modifique nenhuma configuração gerada automaticamente.


## Problema de visibilidade do locatário do aplicativo JWT da conexão do desenvolvedor {#developer-connection-jwt-application-tenant-visibility-issue}

Se em `https://legacy-oauth.cloud.adobe.io/`, todas as organizações (locatários) para as quais os usuários atuais mantêm o administrador do sistema serão listadas. Se você não encontrar o nome da organização aqui ou não puder criar um aplicativo para um locatário necessário aqui, verifique se você tem direitos suficientes (administrador do sistema).

Há um problema conhecido nessa interface de usuário que, para qualquer locatário, somente os dez principais aplicativos ficam visíveis. Ao criar o aplicativo, permaneça nessa página e marque o URL como favorito. Não é necessário ir para a página de listagem do aplicativo e localizar o aplicativo criado. Você pode acessar esse URL marcado diretamente e atualizar/excluir o aplicativo sempre que necessário.

O aplicativo JWT pode não estar listado corretamente. Portanto, é recomendável anotar/marcar o URL ao criar um aplicativo JWT.

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

Se um agente de replicação (que estava sendo publicado no Brand Portal sem problemas) parar de processar trabalhos de publicação, verifique os logs de replicação. O Experience Manager tem repetição automática integrada, portanto, se uma publicação de ativo específica falhar, ela será repetida automaticamente. Se houver algum problema intermitente, como erro de rede, ele poderá ser bem-sucedido durante a repetição.

Se houver falhas contínuas de publicação e a fila estiver bloqueada, verifique a **[!UICONTROL conexão de teste]** e tente resolver os erros que estão sendo relatados.

Com base nos erros, é recomendável registrar um tíquete de suporte, para que a equipe de engenharia da Brand Portal possa ajudá-lo a resolver problemas.

## O token de configuração do Brand Portal IMS expirou {#token-expired}

Se o ambiente do Brand Portal for interrompido abruptamente, há uma possibilidade de que as configurações do IMS não estejam funcionando corretamente. O sistema mostra uma configuração IMS não íntegra e reflete uma mensagem de erro (semelhante à seguinte) de que o token de acesso expirou.

`com.adobe.granite.auth.oauth.AccessTokenProvider failed to get access token from authorization server status: 400 response: Unknown macro: {"error"}`

Para resolver esse problema, é recomendável salvar e fechar manualmente a configuração do IMS e verificar o status de integridade novamente. Se as configurações não funcionarem, exclua as configurações existentes e crie uma nova.


## Configure agentes de replicação para evitar erro de tempo limite de conexão {#connection-timeout}

Normalmente, o trabalho de publicação falha com um erro de tempo limite se houver várias solicitações pendentes na fila de replicação. Para resolver esse problema, verifique se os agentes de replicação estão configurados para evitar o tempo limite.

Para configurar os agentes de replicação:

1. Faça logon na instância de autor do AEM Assets.
1. No painel **Ferramentas**, navegue até **[!UICONTROL Implantação]** > **[!UICONTROL Replicação]**.
1. Na página Replicação, clique em **[!UICONTROL Agentes no autor]**. Você pode ver os quatro agentes de replicação do seu locatário do Brand Portal.
1. Clique na URL do agente de replicação e em **[!UICONTROL Editar]**.
1. Em Configurações do Agente, clique na guia **[!UICONTROL Estendido]**.
1. Marque a caixa de seleção **[!UICONTROL Fechar Conexão]**.
1. Repita as etapas de 4 a 7 para configurar todos os quatro agentes de replicação.
1. Reinicie o servidor.
