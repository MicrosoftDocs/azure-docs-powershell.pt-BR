---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 10141D75-B58D-42B0-B0A6-92FF630E534C
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/enable-azoperationalinsightslinuxperformancecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Enable-AzOperationalInsightsLinuxPerformanceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Enable-AzOperationalInsightsLinuxPerformanceCollection.md
ms.openlocfilehash: 85ff01bdbdf454f498366b33d4684532f8382c7d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891315"
---
# <span data-ttu-id="523a1-101">Enable-AzOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="523a1-101">Enable-AzOperationalInsightsLinuxPerformanceCollection</span></span>

## <span data-ttu-id="523a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="523a1-102">SYNOPSIS</span></span>
<span data-ttu-id="523a1-103">Inicia a coleção de contadores de desempenho de computadores Linux.</span><span class="sxs-lookup"><span data-stu-id="523a1-103">Starts collection of performance counters from Linux computers.</span></span>

## <span data-ttu-id="523a1-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="523a1-104">SYNTAX</span></span>

### <span data-ttu-id="523a1-105">ByWorkspaceName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="523a1-105">ByWorkspaceName (Default)</span></span>
```
Enable-AzOperationalInsightsLinuxPerformanceCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="523a1-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="523a1-106">ByWorkspaceObject</span></span>
```
Enable-AzOperationalInsightsLinuxPerformanceCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="523a1-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="523a1-107">DESCRIPTION</span></span>
<span data-ttu-id="523a1-108">O cmdlet **Enable-AzOperationalInsightsLinuxPerformanceCollection** inicia a coleção de contadores de desempenho de computadores Linux conectados em um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="523a1-108">The **Enable-AzOperationalInsightsLinuxPerformanceCollection** cmdlet starts collection of performance counters from connected Linux computers in a workspace.</span></span>

## <span data-ttu-id="523a1-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="523a1-109">EXAMPLES</span></span>

## <span data-ttu-id="523a1-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="523a1-110">PARAMETERS</span></span>

### <span data-ttu-id="523a1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="523a1-111">-DefaultProfile</span></span>
<span data-ttu-id="523a1-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="523a1-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="523a1-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="523a1-113">-ResourceGroupName</span></span>
<span data-ttu-id="523a1-114">Especifica o nome de um grupo de recursos que contém computadores Linux.</span><span class="sxs-lookup"><span data-stu-id="523a1-114">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="523a1-115">-Workspace</span><span class="sxs-lookup"><span data-stu-id="523a1-115">-Workspace</span></span>
<span data-ttu-id="523a1-116">Especifica um espaço de trabalho no qual este cmdlet opera.</span><span class="sxs-lookup"><span data-stu-id="523a1-116">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="523a1-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="523a1-117">-WorkspaceName</span></span>
<span data-ttu-id="523a1-118">Especifica o nome de um espaço de trabalho no qual este cmdlet opera.</span><span class="sxs-lookup"><span data-stu-id="523a1-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="523a1-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="523a1-119">-Confirm</span></span>
<span data-ttu-id="523a1-120">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="523a1-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="523a1-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="523a1-121">-WhatIf</span></span>
<span data-ttu-id="523a1-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="523a1-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="523a1-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="523a1-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="523a1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="523a1-124">CommonParameters</span></span>
<span data-ttu-id="523a1-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="523a1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="523a1-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="523a1-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="523a1-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="523a1-127">INPUTS</span></span>

### <span data-ttu-id="523a1-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="523a1-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="523a1-129">System.String</span><span class="sxs-lookup"><span data-stu-id="523a1-129">System.String</span></span>

## <span data-ttu-id="523a1-130">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="523a1-130">OUTPUTS</span></span>

### <span data-ttu-id="523a1-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="523a1-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="523a1-132">NOTES</span><span class="sxs-lookup"><span data-stu-id="523a1-132">NOTES</span></span>
* <span data-ttu-id="523a1-133">Palavras-chave: azure, azurerm, arm, resource, management, manager, operational, insights</span><span class="sxs-lookup"><span data-stu-id="523a1-133">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="523a1-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="523a1-134">RELATED LINKS</span></span>

[<span data-ttu-id="523a1-135">Disable-AzOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="523a1-135">Disable-AzOperationalInsightsLinuxPerformanceCollection</span></span>](./Disable-AzOperationalInsightsLinuxPerformanceCollection.md)


