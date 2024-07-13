---
title: Acesso de convidado ao Brand Portal
seo-title: Guest Access to Brand Portal
description: Permita o acesso dos visitantes e economize o esforço para integrar vários usuários sem autenticação.
seo-description: Allow guest access and save the effort to onboard numerous users without authentication.
uuid: edb4378d-1710-44a2-97a6-594d99f62fff
contentOwner: VG
topic-tags: introduction
content-type: reference
products: SG_EXPERIENCEMANAGER/Brand_Portal
discoiquuid: b9e9fe7b-0373-42d1-851b-7c76b47657c2
exl-id: ecce0a45-abae-41c4-9ea7-5dfdcf19e5ea
source-git-commit: 0670b8d372fd2dc5bdb1d0a928601e3e09a6dcf9
workflow-type: tm+mt
source-wordcount: '1040'
ht-degree: 0%

---

# Acesso de convidado ao Brand Portal {#guest-access-to-brand-portal}

O Experience Manager Assets Brand Portal permite o acesso de visitantes ao portal. Um usuário convidado não precisa de credenciais para entrar no portal e tem acesso aos ativos públicos (e coleções) do portal. Os usuários na sessão de convidado podem adicionar ativos ao lightbox (coleção privada) e baixá-los até que a sessão dure ou até que o usuário convidado opte por [[!UICONTROL Encerrar sessão]](#exit-guest-session). Uma sessão de usuário convidado permanece ativa por 15 minutos.

A funcionalidade de acesso de convidado permite que as organizações [compartilhem rapidamente os ativos aprovados](../using/brand-portal-sharing-folders.md#how-to-share-folders) com o público-alvo desejado em escala sem precisar integrá-los. O Brand Portal 6.4.2 em diante está equipado para atender vários usuários convidados simultâneos, o que representa 10% da cota total de usuários por organização. Permitir o acesso do convidado economiza tempo para gerenciar e integrar pontuações de usuários com funcionalidades limitadas no Brand Portal.\
As organizações podem habilitar (ou desabilitar) o acesso de convidado na conta da Brand Portal da organização usando a opção **[!UICONTROL Permitir acesso de convidado]** das configurações de **[!UICONTROL Acesso]** no painel de ferramentas administrativas.

<!--
Comment Type: annotation
Last Modified By: mgulati
Last Modified Date: 2018-08-17T10:42:59.879-0400
Removed the first para: "AEM Assets Brand Portal allows public users to enter the portal anonymously and have restricted access to the allowed public resources as guests. Organization users with guest role need not seek access and authentication from administrators."
-->

![](assets/enable-guest-access.png)

## Iniciar sessão de convidado {#begin-guest-session}

Para entrar no Brand Portal anonimamente, selecione **[!UICONTROL Clique aqui]** correspondente a **[!UICONTROL Acesso de Convidado?]** na tela de boas-vindas do Brand Portal. Insira a verificação de segurança captcha para conceder acesso ao uso do Brand Portal.

![](assets/bp-login-screen.png)

## Duração da sessão de convidado {#guest-session-duration}

Uma sessão de usuário convidado permanece ativa por 15 minutos.
Isso significa que o estado da **[!UICONTROL Lightbox]** é preservado por 15 minutos a partir da hora de início da sessão e, depois disso, a sessão de convidado atual é reiniciada para que o estado da Lightbox seja perdido.

Por exemplo, um usuário convidado faz logon no Brand Portal às 1500 horas e adiciona ativos à **[!UICONTROL Lightbox]** para download às 15:05 horas. Se o usuário não baixar a coleção **[!UICONTROL Lightbox]** (ou seus ativos) antes das 15h15 (dentro de 15 minutos do logon), ele terá que reiniciar a sessão. A **[!UICONTROL Lightbox]** está vazia, o que significa que os ativos carregados não estarão mais disponíveis se a sessão tiver sido perdida.

## Sessões de convidado simultâneas permitidas {#concurrent-guest-sessions-allowed}

O número de sessões de convidados simultâneas é limitado a 10% da cota total de usuários por organização. Isso significa que para uma organização com cota de usuário de 200, no máximo 20 usuários convidados podem trabalhar ao mesmo tempo. O 21º usuário tem o acesso negado e poderá acessá-lo como convidado somente se a sessão de qualquer um dos 20 usuários convidados ativos terminar.

>[!NOTE]
>
>O Brand Portal não envia notificação se o número de usuários licenciados exceder o valor contratado (cota). Além disso, não restringe nenhuma atividade dos usuários licenciados.

## Interação de usuário convidado com o Brand Portal {#guest-user-interaction-with-brand-portal}

### Navegação da interface do usuário do convidado

Ao inserir o Brand Portal como convidado, os usuários podem ver todos os [ativos e pastas compartilhados](../using/brand-portal-sharing-folders.md#sharefolders) publicamente ou exclusivamente com usuários convidados. Essa visualização é a visualização somente conteúdo, que exibe ativos em qualquer um dos layouts do cartão, lista ou coluna.

![](assets/disabled-folder-hierarchy1.png)

No entanto, os usuários convidados verão a árvore de pastas (a partir da pasta raiz) e as pastas compartilhadas organizadas nas respectivas pastas pai ao fazer logon na Brand Portal, se os administradores tiverem habilitado a configuração [Habilitar Hierarquia de Pastas](../using/brand-portal-general-configuration.md#main-pars-header-1621071021).

Essas pastas principais são as pastas virtuais e nenhuma ação pode ser executada nelas. Você pode reconhecer essas pastas virtuais com um ícone de cadeado.

Nenhuma tarefa de ação está visível ao passar o cursor sobre elas ou selecioná-las na **[!UICONTROL Exibição de Cartão]**, ao contrário das pastas compartilhadas. O botão **[!UICONTROL Visão Geral]** é mostrado ao selecionar uma pasta virtual na **[!UICONTROL Exibição de Coluna]** e na **[!UICONTROL Exibição de Lista]**.

>[!NOTE]
>
>A miniatura padrão das pastas virtuais é a imagem em miniatura da primeira pasta compartilhada.

![](assets/enabled-hierarchy1.png) ![](assets/hierarchy1-nonadmin.png) ![](assets/hierarchy-nonadmin.png) ![](assets/hierarchy2-nonadmin.png)

A opção **[!UICONTROL Configurações de Exibição]** permite que os usuários convidados ajustem tamanhos de cartão em **[!UICONTROL Exibição de Cartão]** ou colunas para exibição em **[!UICONTROL Exibição de Lista]**.

![](assets/nav-guest-user.png)

A **[!UICONTROL árvore de conteúdo]** permite mover pela hierarquia de ativos.

![](assets/guest-login-ui.png)

A Brand Portal fornece a opção **[!UICONTROL Visão geral]** para que os usuários convidados visualizem **[!UICONTROL Propriedades do ativo]** de ativos/pastas selecionados. A opção **[!UICONTROL Visão geral]** está visível:

* Na barra de ferramentas na parte superior, ao selecionar um ativo/pasta.
* Na lista suspensa em Selecionar o seletor de painéis.

Ao selecionar a opção **[!UICONTROL Visão geral]** enquanto um ativo/pasta é selecionado, os usuários podem ver o título, o caminho e a hora da criação do ativo. Já na página de detalhes do ativo, a seleção da opção **[!UICONTROL Visão geral]** permite que os usuários vejam os metadados do ativo.

![](assets/overview-option-1.png)

![](assets/overview-rail-selector-1.png)

A opção **[!UICONTROL Navegação]** no painel esquerdo permite navegar dos arquivos para as coleções e de volta na sessão de convidado para que os usuários possam navegar pelos ativos em arquivos ou coleções.

A opção **[!UICONTROL Filtrar]** permite que usuários convidados filtrem arquivos e pastas de ativos usando predicados de pesquisa definidos pelo administrador.

### Recursos do usuário convidado

Os usuários convidados podem acessar ativos públicos no Brand Portal e também ter algumas restrições, conforme discutido posteriormente.

**Os usuários convidados podem**:

* Acesse todas as pastas e coleções públicas destinadas a todos os usuários do Brand Portal.
* Procurar membros, página de detalhes e ter exibição completa do ativo dos membros de todas as pastas e coleções públicas.
* Pesquisar ativos em pastas e coleções públicas.
* Adicionar ativos à coleção lightbox. Essas alterações na coleção persistem durante a sessão.
* Baixe ativos diretamente ou por meio da coleção lightbox.

**Usuários convidados não podem**:

* Crie coleções e pesquisas salvas, ou compartilhe-as ainda mais.
* Acessar configurações de pasta e coleções.
* Compartilhar ativos como links.

### Baixar ativos na sessão de convidado

Os usuários convidados podem baixar diretamente os ativos compartilhados pública ou exclusivamente com usuários convidados no Brand Portal. Os usuários convidados também podem adicionar ativos à **[!UICONTROL Lightbox]** (coleção pública) e baixar a coleção **[!UICONTROL Lightbox]** antes que a sessão expire.

Para baixar ativos e coleções, use o ícone de download de:

* Miniaturas de ação rápida, que aparecem ao passar o mouse sobre o ativo ou a coleção
* A barra de ferramentas na parte superior, que aparece ao selecionar o ativo ou a coleção

![](assets/download-on-guest.png)

Selecionar **[!UICONTROL Habilitar aceleração de download]** na caixa de diálogo [!UICONTROL Download] permite [aprimorar o desempenho do download](../using/accelerated-download.md).

## Sair da sessão de convidado {#exit-guest-session}

Para sair de uma sessão de convidado, use **[!UICONTROL Encerrar Sessão]** nas opções disponíveis no cabeçalho. No entanto, se a guia do navegador usada para a sessão do convidado estiver inativa, a sessão expirará automaticamente após duas horas de inatividade.

![](assets/end-guest-session.png)

## Monitoramento de atividades do usuário convidado {#monitoring-guest-user-activities}

Os administradores podem monitorar a interação do usuário convidado com a Brand Portal. Os relatórios gerados no Brand Portal podem fornecer insights importantes sobre as atividades do usuário convidado. Por exemplo, o relatório **[!UICONTROL Download]** pode ser usado para rastrear a contagem de ativos baixados pelo usuário convidado. O relatório **[!UICONTROL Logons de Usuário]** pode informar quando o usuário convidado fez logon no portal pela última vez e a frequência de logons em uma duração especificada.
