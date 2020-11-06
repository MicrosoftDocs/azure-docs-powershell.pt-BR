---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlsyncagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlSyncAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlSyncAgent.md
ms.openlocfilehash: 9886d2d32dd3bce8841dcf2652cf89054335b112
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440003"
---
# <span data-ttu-id="f1b74-101">Remove-AzureRmSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="f1b74-101">Remove-AzureRmSqlSyncAgent</span></span>

## <span data-ttu-id="f1b74-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f1b74-102">SYNOPSIS</span></span>
<span data-ttu-id="f1b74-103">Remove um agente de sincronização do SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="f1b74-103">Removes an Azure SQL Sync Agent.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f1b74-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f1b74-104">SYNTAX</span></span>

```
Remove-AzureRmSqlSyncAgent [-Name] <String> [-Force] [-PassThru] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f1b74-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f1b74-105">DESCRIPTION</span></span>
<span data-ttu-id="f1b74-106">O cmdlet **Remove-AzureRmSqlSyncAgent** remove um agente de sincronização do SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="f1b74-106">The **Remove-AzureRmSqlSyncAgent** cmdlet removes an Azure SQL Sync Agent.</span></span>

## <span data-ttu-id="f1b74-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f1b74-107">EXAMPLES</span></span>

### <span data-ttu-id="f1b74-108">Exemplo 1: remover um agente de sincronização</span><span class="sxs-lookup"><span data-stu-id="f1b74-108">Example 1: Remove a sync agent</span></span>
```
PS C:\>Remove-AzureRmSqlSyncAgent -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -Name "syncAgent01"
```

<span data-ttu-id="f1b74-109">Esse comando Remove o agente SQL Sync do Azure chamado syncAgent01.</span><span class="sxs-lookup"><span data-stu-id="f1b74-109">This command removes the Azure SQL Sync Agent named syncAgent01.</span></span>

## <span data-ttu-id="f1b74-110">OS</span><span class="sxs-lookup"><span data-stu-id="f1b74-110">PARAMETERS</span></span>

### <span data-ttu-id="f1b74-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1b74-111">-DefaultProfile</span></span>
<span data-ttu-id="f1b74-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="f1b74-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1b74-113">-Force</span><span class="sxs-lookup"><span data-stu-id="f1b74-113">-Force</span></span>
<span data-ttu-id="f1b74-114">Ignorar a mensagem de confirmação para executar a ação</span><span class="sxs-lookup"><span data-stu-id="f1b74-114">Skip confirmation message for performing the action</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1b74-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="f1b74-115">-Name</span></span>
<span data-ttu-id="f1b74-116">O nome do agente de sincronização.</span><span class="sxs-lookup"><span data-stu-id="f1b74-116">The sync agent name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncAgentName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1b74-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f1b74-117">-PassThru</span></span>
<span data-ttu-id="f1b74-118">Define se o retorne o agente de sincronização removido</span><span class="sxs-lookup"><span data-stu-id="f1b74-118">Defines Whether return the removed sync agent</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1b74-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1b74-119">-ResourceGroupName</span></span>
<span data-ttu-id="f1b74-120">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f1b74-120">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1b74-121">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="f1b74-121">-ServerName</span></span>
<span data-ttu-id="f1b74-122">O nome do Azure SQL Server no qual o agente de sincronização se encontra.</span><span class="sxs-lookup"><span data-stu-id="f1b74-122">The name of the Azure SQL Server the sync agent is in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1b74-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f1b74-123">-Confirm</span></span>
<span data-ttu-id="f1b74-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f1b74-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1b74-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1b74-125">-WhatIf</span></span>
<span data-ttu-id="f1b74-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f1b74-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1b74-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f1b74-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1b74-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1b74-128">CommonParameters</span></span>
<span data-ttu-id="f1b74-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1b74-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1b74-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1b74-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1b74-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f1b74-131">INPUTS</span></span>

### <span data-ttu-id="f1b74-132">System. String</span><span class="sxs-lookup"><span data-stu-id="f1b74-132">System.String</span></span>

## <span data-ttu-id="f1b74-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f1b74-133">OUTPUTS</span></span>

### <span data-ttu-id="f1b74-134">Microsoft. Azure. Commands. Sql. datasync. Model. AzureSqlSyncAgentModel</span><span class="sxs-lookup"><span data-stu-id="f1b74-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentModel</span></span>

## <span data-ttu-id="f1b74-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f1b74-135">NOTES</span></span>

## <span data-ttu-id="f1b74-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f1b74-136">RELATED LINKS</span></span>

[<span data-ttu-id="f1b74-137">New-AzureRmSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="f1b74-137">New-AzureRmSqlSyncAgent</span></span>](./New-AzureRmSqlSyncAgent.md)

[<span data-ttu-id="f1b74-138">Get-AzureRmSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="f1b74-138">Get-AzureRmSqlSyncAgent</span></span>](./Get-AzureRmSqlSyncAgent.md)
