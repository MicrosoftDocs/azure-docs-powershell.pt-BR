---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 47AFBAC7-8818-4788-B685-7AB4DCD6C2DE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/disable-azurermoperationalinsightslinuxperformancecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Disable-AzureRmOperationalInsightsLinuxPerformanceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Disable-AzureRmOperationalInsightsLinuxPerformanceCollection.md
ms.openlocfilehash: e6a77e8e89f710e1f8f827a27b1e1709ca8e3f1a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428046"
---
# <span data-ttu-id="e8ddc-101">Disable-AzureRmOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="e8ddc-101">Disable-AzureRmOperationalInsightsLinuxPerformanceCollection</span></span>

## <span data-ttu-id="e8ddc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e8ddc-102">SYNOPSIS</span></span>
<span data-ttu-id="e8ddc-103">Interrompe a coleta de contadores de desempenho de computadores Linux.</span><span class="sxs-lookup"><span data-stu-id="e8ddc-103">Stops collection of performance counters from Linux computers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e8ddc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e8ddc-104">SYNTAX</span></span>

### <span data-ttu-id="e8ddc-105">ByWorkspaceName (padrão)</span><span class="sxs-lookup"><span data-stu-id="e8ddc-105">ByWorkspaceName (Default)</span></span>
```
Disable-AzureRmOperationalInsightsLinuxPerformanceCollection [-ResourceGroupName] <String>
 [-WorkspaceName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8ddc-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="e8ddc-106">ByWorkspaceObject</span></span>
```
Disable-AzureRmOperationalInsightsLinuxPerformanceCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e8ddc-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e8ddc-107">DESCRIPTION</span></span>
<span data-ttu-id="e8ddc-108">O cmdlet **Disable-AzureRmOperationalInsightsLinuxPerformanceCollection** interrompe a coleta de contadores de desempenho de computadores Linux conectados em um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="e8ddc-108">The **Disable-AzureRmOperationalInsightsLinuxPerformanceCollection** cmdlet stops collection of performance counters from connected Linux computers in a workspace.</span></span>

## <span data-ttu-id="e8ddc-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e8ddc-109">EXAMPLES</span></span>

## <span data-ttu-id="e8ddc-110">OS</span><span class="sxs-lookup"><span data-stu-id="e8ddc-110">PARAMETERS</span></span>

### <span data-ttu-id="e8ddc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8ddc-111">-DefaultProfile</span></span>
<span data-ttu-id="e8ddc-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="e8ddc-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e8ddc-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8ddc-113">-ResourceGroupName</span></span>
<span data-ttu-id="e8ddc-114">Especifica o nome de um grupo de recursos que contém computadores Linux.</span><span class="sxs-lookup"><span data-stu-id="e8ddc-114">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="e8ddc-115">-Espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="e8ddc-115">-Workspace</span></span>
<span data-ttu-id="e8ddc-116">Especifica um espaço de trabalho no qual esse cmdlet Opera.</span><span class="sxs-lookup"><span data-stu-id="e8ddc-116">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="e8ddc-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e8ddc-117">-WorkspaceName</span></span>
<span data-ttu-id="e8ddc-118">Especifica o nome de um espaço de trabalho no qual esse cmdlet Opera.</span><span class="sxs-lookup"><span data-stu-id="e8ddc-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="e8ddc-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e8ddc-119">-Confirm</span></span>
<span data-ttu-id="e8ddc-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e8ddc-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8ddc-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8ddc-121">-WhatIf</span></span>
<span data-ttu-id="e8ddc-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e8ddc-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e8ddc-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e8ddc-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8ddc-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8ddc-124">CommonParameters</span></span>
<span data-ttu-id="e8ddc-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8ddc-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8ddc-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8ddc-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8ddc-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e8ddc-127">INPUTS</span></span>

### <span data-ttu-id="e8ddc-128">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="e8ddc-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>
<span data-ttu-id="e8ddc-129">Parâmetros: espaço de trabalho (ByValue)</span><span class="sxs-lookup"><span data-stu-id="e8ddc-129">Parameters: Workspace (ByValue)</span></span>

### <span data-ttu-id="e8ddc-130">System. String</span><span class="sxs-lookup"><span data-stu-id="e8ddc-130">System.String</span></span>

## <span data-ttu-id="e8ddc-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e8ddc-131">OUTPUTS</span></span>

### <span data-ttu-id="e8ddc-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="e8ddc-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="e8ddc-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e8ddc-133">NOTES</span></span>
* <span data-ttu-id="e8ddc-134">Palavras-chave: Azure, azurerm, ARM, Resource, Management, Manager, Operational, insights</span><span class="sxs-lookup"><span data-stu-id="e8ddc-134">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="e8ddc-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e8ddc-135">RELATED LINKS</span></span>

[<span data-ttu-id="e8ddc-136">Enable-AzureRmOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="e8ddc-136">Enable-AzureRmOperationalInsightsLinuxPerformanceCollection</span></span>](./Enable-AzureRmOperationalInsightsLinuxPerformanceCollection.md)

[<span data-ttu-id="e8ddc-137">New-AzureRmOperationalInsightsLinuxSyslogDataSource</span><span class="sxs-lookup"><span data-stu-id="e8ddc-137">New-AzureRmOperationalInsightsLinuxSyslogDataSource</span></span>](./New-AzureRmOperationalInsightsLinuxSyslogDataSource.md)


