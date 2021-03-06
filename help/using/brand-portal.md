---
title: Visão geral do Experience Manager Assets Brand Portal
seo-title: Overview of Experience Manager Assets Brand Portal
description: O Experience Manager Assets Brand Portal pode ajudá-lo a adquirir, controlar e distribuir com facilidade ativos criativos aprovados para terceiros e usuários de negócios internos em todos os dispositivos.
seo-description: Experience Manager Assets Brand Portal can help you easily acquire, control, and securely distribute approved creative assets to external parties and internal business users across devices.
uuid: b1e54d03-eb2e-488e-af4d-bae817dd135a
content-type: reference
products: SG_EXPERIENCEMANAGER/Brand_Portal
topic-tags: introduction
discoiquuid: 6aefa298-4728-4b8e-a85b-e419ee37f2f4
exl-id: 0f2c45e4-416e-451a-905b-06c5e42a9272
source-git-commit: fb2ce4d39fd9e7aa69ba541bd48a6b9cddd3b4c5
workflow-type: tm+mt
source-wordcount: '1576'
ht-degree: 6%

---

# Visão geral do Experience Manager Assets Brand Portal {#overview-of-aem-assets-brand-portal}

Como profissional de marketing, às vezes é necessário colaborar com parceiros de canal e usuários de negócios internos para criar, gerenciar e fornecer conteúdo digital relevante aos clientes com rapidez. A entrega atempada de conteúdo relevante em toda a jornada do cliente é fundamental para aumentar a demanda, a conversão, o engajamento e a fidelidade do cliente.

Entretanto, é um desafio desenvolver soluções que ofereçam suporte ao compartilhamento eficiente e seguro de logotipos de marcas, diretrizes, ativos de campanha ou capturas de produtos aprovados, com equipes internas estendidas, parceiros e revendedores.

**Adobe Experience Manager (AEM) Assets Brand Portal** O concentra-se na necessidade do comerciante em colaborar com os usuários globais do Brand Portal, fornecendo distribuição de ativos e recursos de contribuição de ativos.

A distribuição de ativos permite que você adquira, controle e distribua com facilidade ativos criativos aprovados a terceiros e usuários de negócios internos em todos os dispositivos. Enquanto isso, a contribuição de ativos permite que os usuários do Brand Portal façam upload de ativos no Brand Portal e publiquem no Experience Manager Assets, sem precisar acessar o ambiente de criação. O recurso de contribuição é chamado como **Origem de ativos no Brand Portal**. E, em conjunto, melhora a experiência geral da Brand Portal de distribuição de ativos e contribuição dos usuários da Brand Portal (agências/equipes externas), acelera o tempo de comercialização de ativos e reduz o risco de não conformidade e acesso não autorizado.
Consulte [Origem de ativos no Brand Portal](brand-portal-asset-sourcing.md).

O ambiente de portal baseado em navegador permite fazer upload, navegar, pesquisar, visualizar e exportar ativos facilmente em formatos aprovados.

## Configurar o Experience Manager Assets com o Brand Portal {#configure-brand-portal}

A configuração do Adobe Experience Manager Assets com o Brand Portal permite a publicação de ativos, a distribuição de ativos e os recursos de contribuição de ativos para os usuários do Brand Portal.

>[!NOTE]
>
>A configuração do Experience Manager Assets com Brand Portal é compatível com o Experience Manager Assets as a Cloud Service, Experience Manager Assets 6.3 e superior.

O Experience Manager Assets as a Cloud Service é configurado automaticamente com o Brand Portal ao ativar o Brand Portal no Cloud Manager. O workflow de ativação cria as configurações necessárias no backend e ativa o Brand Portal na mesma organização IMS da instância as a Cloud Service do Experience Manager Assets.

Enquanto isso, o Experience Manager Assets (no local e serviço gerenciado) é configurado manualmente com o Brand Portal usando o Adobe Developer Console, que obtém um token Adobe Identity Management Services (IMS) para autorização do locatário do Brand Portal.

Para obter mais informações, consulte [configuração do Experience Manager Assets com Brand Portal](../using/configure-aem-assets-with-brand-portal.md).

## Personalidades do usuário no Brand Portal {#Personas}

O Brand Portal oferece suporte às seguintes funções de usuário:

* Usuário convidado
* Visualizador
* Editor
* Administrador

A tabela a seguir lista as tarefas que os usuários nessas funções podem realizar:

|  | **Navegar** | **Pesquisar** | **Download** | **Compartilhar pastas** | **Compartilhar uma coleção** | **Compartilhar ativos como um link** | **Acesso às Ferramentas administrativas** |
|--- |--- |--- |--- |--- |--- |--- |--- |
| **Usuário convidado** | ✓* | ✓* | ✓* | x | x | x | x |
| **Visualizador** | ✓ | ✓ | ✓ | x | x | x | x |
| **Editor** | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | x |
| **Administrador** | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ |

>[!NOTE]
>
>Os usuários convidados podem navegar, acessar e pesquisar ativos somente em pastas públicas e coleções.

<!--
&#42; Viewer users can access and download the public assets shared with them, and can add these assets to create their own collections.

>[!NOTE]
>
>There is a known issue that the share link for collections is currently visible to the viewer users. The viewer users does not have the privilege to add users to create a share link. This issue will be fixed in the upcoming release, the option to share link for the collections will not be available to the viewer users.
-->

### Usuário convidado {#guest-user}

O Experience Manager Assets Brand Portal permite [acesso de convidado](#request-access-to-brand-portal) para o Brand Portal. Um usuário convidado não precisa de credenciais para entrar no portal e tem acesso às pastas e coleções públicas. Como usuário convidado, você pode navegar pelos detalhes do ativo e ter uma visualização completa do ativo de membros de pastas e coleções públicas. Você pode pesquisar, baixar e adicionar ativos públicos ao [!UICONTROL Lightbox] coleção.

No entanto, a sessão de convidado impede que você crie coleções e pesquisas salvas e as compartilhe mais. Os usuários em uma sessão de convidado não podem acessar as configurações de pasta e coleção e não podem compartilhar ativos como link. Esta é uma lista de tarefas que um usuário convidado pode executar:

* [Procurar e acessar ativos públicos](browse-assets-brand-portal.md)

* [Pesquisar ativos públicos](brand-portal-searching.md)

* [Baixar ativos públicos](brand-portal-download-assets.md)

* [Adicionar ativos a [!UICONTROL Lightbox]](brand-portal-light-box.md#add-assets-to-lightbox)

Para obter mais informações, consulte [acesso de convidado ao Brand Portal](../using/guest-access.md).

### Visualizador {#viewer}

Usuário do Brand Portal definido em [!DNL Admin Console] que tem acesso ao Brand Portal com a função de Visualizador. Um usuário com essa função pode fazer logon no Brand Portal e acessar pastas, coleções e ativos permitidos. O usuário também pode navegar, visualizar, baixar e exportar ativos (representações originais ou específicas), definir configurações da conta e procurar ativos. Esta é uma lista de tarefas que um Visualizador pode executar:

* [Procurar ativos](browse-assets-brand-portal.md)

* [Pesquisar por ativos](brand-portal-searching.md)

* [Baixar ativos](brand-portal-download-assets.md)

### Editor {#editor}

Um usuário com a função de Editor pode executar todas as tarefas que um Visualizador pode executar. Além disso, o e o Editor podem exibir os arquivos e pastas que um administrador compartilha. O usuário com a função de um Editor também pode compartilhar conteúdo (arquivos, pastas, coleções) com outras pessoas.

Além das tarefas que um Visualizador pode executar, um Editor pode executar as seguintes tarefas adicionais:

* [Compartilhar pastas](brand-portal-sharing-folders.md)

* [Compartilhar uma coleção](brand-portal-share-collection.md)

* [Compartilhar ativos como um link](brand-portal-link-share.md)

### Administrador {#administrator}

Um administrador inclui um usuário marcado como administrador de sistema ou administrador de produto da Brand Portal em [!UICONTROL Admin Console]. Um administrador pode adicionar e remover administradores e usuários do sistema, definir predefinições, enviar emails para usuários e exibir relatórios de uso e armazenamento do portal.

>[!NOTE]
>
>No Brand Portal, um usuário marcado com a função de administrador de suporte no [!UICONTROL Admin Console] tem os mesmos privilégios de um administrador de sistema.

Um administrador pode executar todas as tarefas que um Editor pode executar. Veja a seguir as tarefas adicionais que um administrador pode executar:

* [Gerenciar usuários, grupos e cargos de usuários](brand-portal-adding-users.md)

* [Personalizar papel de parede, cabeçalhos de página e emails](brand-portal-branding.md)

* [Usar facetas de busca personalizada](brand-portal-search-facets.md)

* [Usar o formulário de esquema de metadados](brand-portal-metadata-schemas.md)

* [Aplicar predefinições de imagens ou representações dinâmicas](brand-portal-image-presets.md)

* [Trabalhar com relatórios](brand-portal-reports.md)

Além das tarefas acima, um Autor no AEM Assets pode executar as seguintes tarefas:

* [Configurar o AEM Assets com o Brand Portal](../using/configure-aem-assets-with-brand-portal.md)

* [Publicar pastas no Brand Portal](https://experienceleague.adobe.com/docs/experience-manager-65/assets/brandportal/brand-portal-publish-folder.html)

* [Publicar coleções no Brand Portal](https://experienceleague.adobe.com/docs/experience-manager-65/assets/brandportal/brand-portal-publish-collection.html)

## Alias alternativo para o url do Brand Portal {#tenant-alias-for-portal-url}

A partir do Brand Portal 6.4.3, as organizações podem ter um URL alternativo (alias) para o URL existente do locatário do Brand Portal. O URL de alias pode ser criado com um prefixo alternativo no URL.\
Observe que somente o prefixo do URL do Brand Portal pode ser personalizado e não o URL inteiro. Por exemplo, uma organização com domínio existente `geomettrix.brand-portal.adobe.com` pode obter `geomettrixinc.brand-portal.adobe.com` criado mediante solicitação.

No entanto, a instância do autor do AEM pode ser [configurado](../using/configure-aem-assets-with-brand-portal.md) somente com o URL da id do locatário e não com o URL do alias do locatário (alternativo).

>[!NOTE]
>
>Para obter um alias para o nome do locatário no URL do portal existente, as organizações precisam entrar em contato com o Suporte ao cliente com uma nova solicitação de criação de alias do locatário. Essa solicitação é processada verificando primeiro se o alias está disponível e criando o alias.
>
>Para substituir o alias antigo ou excluí-lo, é necessário seguir o mesmo processo.

## Solicitar acesso ao Brand Portal {#request-access-to-brand-portal}

Os usuários podem solicitar acesso ao Brand Portal a partir da tela de logon. Essas solicitações são enviadas para administradores do Brand Portal, que concedem acesso aos usuários por meio do Adobe [!UICONTROL Admin Console]. Após o acesso ser concedido, os usuários recebem um email de notificação.

Para solicitar acesso, faça o seguinte:

1. Na página de logon da Brand Portal, selecione **[!UICONTROL Clique aqui]** correspondente a **[!UICONTROL Precisa de acesso?]**. No entanto, para entrar na sessão de convidado, selecione o **[!UICONTROL Clique aqui]** correspondente a **[!UICONTROL Acesso de convidado?]**.

   ![Tela de logon do Brand Portal](assets/bp-login-requestaccess.png)

   O [!UICONTROL Solicitar acesso] será aberta.

1. Para solicitar acesso à Brand Portal de uma organização, você deve ter uma [!UICONTROL Adobe ID], [!UICONTROL Enterprise ID]ou [!UICONTROL Federated ID].

   No [!UICONTROL Solicitar acesso] , faça logon usando sua ID (cenário 1) ou crie um [!UICONTROL Adobe ID] (cenário 2):

   ![[!UICONTROL Solicitar acesso]](assets/bplogin_request_access_2.png)

   **Cenário 1**

   1. Se você tiver uma [!UICONTROL Adobe ID], [!UICONTROL Enterprise ID]ou [!UICONTROL Federated ID], clique em **[!UICONTROL Fazer logon]**.
O [!UICONTROL Fazer logon] será aberta.

   1. Forneça sua [!UICONTROL Adobe ID] credenciais e clique em **[!UICONTROL Fazer logon]**.

      ![Logon no Adobe](assets/bplogin_request_access_3.png)
   Você é redirecionado para a função [!UICONTROL Solicitar acesso] página.

   **Cenário 2**

   1. Se você não tiver um [!UICONTROL Adobe ID], para criar um, clique em **[!UICONTROL Obter uma Adobe ID]** do [!UICONTROL Solicitar acesso] página.
O [!UICONTROL Fazer logon] será aberta.
   1. Clique em **[!UICONTROL Obter uma Adobe ID]**.
O [!UICONTROL Cadastrar-se] será aberta.
   1. Insira seu nome e sobrenome, ID de email e senha.
   1. Selecionar **[!UICONTROL Cadastrar-se]**.

      ![](assets/bplogin_request_access_5.png)
   Você é redirecionado para a função [!UICONTROL Solicitar acesso] página.

1. A próxima página exibe seu nome e a ID de email usada para solicitar acesso. Deixe um comentário para o administrador e clique em **[!UICONTROL Enviar]**.

   ![](assets/bplogin-request-access.png)

## Os administradores de produtos concedem acesso {#grant-access-to-brand-portal}

Os administradores de produtos do Brand Portal recebem solicitações de acesso na área de notificação do Brand Portal e por meio de emails na caixa de entrada.

![Acesso à notificação solicitada](assets/bplogin_request_access_7.png)

Para conceder acesso, os administradores do produto precisam clicar na notificação relevante na área de notificação do Brand Portal e, em seguida, clicar em **[!UICONTROL Conceder acesso]**.
Como alternativa, os administradores de produto podem seguir o link fornecido no email de solicitação de acesso para visitar o Adobe [!UICONTROL Admin Console] e adicionar o usuário à configuração de produto relevante.

Você é redirecionado para a função [Adobe [!UICONTROL Admin Console]](https://adminconsole.adobe.com/enterprise/overview) página inicial. Use o Adobe [!UICONTROL Admin Console] para criar usuários e atribuí-los a perfis de produto (conhecidos anteriormente como configurações de produto), que são exibidos como grupos no Brand Portal. Para obter mais informações sobre como adicionar usuários em [!UICONTROL Admin Console], consulte [Adicionar um usuário](brand-portal-adding-users.md#add-a-user) (siga as Etapas 4 a 7 no procedimento para adicionar um usuário).

## Idiomas do Brand Portal {#brand-portal-language}

Você pode alterar o idioma Brand Portal do Adobe [!UICONTROL Configurações do Experience Cloud].

![Acesso à notificação solicitada](assets/BPLang.png)

Para alterar o idioma:

1. Selecionar [!UICONTROL Usuário] > [!UICONTROL Editar perfil] no menu superior.

   ![Editar perfil](assets/EditBPProfile.png)

1. Ligado [!UICONTROL Configurações do Experience Cloud] selecione um idioma na página [!UICONTROL Idioma] menu suspenso.

## Notificação de manutenção do Brand Portal {#brand-portal-maintenance-notification}

Antes da Brand Portal ser agendada para manutenção, uma notificação é exibida como um banner depois que você faz logon no Brand Portal. Um exemplo de notificação:

![](assets/bp_maintenance_notification.png)

É possível ignorar esta notificação e continuar usando o Brand Portal. Essa notificação é exibida em cada nova sessão.

## Informações sobre a versão e o sistema {#release-and-system-information}

* [Novidades](whats-new.md)
* [Notas de versão](brand-portal-release-notes.md)
* [Formatos de arquivo não compatíveis](brand-portal-supported-formats.md)

## Recursos relacionados {#related-resources}

<!--
* [Adobe Customer Support]()
-->

* [Fóruns do AEM](https://experienceleaguecommunities.adobe.com/t5/adobe-experience-manager/ct-p/adobe-experience-manager-community)
