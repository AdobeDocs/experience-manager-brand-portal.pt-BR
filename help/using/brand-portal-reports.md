---
title: Trabalhar com relatórios
seo-title: Work with reports
description: Os administradores do Experience Manager Assets Brand Portal podem exibir relatórios sobre o uso do Brand Portal e criar, gerenciar e exibir relatórios sobre ativos baixados, expirados, publicados e compartilhados por meio do Brand Portal.
seo-description: Experience Manager Assets Brand Portal Administrators can view report about Brand Portal usage, and create, manage, and view reports around assets downloaded, expired, published, and link shared through Brand Portal.
uuid: dc4e5275-a614-4b95-8c70-2b7e470c50a7
content-type: reference
topic-tags: administration
products: SG_EXPERIENCEMANAGER/Brand_Portal
discoiquuid: 7683074f-b6ea-42e0-a411-3b13eb88d1f2
role: Admin
exl-id: 03d0292c-23c2-4ea0-9781-eb27768e6c33
source-git-commit: 955cd8afe939ff47e9f08f312505e230e2f38495
workflow-type: tm+mt
source-wordcount: '1000'
ht-degree: 1%

---

# Trabalhar com relatórios {#work-with-reports}

O recurso de geração de relatórios é fundamental para avaliar o uso do Brand Portal e saber como os usuários internos e externos interagem com os ativos aprovados. Os administradores podem exibir o relatório de Uso do Brand Portal, que está sempre disponível na página Relatórios de ativos. No entanto, os relatórios para logons de usuários e ativos baixados, expirados, publicados e compartilhados por meio de links podem ser gerados e exibidos na página Relatórios de ativos. Esses relatórios são úteis na análise da implantação de ativos, que permitem obter as principais métricas de sucesso para medir a adoção de ativos aprovados dentro e fora da organização.

A interface de gerenciamento de relatórios é intuitiva e inclui opções e controles refinados para acessar relatórios salvos. É possível visualizar, baixar ou excluir relatórios na página Relatórios de ativos, onde todos os relatórios gerados anteriormente são listados.

## Exibir relatórios {#view-reports}

Para exibir um relatório, siga estas etapas:

1. Na barra de ferramentas na parte superior, toque/clique no logotipo do Experience Manager para acessar as ferramentas administrativas.

   ![](assets/aemlogo.png)

1. No painel de ferramentas administrativas, clique em **[!UICONTROL Criar/Gerenciar Relatórios]** para abrir a página **[!UICONTROL Relatórios de Ativos]**.

   ![](assets/access-asset-reports.png)

1. Acesse o relatório **[!UICONTROL Uso]** e outros relatórios gerados a partir da página Relatórios de ativos.

   >[!NOTE]
   >
   >O relatório de uso é um relatório padrão gerado no Brand Portal. Ele não pode ser criado ou excluído. No entanto, você pode criar, baixar e excluir os relatórios Download, Expiração, Publish, Compartilhamento de links e Logons de usuário.

   Para exibir um relatório, clique no link do relatório. Como alternativa, selecione o relatório e toque/clique no ícone Exibir na barra de ferramentas.

   O **[!UICONTROL Relatório de uso]** exibe informações sobre o número de usuários ativos do Brand Portal, o espaço de armazenamento ocupado por todos os ativos e a contagem total de ativos no Brand Portal. Os usuários do portal de marcas que não estão atribuídos a nenhum perfil de produto no Admin Console são considerados usuários inativos e não são refletidos no **[!UICONTROL Relatório de uso]**.
O relatório também exibe a capacidade permitida para cada uma dessas métricas de informações.

   ![](assets/usage-report.png)

   O relatório **[!UICONTROL Logons de Usuário]** fornece informações sobre os usuários que fizeram logon no Brand Portal. O relatório mostra nomes de exibição, IDs de email, personas (administrador, visualizador, editor, convidado), grupos, último logon, status da atividade e contagem de logon de cada usuário da implantação do Brand Portal 6.4.2 até o momento da geração do relatório.

   ![](assets/user-logins.png)

   **[!UICONTROL Baixar]** listas de relatórios e detalhes sobre todos os ativos baixados em um intervalo de data e hora específico.

   ![](assets/download-report.png)

   >[!NOTE]
   >
   >O relatório **[!UICONTROL Download]** de ativos exibe somente os ativos que foram selecionados e baixados individualmente da Brand Portal. Se um usuário tiver baixado uma pasta contendo ativos, o relatório não exibirá a pasta ou os ativos dentro da pasta.

   O relatório **[!UICONTROL Expiração]** lista e detalha todos os ativos que expiraram em um período específico.

   ![](assets/expiration-report.png)

   O relatório do **[!UICONTROL Publish]** lista e fornece informações sobre todos os ativos publicados do Experience Manager Assets para o Brand Portal em um intervalo de tempo especificado.

   ![](assets/publish-report.png)

   >[!NOTE]
   >
   >O Relatório do Publish não exibe informações sobre fragmentos de conteúdo, pois eles não podem ser publicados na Brand Portal.

   O **[!UICONTROL Relatório de compartilhamento de links]** lista todos os ativos compartilhados por meio de links da interface do Brand Portal em um intervalo de tempo específico. O relatório também informa quando o ativo foi compartilhado por meio de um link, por qual usuário, quando o link expira e o número de links compartilhados para o locatário (e usuários com os quais o link do ativo foi compartilhado). As colunas do Relatório de compartilhamento de link não são personalizáveis.

   ![](assets/link-share-report.png)

   >[!NOTE]
   >
   >O Relatório de compartilhamento de links não exibe usuários que têm acesso ao ativo compartilhado por meio do link ou que baixaram o ativo por meio do link.
   >
   >Para rastrear downloads por meio do link compartilhado, você precisa gerar um relatório de download após selecionar a opção **[!UICONTROL Somente Downloads de Compartilhamento de Link]** na página **[!UICONTROL Criar Relatório]**. No entanto, o usuário (baixado por) é anônimo neste caso.

## Gerar relatórios {#generate-reports}

Os administradores podem gerar e gerenciar os seguintes relatórios padrão. Uma vez gerados, eles são salvos para serem [acessados](../using/brand-portal-reports.md#main-pars-header) mais tarde:

* Logons de usuário
* Download
* Expiração
* Publicação
* Compartilhamento de link

As colunas no relatório de Download, Expiração e Publish podem ser personalizadas para exibição. Para gerar um relatório, siga estas etapas:

1. Na barra de ferramentas na parte superior, toque/clique no logotipo do Experience Manager para acessar as ferramentas administrativas.

1. No painel de ferramentas administrativas, toque/clique em **[!UICONTROL Criar/Gerenciar relatórios]** para abrir a página **[!UICONTROL Relatórios de ativos]**.

   ![](assets/asset-reports.png)

1. Na página Relatórios de ativos, toque/clique em **[!UICONTROL Criar]**.
1. Na página **[!UICONTROL Criar relatório]**, selecione um relatório a ser criado e toque/clique em **[!UICONTROL Avançar]**.

   ![](assets/crete-report.png)

1. Configurar detalhes do relatório. Especifique o título, a descrição, a estrutura de pastas (onde o relatório precisa ser executado e gerar estatísticas) e o intervalo de datas dos relatórios **[!UICONTROL Download]**, **[!UICONTROL Expiração]** e **[!UICONTROL Publish]**.

   ![](assets/create-report-page.png)

   Por outro lado, o **[!UICONTROL Relatório de compartilhamento de links]** precisa apenas dos parâmetros de título, descrição e intervalo de datas.

   ![](assets/create-link-share-report.png)

   >[!NOTE]
   >
   >Os caracteres especiais # e % no título do relatório são substituídos por um hífen (-) na geração do relatório.

1. Toque/clique em **[!UICONTROL Avançar]** para configurar as colunas dos relatórios de Download, Expiração e Publish.
1. Marque ou desmarque as caixas de seleção apropriadas, conforme necessário. Por exemplo, para exibir nomes de usuários (que baixaram ativos) no relatório **[!UICONTROL Download]**, selecione **[!UICONTROL Baixado por]**. A imagem a seguir ilustra a seleção de colunas padrão no relatório de Download.

   ![](assets/createdownloadreport.png)

   Você também pode adicionar colunas personalizadas a esses relatórios para exibir mais dados para seus requisitos personalizados.

   Para adicionar colunas personalizadas ao Download, Publish ou relatório de Expiração, siga estas etapas:

   1. Para exibir uma coluna personalizada, toque/clique em **[!UICONTROL Adicionar]** em [!UICONTROL Colunas personalizadas].
   1. Especifique o nome da coluna no campo **[!UICONTROL Nome da Coluna]**.
   1. Selecione a propriedade para a qual a coluna precisa ser mapeada, usando o seletor de propriedades.

      ![](assets/property-picker.png)
Como alternativa, digite o caminho no campo caminho da propriedade.

      ![](assets/property-path.png)

      Para adicionar mais colunas personalizadas, toque/clique em **Adicionar** e repita as etapas 2 e 3.

1. Toque/clique em **[!UICONTROL Criar]**. Uma mensagem notifica que a geração de relatório foi iniciada.

## Baixar relatórios {#download-reports}

Para salvar e baixar um relatório como arquivo .csv, siga um destes procedimentos:

* Selecione um relatório na página Relatórios de ativos e toque/clique em **[!UICONTROL Baixar]** na barra de ferramentas na parte superior.

![](assets/download-asset-report.png)

* Na página Relatórios de ativos, abra um relatório. Selecione a opção **[!UICONTROL Baixar]** na parte superior da página do relatório.

![](assets/download-report-fromwithin.png)

## Excluir relatórios {#delete-reports}

Para excluir um relatório existente, selecione o relatório na página **[!UICONTROL Relatórios de ativos]** e toque/clique em **[!UICONTROL Excluir]** na barra de ferramentas na parte superior.

>[!NOTE]
>
>Não é possível excluir o relatório de **[!UICONTROL Uso]**.
