---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 5C1C51FE-747F-4176-84ED-A28AA3475581
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/remove-azoperationalinsightsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsDataSource.md
ms.openlocfilehash: 1a99f06fac37c0d96a159b0c17afc606d850ee65
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890217"
---
# <span data-ttu-id="b8748-101">Remove-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="b8748-101">Remove-AzOperationalInsightsDataSource</span></span>

## <span data-ttu-id="b8748-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b8748-102">SYNOPSIS</span></span>
<span data-ttu-id="b8748-103">Exclui uma fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="b8748-103">Deletes a data source.</span></span>

## <span data-ttu-id="b8748-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="b8748-104">SYNTAX</span></span>

### <span data-ttu-id="b8748-105">ByWorkspaceName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="b8748-105">ByWorkspaceName (Default)</span></span>
```
Remove-AzOperationalInsightsDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String> [-Name] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8748-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="b8748-106">ByWorkspaceObject</span></span>
```
Remove-AzOperationalInsightsDataSource [-Workspace] <PSWorkspace> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b8748-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="b8748-107">DESCRIPTION</span></span>
<span data-ttu-id="b8748-108">O cmdlet **Remove-AzOperationalInsightsDataSource** exclui uma fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="b8748-108">The **Remove-AzOperationalInsightsDataSource** cmdlet deletes a data source.</span></span>

## <span data-ttu-id="b8748-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b8748-109">EXAMPLES</span></span>

## <span data-ttu-id="b8748-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="b8748-110">PARAMETERS</span></span>

### <span data-ttu-id="b8748-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8748-111">-DefaultProfile</span></span>
<span data-ttu-id="b8748-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="b8748-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8748-113">-Force</span><span class="sxs-lookup"><span data-stu-id="b8748-113">-Force</span></span>
<span data-ttu-id="b8748-114">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="b8748-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b8748-115">-Name</span><span class="sxs-lookup"><span data-stu-id="b8748-115">-Name</span></span>
<span data-ttu-id="b8748-116">Especifica o nome de uma fonte de dados a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="b8748-116">Specifies the name of a data source to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8748-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8748-117">-ResourceGroupName</span></span>
<span data-ttu-id="b8748-118">Especifica o nome de um grupo de recursos que contém computadores.</span><span class="sxs-lookup"><span data-stu-id="b8748-118">Specifies the name of a resource group that contains computers.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8748-119">-Workspace</span><span class="sxs-lookup"><span data-stu-id="b8748-119">-Workspace</span></span>
<span data-ttu-id="b8748-120">Especifica um espaço de trabalho no qual este cmdlet opera.</span><span class="sxs-lookup"><span data-stu-id="b8748-120">Specifies a workspace in which this cmdlet operates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b8748-121">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="b8748-121">-WorkspaceName</span></span>
<span data-ttu-id="b8748-122">Especifica o nome de um espaço de trabalho no qual este cmdlet opera.</span><span class="sxs-lookup"><span data-stu-id="b8748-122">Specifies the name of a workspace in which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8748-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b8748-123">-Confirm</span></span>
<span data-ttu-id="b8748-124">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b8748-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8748-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8748-125">-WhatIf</span></span>
<span data-ttu-id="b8748-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b8748-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b8748-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b8748-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8748-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8748-128">CommonParameters</span></span>
<span data-ttu-id="b8748-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8748-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8748-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8748-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8748-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b8748-131">INPUTS</span></span>

### <span data-ttu-id="b8748-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="b8748-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="b8748-133">System.String</span><span class="sxs-lookup"><span data-stu-id="b8748-133">System.String</span></span>

## <span data-ttu-id="b8748-134">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="b8748-134">OUTPUTS</span></span>

### <span data-ttu-id="b8748-135">System.Void</span><span class="sxs-lookup"><span data-stu-id="b8748-135">System.Void</span></span>

## <span data-ttu-id="b8748-136">NOTES</span><span class="sxs-lookup"><span data-stu-id="b8748-136">NOTES</span></span>
* <span data-ttu-id="b8748-137">Palavras-chave: azure, azurerm, arm, resource, management, manager, operational, insights</span><span class="sxs-lookup"><span data-stu-id="b8748-137">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="b8748-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b8748-138">RELATED LINKS</span></span>

[<span data-ttu-id="b8748-139">Get-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="b8748-139">Get-AzOperationalInsightsDataSource</span></span>](./Get-AzOperationalInsightsDataSource.md)

[<span data-ttu-id="b8748-140">Set-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="b8748-140">Set-AzOperationalInsightsDataSource</span></span>](./Set-AzOperationalInsightsDataSource.md)


