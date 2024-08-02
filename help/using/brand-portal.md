---
title: Visão geral do Experience Manager Assets Brand Portal
description: Saiba como o Experience Manager Assets Brand Portal pode ajudá-lo a adquirir, controlar e distribuir com facilidade e segurança os ativos criativos aprovados para terceiros e usuários empresariais internos em todos os dispositivos.
content-type: reference
products: SG_EXPERIENCEMANAGER/Brand_Portal
topic-tags: introduction
exl-id: 0f2c45e4-416e-451a-905b-06c5e42a9272
source-git-commit: 32a67abf466dd3bf635b851b02377ed23591915e
workflow-type: tm+mt
source-wordcount: '1622'
ht-degree: 4%

---

# Visão geral do Experience Manager Assets Brand Portal {#overview-of-aem-assets-brand-portal}

Como profissional de marketing, às vezes é necessário colaborar com parceiros de canal e usuários de negócios internos para criar, gerenciar e fornecer rapidamente conteúdo digital relevante aos clientes. A entrega oportuna de conteúdo relevante em toda a jornada do cliente é essencial para impulsionar maior demanda, conversão, envolvimento e fidelidade do cliente.

Entretanto, o desenvolvimento de soluções que suportem o compartilhamento eficiente e seguro de itens como logotipos de marcas aprovadas, ativos de campanha ou imagens de produtos com equipes, parceiros e revendedores é um desafio. Garantir a eficiência e a segurança nesse processo requer planejamento e execução cuidadosos.

O **Adobe Experience Manager (AEM) Assets Brand Portal** concentra-se na necessidade do profissional de marketing de colaborar efetivamente com os usuários globais do Brand Portal, fornecendo distribuição de ativos e recursos de contribuição de ativos.

A distribuição de ativos permite adquirir, controlar e distribuir com segurança os ativos criativos aprovados para terceiros e usuários comerciais internos em todos os dispositivos. No entanto, a contribuição do ativo permite que os usuários do Brand Portal façam upload de ativos no Brand Portal e os publiquem no Experience Manager Assets, sem precisar acessar o ambiente do autor. O recurso de contribuição é chamado de **Origem do Assets no Brand Portal**. Juntos, ele melhora a experiência geral da Brand Portal em distribuição de ativos e a contribuição dos usuários da Brand Portal (agências/equipes externas), acelera o tempo de entrada no mercado dos ativos e reduz o risco de não conformidade e acesso não autorizado.
Consulte [Origem de ativos no Brand Portal](brand-portal-asset-sourcing.md).

O ambiente de portal baseado em navegador permite fazer upload, navegar, pesquisar, visualizar e exportar ativos facilmente em formatos aprovados.

## Configurar o Experience Manager Assets com o Brand Portal {#configure-brand-portal}

A configuração do Adobe Experience Manager Assets com Brand Portal habilita a publicação de ativos, a distribuição de ativos e os recursos de contribuição de ativos para os usuários do Brand Portal.

>[!NOTE]
>
>A configuração do Experience Manager Assets com Brand Portal é compatível com o Experience Manager Assets as a Cloud Service, Experience Manager Assets 6.3 e superior.

O Experience Manager Assets as a Cloud Service é configurado automaticamente com o Brand Portal ao ativar o Brand Portal na Cloud Manager. O fluxo de trabalho de ativação cria as configurações necessárias no backend e ativa o Brand Portal na mesma organização IMS da instância as a Cloud Service do Experience Manager Assets.

No entanto, o Experience Manager Assets (no local e managed service) é configurado manualmente com o Brand Portal usando o Adobe Developer Console, que obtém um token Adobe Identity Management Services (IMS) para autorização do locatário do Brand Portal.

Para obter mais informações, consulte [configurando o Experience Manager Assets com o Brand Portal](../using/configure-aem-assets-with-brand-portal.md).

## Personalidades do usuário no Brand Portal {#Personas}

O Brand Portal é compatível com as seguintes funções de usuário:

* Usuário convidado
* Visualizador
* Editor
* Administrador

A tabela a seguir lista as tarefas que os usuários nessas funções podem executar:

|  | **Navegar** | **Pesquisar** | **Download** | **Compartilhar pastas** | **Compartilhar uma coleção** | **Compartilhar ativos como um link** | **Acesso às Ferramentas Administrativas** |
|--- |--- |--- |--- |--- |--- |--- |--- |
| **Usuário convidado** | ✓ µ* | ✓ µ* | ✓ µ* | x | x | x | x |
| **Visualizador** | ✓ | ✓ | ✓ | x | x | x | x |
| **Editor** | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | x |
| **Administrador** | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ |

>[!NOTE]
>
>Os usuários convidados podem navegar, acessar e pesquisar ativos somente em pastas e coleções públicas.

<!--
&#42; Viewer users can access and download the public assets shared with them, and can add these assets to create their own collections.

>[!NOTE]
>
>There is a known issue that the share link for collections is currently visible to the viewer users. The viewer users does not have the privilege to add users to create a share link. This issue will be fixed in the upcoming release, the option to share link for the collections will not be available to the viewer users.
-->

### Usuário convidado {#guest-user}

O Experience Manager Assets Brand Portal permite [acesso de convidado](#request-access-to-brand-portal) ao Brand Portal. Um usuário convidado não precisa de credenciais para entrar no portal e tem acesso às pastas e coleções públicas. Como usuário convidado, você pode navegar pelos detalhes do ativo e ter uma exibição completa do ativo dos membros de pastas e coleções públicas. Pesquise, baixe e adicione ativos públicos à coleção [!UICONTROL Lightbox].

No entanto, a sessão de convidado o impede de criar coleções e pesquisas salvas, e as compartilha ainda mais. Os usuários em uma sessão de convidado não podem acessar configurações de pasta e coleções e não podem compartilhar ativos como link. Esta é uma lista de tarefas que um usuário convidado pode executar:

* [Procurar e acessar ativos públicos](browse-assets-brand-portal.md)

* [Pesquisar ativos públicos](brand-portal-searching.md)

* [Baixar ativos públicos](brand-portal-download-assets.md)

* [Adicionar ativos à [!UICONTROL Lightbox]](brand-portal-light-box.md#add-assets-to-lightbox)

Para obter mais informações, vá para [Acesso de convidado ao Brand Portal](../using/guest-access.md).

### Visualizador {#viewer}

Usuário do Brand Portal definido no [!DNL Admin Console] que tem acesso ao Brand Portal com a função de Visualizador. Um usuário com essa função pode fazer logon no Brand Portal e acessar pastas, coleções e ativos permitidos. O usuário também pode navegar, visualizar, baixar e exportar ativos (representações originais ou específicas), definir configurações de conta e pesquisar ativos. Esta é uma lista de tarefas que um Visualizador pode executar:

* [Procurar ativos](browse-assets-brand-portal.md)

* [Pesquisar por ativos](brand-portal-searching.md)

* [Baixar ativos](brand-portal-download-assets.md)

### Editor {#editor}

Um usuário com a função de Editor pode executar todas as tarefas que um Visualizador pode executar. Além disso, o e o Editor podem exibir os arquivos e pastas compartilhados por um administrador. O usuário com a função de um Editor também pode compartilhar conteúdo (arquivos, pastas, coleções) com outros.

Além das tarefas que um Visualizador pode executar, um Editor pode executar as seguintes tarefas adicionais:

* [Compartilhar pastas](brand-portal-sharing-folders.md)

* [Compartilhar uma coleção](brand-portal-share-collection.md)

* [Compartilhar ativos como um link](brand-portal-link-share.md)

### Administrador {#administrator}

Um administrador inclui um usuário marcado como administrador do sistema ou administrador de produto do Brand Portal no [!UICONTROL Admin Console]. Um administrador pode adicionar e remover administradores e usuários do sistema, definir predefinições, enviar e-mails aos usuários e exibir relatórios de uso do portal e de armazenamento.

>[!NOTE]
>
>No Brand Portal, um usuário marcado com a função de administrador de suporte no [!UICONTROL Admin Console] tem os mesmos privilégios de um administrador do sistema.

Um administrador pode executar todas as tarefas que um Editor pode executar. Estas são as tarefas adicionais que um administrador pode executar:

* [Gerenciar usuários, grupos e funções de usuário](brand-portal-adding-users.md)
* [Personalizar papel de parede, cabeçalhos de página e emails](brand-portal-branding.md)
* [Usar aspectos de pesquisa personalizados](brand-portal-search-facets.md)
* [Usar esquema de metadados](brand-portal-metadata-schemas.md)
* [Aplicar predefinições de imagens ou representações dinâmicas](brand-portal-image-presets.md)
* [Trabalhar com relatórios](brand-portal-reports.md)

Além das tarefas acima, um Autor no AEM Assets pode executar as seguintes tarefas:

* [Configurar o AEM Assets com o Brand Portal](../using/configure-aem-assets-with-brand-portal.md)
* [Publicar pastas no Brand Portal](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/assets/brandportal/brand-portal-publish-folder)
* [Publicar coleções no Brand Portal](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/assets/brandportal/brand-portal-publish-collection)

## Alias alternativo para o URL do Brand Portal {#tenant-alias-for-portal-url}

A partir do Brand Portal 6.4.3, as organizações podem ter um URL alternativo (alias) para cada URL existente de seu locatário do Brand Portal. O URL alias pode ser criado tendo um prefixo alternativo no URL.\
Se o nome do locatário tiver mais de 32 caracteres, um alias de locatário precisará ser criado.
Observe que somente o prefixo do URL do Brand Portal pode ser personalizado, e não o URL inteiro. Por exemplo, uma organização com o domínio existente `geomettrix.brand-portal.adobe.com` pode obter a criação de `geomettrixinc.brand-portal.adobe.com` mediante solicitação.

No entanto, a instância do Autor AEM pode ser [configurada](../using/configure-aem-assets-with-brand-portal.md) somente com a URL da ID do locatário e não com a URL do alias do locatário (alternativo).

>[!NOTE]
>
>Para obter um alias para o nome do locatário em um URL de portal existente, as organizações precisam entrar em contato com o Suporte ao cliente com uma nova solicitação de criação de alias de locatário. Primeiro, verifique se o alias está disponível, depois crie o alias para processar essa solicitação.
>
>Para substituir o alias antigo ou excluir o alias antigo, o mesmo processo precisa ser seguido.

## Solicitar acesso ao Brand Portal {#request-access-to-brand-portal}

Os usuários podem solicitar acesso ao Brand Portal na tela de logon. Essas solicitações são enviadas aos administradores do Brand Portal, que concedem acesso aos usuários por meio do Adobe [!UICONTROL Admin Console]. Depois que o acesso for concedido, os usuários receberão um email de notificação.

Para solicitar acesso, faça o seguinte:

1. Na página de login do Brand Portal, selecione **[!UICONTROL Clique aqui]** correspondente a **[!UICONTROL Precisa de Acesso?]**. No entanto, para entrar na sessão de convidado, selecione a **[!UICONTROL Clique aqui]** correspondente a **[!UICONTROL Acesso de convidado?]**.

   ![tela de logon do Brand Portal](assets/bp-login-requestaccess.png)

   A página [!UICONTROL Solicitar Acesso] é aberta.

1. Para solicitar acesso à Brand Portal de uma organização, você deve ter um [!UICONTROL Adobe ID], [!UICONTROL Enterprise ID] ou [!UICONTROL Federated ID] válido.

   Na página [!UICONTROL Solicitar Acesso], entre usando sua ID (cenário 1) ou crie uma [!UICONTROL Adobe ID] (cenário 2):

   ![[!UICONTROL Solicitar acesso]](assets/bplogin_request_access_2.png)

   **Cenário 1**

   1. Se você tiver um [!UICONTROL Adobe ID], [!UICONTROL Enterprise ID] ou [!UICONTROL Federated ID], clique em **[!UICONTROL Entrar]**.
A página [!UICONTROL Entrar] é aberta.

   1. Forneça suas credenciais do [!UICONTROL Adobe ID] e clique em **[!UICONTROL Entrar]**.

      ![entrar no Adobe](assets/bplogin_request_access_3.png)

   Você será redirecionado para a página [!UICONTROL Solicitar Acesso].

   **Cenário 2**

   1. Para criar uma [!UICONTROL Adobe ID], clique em **[!UICONTROL Obter uma Adobe ID]** na página [!UICONTROL Solicitar Acesso].
A página [!UICONTROL Entrar] é aberta.
   1. Clique em **[!UICONTROL Obter uma Adobe ID]**.
A página [!UICONTROL Inscrever-se] é aberta.
   1. Insira seu nome e sobrenome, ID de email e senha.
   1. Selecione **[!UICONTROL Inscrever-se]**.

      ![](assets/bplogin_request_access_5.png)

   Você será redirecionado para a página [!UICONTROL Solicitar Acesso].

1. A próxima página exibe seu nome e a ID de e-mail usada para solicitar acesso. Deixe um comentário para o administrador e clique em **[!UICONTROL Enviar]**.

   ![](assets/bplogin-request-access.png)

## Administradores de produto concedem acesso {#grant-access-to-brand-portal}

Os administradores de produtos do Brand Portal recebem solicitações de acesso na área de notificação do Brand Portal e por meio de emails na caixa de entrada.

![Notificação de solicitação de acesso](assets/bplogin_request_access_7.png)

Para conceder acesso, os administradores de produtos precisam clicar na notificação relevante na área de notificação do Brand Portal e, em seguida, clicar em **[!UICONTROL Conceder acesso]**.
Como alternativa, os administradores de produtos podem seguir o link fornecido no email de solicitação de acesso para visitar o Adobe [!UICONTROL Admin Console] e adicionar o usuário à configuração de produto relevante.

Você será redirecionado para a página inicial [Adobe [!UICONTROL Admin Console]](https://adminconsole.adobe.com/enterprise/overview). Use o Adobe [!UICONTROL Admin Console] para criar usuários e atribuí-los a perfis de produtos (conhecidos anteriormente como configurações de produtos), que são exibidos como grupos no Brand Portal. Para obter mais informações sobre como adicionar usuários no [!UICONTROL Admin Console], consulte [Adicionar um usuário](brand-portal-adding-users.md#add-a-user) (siga as Etapas 4 a 7 no procedimento para adicionar um usuário).

## Idiomas do Brand Portal {#brand-portal-language}

Você pode alterar o idioma do Brand Portal de Adobe [!UICONTROL Configurações de Experience Cloud].

![Notificação de solicitação de acesso](assets/BPLang.png)

Para alterar o idioma:

1. Selecione [!UICONTROL Usuário] > [!UICONTROL Editar perfil] no menu superior.

   ![Editar Perfil](assets/EditBPProfile.png)

1. Na página [!UICONTROL Configurações de Experience Cloud], selecione um idioma no menu suspenso [!UICONTROL Idioma].

## Notificação de manutenção do Brand Portal {#brand-portal-maintenance-notification}

Antes de o Brand Portal ser agendado para manutenção, uma notificação é exibida como um banner após você fazer logon no Brand Portal. Um exemplo de notificação:

![](assets/bp_maintenance_notification.png)

Você pode ignorar esta notificação e continuar usando o Brand Portal. Essa notificação aparece em cada nova sessão.

## Informações sobre versão e sistema {#release-and-system-information}

* [Novidades](whats-new.md)
* [Notas de versão](brand-portal-release-notes.md)
* [Formatos de arquivo não compatíveis](brand-portal-supported-formats.md)

## Recursos relacionados {#related-resources}

<!--
* [Adobe Customer Support]()
-->

* [Fóruns do AEM](https://experienceleaguecommunities.adobe.com/t5/adobe-experience-manager/ct-p/adobe-experience-manager-community?profile.language=pt)
