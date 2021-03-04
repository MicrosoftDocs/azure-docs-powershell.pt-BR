---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 47AFBAC7-8818-4788-B685-7AB4DCD6C2DE
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/disable-azoperationalinsightslinuxperformancecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Disable-AzOperationalInsightsLinuxPerformanceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Disable-AzOperationalInsightsLinuxPerformanceCollection.md
ms.openlocfilehash: f5a7a5930adde047fe4b0d2766711050bff9e91d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891324"
---
# <span data-ttu-id="d5a5d-101">Disable-AzOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="d5a5d-101">Disable-AzOperationalInsightsLinuxPerformanceCollection</span></span>

## <span data-ttu-id="d5a5d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d5a5d-102">SYNOPSIS</span></span>
<span data-ttu-id="d5a5d-103">Interrompe a coleção de contadores de desempenho de computadores Linux.</span><span class="sxs-lookup"><span data-stu-id="d5a5d-103">Stops collection of performance counters from Linux computers.</span></span>

## <span data-ttu-id="d5a5d-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="d5a5d-104">SYNTAX</span></span>

### <span data-ttu-id="d5a5d-105">ByWorkspaceName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="d5a5d-105">ByWorkspaceName (Default)</span></span>
```
Disable-AzOperationalInsightsLinuxPerformanceCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d5a5d-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="d5a5d-106">ByWorkspaceObject</span></span>
```
Disable-AzOperationalInsightsLinuxPerformanceCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d5a5d-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="d5a5d-107">DESCRIPTION</span></span>
<span data-ttu-id="d5a5d-108">O cmdlet **Disable-AzOperationalInsightsLinuxPerformanceCollection** interrompe a coleção de contadores de desempenho de computadores Linux conectados em um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="d5a5d-108">The **Disable-AzOperationalInsightsLinuxPerformanceCollection** cmdlet stops collection of performance counters from connected Linux computers in a workspace.</span></span>

## <span data-ttu-id="d5a5d-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d5a5d-109">EXAMPLES</span></span>

## <span data-ttu-id="d5a5d-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="d5a5d-110">PARAMETERS</span></span>

### <span data-ttu-id="d5a5d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5a5d-111">-DefaultProfile</span></span>
<span data-ttu-id="d5a5d-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="d5a5d-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d5a5d-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5a5d-113">-ResourceGroupName</span></span>
<span data-ttu-id="d5a5d-114">Especifica o nome de um grupo de recursos que contém computadores Linux.</span><span class="sxs-lookup"><span data-stu-id="d5a5d-114">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="d5a5d-115">-Workspace</span><span class="sxs-lookup"><span data-stu-id="d5a5d-115">-Workspace</span></span>
<span data-ttu-id="d5a5d-116">Especifica um espaço de trabalho no qual este cmdlet opera.</span><span class="sxs-lookup"><span data-stu-id="d5a5d-116">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="d5a5d-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="d5a5d-117">-WorkspaceName</span></span>
<span data-ttu-id="d5a5d-118">Especifica o nome de um espaço de trabalho no qual este cmdlet opera.</span><span class="sxs-lookup"><span data-stu-id="d5a5d-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="d5a5d-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d5a5d-119">-Confirm</span></span>
<span data-ttu-id="d5a5d-120">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d5a5d-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d5a5d-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d5a5d-121">-WhatIf</span></span>
<span data-ttu-id="d5a5d-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d5a5d-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d5a5d-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d5a5d-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d5a5d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5a5d-124">CommonParameters</span></span>
<span data-ttu-id="d5a5d-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5a5d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5a5d-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5a5d-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5a5d-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d5a5d-127">INPUTS</span></span>

### <span data-ttu-id="d5a5d-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="d5a5d-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="d5a5d-129">System.String</span><span class="sxs-lookup"><span data-stu-id="d5a5d-129">System.String</span></span>

## <span data-ttu-id="d5a5d-130">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="d5a5d-130">OUTPUTS</span></span>

### <span data-ttu-id="d5a5d-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="d5a5d-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="d5a5d-132">NOTES</span><span class="sxs-lookup"><span data-stu-id="d5a5d-132">NOTES</span></span>
* <span data-ttu-id="d5a5d-133">Palavras-chave: azure, azurerm, arm, resource, management, manager, operational, insights</span><span class="sxs-lookup"><span data-stu-id="d5a5d-133">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="d5a5d-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d5a5d-134">RELATED LINKS</span></span>

[<span data-ttu-id="d5a5d-135">Enable-AzOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="d5a5d-135">Enable-AzOperationalInsightsLinuxPerformanceCollection</span></span>](./Enable-AzOperationalInsightsLinuxPerformanceCollection.md)

[<span data-ttu-id="d5a5d-136">New-AzOperationalInsightsLinuxSyslogDataSource</span><span class="sxs-lookup"><span data-stu-id="d5a5d-136">New-AzOperationalInsightsLinuxSyslogDataSource</span></span>](./New-AzOperationalInsightsLinuxSyslogDataSource.md)


