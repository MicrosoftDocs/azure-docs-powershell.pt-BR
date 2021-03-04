---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: F94415DA-1A4A-4D37-A626-1EDF5D1EFE74
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/get-azoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspace.md
ms.openlocfilehash: 4082e7fc36228953ea33f8f3252bab642ca50e2c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891778"
---
# <span data-ttu-id="a6a94-101">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="a6a94-101">Get-AzOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="a6a94-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a6a94-102">SYNOPSIS</span></span>
<span data-ttu-id="a6a94-103">Obtém informações sobre um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="a6a94-103">Gets information about a workspace.</span></span>

## <span data-ttu-id="a6a94-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="a6a94-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsWorkspace [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a6a94-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="a6a94-105">DESCRIPTION</span></span>
<span data-ttu-id="a6a94-106">O cmdlet **Get-AzOperationalInsightsWorkspace** obtém informações sobre um espaço de trabalho existente.</span><span class="sxs-lookup"><span data-stu-id="a6a94-106">The **Get-AzOperationalInsightsWorkspace** cmdlet gets information about an existing workspace.</span></span>
<span data-ttu-id="a6a94-107">Se você especificar um nome de espaço de trabalho, esse cmdlet obterá informações sobre esse espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="a6a94-107">If you specify a workspace name, this cmdlet gets information about that workspace.</span></span>
<span data-ttu-id="a6a94-108">Se você não especificar um nome, esse cmdlet obterá informações sobre todos os espaços de trabalho em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a6a94-108">If you do not specify a name, this cmdlet gets information about all workspaces in a resource group.</span></span>
<span data-ttu-id="a6a94-109">Se você não especificar um nome e um grupo de recursos, este cmdlet obtém informações sobre todos os espaços de trabalho em uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="a6a94-109">If you do not specify a name and resource group, this cmdlet gets information about all workspaces in a subscription.</span></span>

## <span data-ttu-id="a6a94-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a6a94-110">EXAMPLES</span></span>

### <span data-ttu-id="a6a94-111">Exemplo 1: Obter um espaço de trabalho pelo nome</span><span class="sxs-lookup"><span data-stu-id="a6a94-111">Example 1: Get a workspace by name</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspace -Name "MyWorkspace" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="a6a94-112">Este comando obtém um espaço de trabalho chamado MyWorkspace no grupo de recursos chamado ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="a6a94-112">This command gets a workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

## <span data-ttu-id="a6a94-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="a6a94-113">PARAMETERS</span></span>

### <span data-ttu-id="a6a94-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6a94-114">-DefaultProfile</span></span>
<span data-ttu-id="a6a94-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="a6a94-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a6a94-116">-Name</span><span class="sxs-lookup"><span data-stu-id="a6a94-116">-Name</span></span>
<span data-ttu-id="a6a94-117">Especifica o nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="a6a94-117">Specifies the workspace name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6a94-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6a94-118">-ResourceGroupName</span></span>
<span data-ttu-id="a6a94-119">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="a6a94-119">Specifies the name of an Azure resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6a94-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6a94-120">CommonParameters</span></span>
<span data-ttu-id="a6a94-121">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6a94-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6a94-122">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6a94-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6a94-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a6a94-123">INPUTS</span></span>

### <span data-ttu-id="a6a94-124">System.String</span><span class="sxs-lookup"><span data-stu-id="a6a94-124">System.String</span></span>

## <span data-ttu-id="a6a94-125">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="a6a94-125">OUTPUTS</span></span>

### <span data-ttu-id="a6a94-126">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="a6a94-126">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="a6a94-127">NOTES</span><span class="sxs-lookup"><span data-stu-id="a6a94-127">NOTES</span></span>

## <span data-ttu-id="a6a94-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a6a94-128">RELATED LINKS</span></span>

[<span data-ttu-id="a6a94-129">Cmdlets do Insights Operacionais do Azure</span><span class="sxs-lookup"><span data-stu-id="a6a94-129">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


