---
title: Acesso de convidado ao Brand Portal
seo-title: Guest Access to Brand Portal
description: Permita acesso de convidado e poupe o esforço para integrar vários usuários sem autenticação.
seo-description: Allow guest access and save the effort to onboard numerous users without authentication.
uuid: edb4378d-1710-44a2-97a6-594d99f62fff
contentOwner: VG
topic-tags: introduction
content-type: reference
products: SG_EXPERIENCEMANAGER/Brand_Portal
discoiquuid: b9e9fe7b-0373-42d1-851b-7c76b47657c2
exl-id: ecce0a45-abae-41c4-9ea7-5dfdcf19e5ea
source-git-commit: 51dc6f9c3b3a59751d7910513279e52906d97b88
workflow-type: tm+mt
source-wordcount: '1026'
ht-degree: 0%

---

# Acesso de convidado ao Brand Portal {#guest-access-to-brand-portal}

O Experience Manager Assets Brand Portal permite acesso de convidado ao portal. Um usuário convidado não precisa de credenciais para entrar no portal e tem acesso aos ativos públicos (e coleções) do portal. Os usuários na sessão de convidado podem adicionar ativos ao lightbox (coleção privada) e baixar o mesmo até que sua sessão dure, o que é 2 horas a partir do início da sessão, a menos que o usuário convidado escolha [[!UICONTROL Sessão final]](#exit-guest-session).

A funcionalidade de acesso de convidado permite que as organizações [compartilhem rapidamente os ativos aprovados](../using/brand-portal-sharing-folders.md#how-to-share-folders) com o público-alvo desejado em escala sem ter que incorporá-los. O Brand Portal 6.4.2 em diante é equipado para atender vários usuários convidados simultâneos, que é 10% da cota total de usuários por organização. Permitir o acesso de convidado economiza tempo para gerenciar e pontuações de usuários integrados com funcionalidades limitadas no Brand Portal.\
As organizações podem habilitar (ou desabilitar) o acesso de convidado na conta Brand Portal da organização usando a opção **[!UICONTROL Permitir acesso de convidado]** nas configurações de **[!UICONTROL Acesso]** no painel de ferramentas administrativas.

<!--
Comment Type: annotation
Last Modified By: mgulati
Last Modified Date: 2018-08-17T10:42:59.879-0400
Removed the first para: "AEM Assets Brand Portal allows public users to enter the portal anonymously and have restricted access to the allowed public resources as guests. Organization users with guest role need not seek access and authentication from administrators."
-->

![](assets/enable-guest-access.png)

## Iniciar sessão de convidado {#begin-guest-session}

Para inserir o Brand Portal anonimamente, selecione **[!UICONTROL Clique aqui]** correspondente a **[!UICONTROL Acesso de Convidado?]** na tela de boas-vindas do Brand Portal. Insira a verificação de segurança do captcha para conceder acesso para usar o Brand Portal.

![](assets/bp-login-screen.png)

## Duração da sessão de convidado {#guest-session-duration}


Uma sessão de usuário convidado permanece ativa por 15 minutos.
Isso significa que o estado do **[!UICONTROL Lightbox]** é preservado por 15 minutos da hora de início da sessão e, depois disso, a sessão de convidado atual é reiniciada para que o estado do Lightbox seja perdido.

Por exemplo, um usuário convidado faz logon no Brand Portal às 1500 horas e adiciona ativos a **[!UICONTROL Lightbox]** para download às 15:05 horas. Se o usuário não baixar a coleção **[!UICONTROL Lightbox]** (ou seus ativos) antes de 15:15 horas (dentro de 15 minutos do logon), ele precisará reiniciar a sessão. O **[!UICONTROL Lightbox]** está vazio, o que significa que os ativos carregados não estarão mais disponíveis se a sessão tiver sido perdida.

## Sessões de convidado simultâneas permitidas {#concurrent-guest-sessions-allowed}

O número de sessões de convidado simultâneas é limitado a 10% da cota total de usuários por organização. Significa que para uma organização com cota de usuário de 200, no máximo 20 usuários convidados podem trabalhar ao mesmo tempo. O 21º usuário tem acesso negado e só pode acessar como convidado se a sessão de qualquer um dos 20 usuários convidados ativos terminar.

>[!NOTE]
>
>A Brand Portal não envia notificação se o número de usuários licenciados exceder o valor contratado (cota). Além disso, não restringe nenhuma atividade dos usuários licenciados.

## Interação do usuário convidado com o Brand Portal {#guest-user-interaction-with-brand-portal}

### Navegação da interface de usuário do convidado

Ao entrar na Brand Portal como convidado, os usuários podem ver todos os [ativos e pastas compartilhados](../using/brand-portal-sharing-folders.md#sharefolders) publicamente ou com usuários convidados exclusivamente. Essa exibição é a exibição somente conteúdo, que exibe ativos em qualquer um dos layouts de cartão, lista ou coluna.

![](assets/disabled-folder-hierarchy1.png)

No entanto, os usuários convidados veem a árvore de pastas (começando pela pasta raiz) e as pastas compartilhadas organizadas em suas respectivas pastas pai ao fazer logon na Brand Portal, se os administradores tiverem ativado a configuração [Ativar hierarquia de pastas](../using/brand-portal-general-configuration.md#main-pars-header-1621071021).

Essas pastas pai são as pastas virtuais e nenhuma ação pode ser executada nelas. Você pode reconhecer essas pastas virtuais com um ícone de cadeado.

Nenhuma tarefa de ação é visível ao passar o mouse ou selecioná-la em **[!UICONTROL Exibição de cartão]**, ao contrário das pastas compartilhadas. **** O botão Visão geral é exibido ao selecionar uma pasta virtual na  **[!UICONTROL Exibição de]** coluna e Exibição  **[!UICONTROL de lista]**.

>[!NOTE]
>
>A miniatura padrão das pastas virtuais é a imagem em miniatura da primeira pasta compartilhada.

![](assets/enabled-hierarchy1.png) ![](assets/hierarchy1-nonadmin.png) ![](assets/hierarchy-nonadmin.png) ![](assets/hierarchy2-nonadmin.png)

**[!UICONTROL A opção Exibir]** configurações permite que os usuários convidados ajustem os tamanhos dos cartões nas colunas  **[!UICONTROL Visualizador de]** cartão a serem exibidas na Exibição  **[!UICONTROL de lista]**.

![](assets/nav-guest-user.png)

A **[!UICONTROL Árvore de conteúdo]** permite percorrer a hierarquia de ativos.

![](assets/guest-login-ui.png)

O Brand Portal fornece a opção **[!UICONTROL Visão geral]** para os usuários convidados visualizarem **[!UICONTROL Propriedades do ativo]** dos ativos/pastas selecionados. A opção **[!UICONTROL Visão geral]** está visível:

* Na barra de ferramentas, na parte superior, ao selecionar um ativo/pasta.
* Na lista suspensa ao selecionar o Seletor de painéis.

Ao selecionar a opção **[!UICONTROL Visão geral]** enquanto um ativo/pasta é selecionado, os usuários podem ver o título, o caminho e o horário da criação do ativo. Enquanto na página de detalhes do ativo, selecionar a opção **[!UICONTROL Visão geral]** permite que os usuários vejam os metadados do ativo.

![](assets/overview-option-1.png)

![](assets/overview-rail-selector-1.png)

**** A opção Navegação no painel esquerdo permite navegar de arquivos para coleções e de volta na sessão de convidado, para que os usuários possam navegar pelos ativos em arquivos ou coleções.

**** A opção Filtrar permite que usuários convidados filtrem arquivos de ativos e pastas usando predicados de pesquisa definidos pelo administrador.

### Recursos do usuário convidado

Os usuários convidados podem acessar ativos públicos no Brand Portal e também ter poucas restrições, conforme discutido ainda mais.

**Os usuários convidados podem**:

* Acesse todas as pastas públicas e coleções destinadas a todos os usuários do Brand Portal.
* Pesquise membros, página de detalhes e tenha uma visualização completa de ativos dos membros de todas as pastas públicas e coleções.
* Pesquise ativos em pastas públicas e coleções.
* Adicione ativos à coleção lightbox. Essas alterações na coleção persistem durante a sessão.
* Baixe ativos diretamente ou por meio da coleção lightbox.

**Usuários convidados não podem**:

* Crie coleções e pesquisas salvas, ou compartilhe-as ainda mais.
* Acesse as configurações de pasta e coleções.
* Compartilhar ativos como links.

### Baixar ativos na sessão de convidado

Os usuários convidados podem baixar diretamente ativos compartilhados publicamente ou exclusivamente com usuários convidados no Brand Portal. Os usuários convidados também podem adicionar ativos a **[!UICONTROL Lightbox]** (coleção pública) e baixar a coleção **[!UICONTROL Lightbox]** antes que a sessão expire.

Para baixar ativos e coleções, use o ícone de download de:

* Miniaturas de ação rápida, que aparecem ao passar o mouse sobre o ativo ou a coleção
* A barra de ferramentas na parte superior, que aparece ao selecionar o ativo ou a coleção

![](assets/download-on-guest.png)

Selecionar **[!UICONTROL Ativar aceleração de download]** na caixa de diálogo [!UICONTROL Baixar] permite [melhorar o desempenho de download](../using/accelerated-download.md).

## Sessão de convidado de saída {#exit-guest-session}

Para sair de uma sessão de convidado, use **[!UICONTROL End Session]** a partir das opções disponíveis no cabeçalho. No entanto, se a guia do navegador usada para a sessão de convidado estiver inativa, a sessão expirará automaticamente após duas horas de inatividade.

![](assets/end-guest-session.png)

## Monitorar atividades de usuário convidado {#monitoring-guest-user-activities}

Os administradores podem monitorar a interação do usuário convidado com a Brand Portal. Os relatórios gerados no Brand Portal podem fornecer informações importantes sobre atividades de usuários convidados. Por exemplo, o relatório **[!UICONTROL Download]** pode ser usado para rastrear a contagem de ativos baixados pelo usuário convidado. **[!UICONTROL Relatório de]** logins do usuário pode informar quando o usuário convidado fez logon pela última vez no portal e a frequência de logons em uma duração especificada.
