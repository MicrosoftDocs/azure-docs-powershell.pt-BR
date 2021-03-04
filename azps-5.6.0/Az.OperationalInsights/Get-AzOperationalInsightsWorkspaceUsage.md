---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 818A048F-7CBE-4845-BBC2-6420CE48199A
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/get-azoperationalinsightsworkspaceusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceUsage.md
ms.openlocfilehash: b5b14cbf816a7872abf431f787f9e3102006901c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892062"
---
# <span data-ttu-id="d2ac4-101">Get-AzOperationalInsightsWorkspaceUsage</span><span class="sxs-lookup"><span data-stu-id="d2ac4-101">Get-AzOperationalInsightsWorkspaceUsage</span></span>

## <span data-ttu-id="d2ac4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d2ac4-102">SYNOPSIS</span></span>
<span data-ttu-id="d2ac4-103">Obtém os dados de uso de um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="d2ac4-103">Gets the usage data for a workspace.</span></span>

## <span data-ttu-id="d2ac4-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="d2ac4-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsWorkspaceUsage [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d2ac4-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="d2ac4-105">DESCRIPTION</span></span>
<span data-ttu-id="d2ac4-106">O cmdlet **Get-AzOperationalInsightsWorkspaceUsage** recupera os dados de uso de um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="d2ac4-106">The **Get-AzOperationalInsightsWorkspaceUsage** cmdlet retrieves the usage data for a workspace.</span></span>
<span data-ttu-id="d2ac4-107">Isso expõe a quantos dados foram analisados pelo espaço de trabalho durante um determinado período.</span><span class="sxs-lookup"><span data-stu-id="d2ac4-107">This exposes how much data has been analyzed by the workspace over a certain period.</span></span>

## <span data-ttu-id="d2ac4-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d2ac4-108">EXAMPLES</span></span>

### <span data-ttu-id="d2ac4-109">Exemplo 1: Obter dados de uso pelo nome do espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="d2ac4-109">Example 1: Get usage data by workspace name</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspaceUsage -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
```

<span data-ttu-id="d2ac4-110">Este comando obtém os detalhes de uso do espaço de trabalho chamado MyWorkspace no grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="d2ac4-110">This command gets the usage details for the workspace named MyWorkspace in the specified resource group.</span></span>

### <span data-ttu-id="d2ac4-111">Exemplo 2: Obter dados de uso usando o pipeline</span><span class="sxs-lookup"><span data-stu-id="d2ac4-111">Example 2: Get usage data using the pipeline</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Get-AzOperationalInsightsWorkspaceUsage
```

<span data-ttu-id="d2ac4-112">Esse comando obtém o espaço de trabalho chamado MyWorkSpace usando o cmdlet Get-AzOperationalInsightsWorkspace e passa o espaço de trabalho para o cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="d2ac4-112">This command gets the workspace named MyWorkSpace using the Get-AzOperationalInsightsWorkspace cmdlet, and then passes the workspace to the current cmdlet.</span></span>
<span data-ttu-id="d2ac4-113">O comando obtém os detalhes de uso desse espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="d2ac4-113">The command gets the usage details for that workspace.</span></span>

## <span data-ttu-id="d2ac4-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="d2ac4-114">PARAMETERS</span></span>

### <span data-ttu-id="d2ac4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2ac4-115">-DefaultProfile</span></span>
<span data-ttu-id="d2ac4-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="d2ac4-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d2ac4-117">-Name</span><span class="sxs-lookup"><span data-stu-id="d2ac4-117">-Name</span></span>
<span data-ttu-id="d2ac4-118">Especifica o nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="d2ac4-118">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="d2ac4-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2ac4-119">-ResourceGroupName</span></span>
<span data-ttu-id="d2ac4-120">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="d2ac4-120">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="d2ac4-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2ac4-121">CommonParameters</span></span>
<span data-ttu-id="d2ac4-122">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2ac4-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2ac4-123">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2ac4-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2ac4-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d2ac4-124">INPUTS</span></span>

### <span data-ttu-id="d2ac4-125">System.String</span><span class="sxs-lookup"><span data-stu-id="d2ac4-125">System.String</span></span>

## <span data-ttu-id="d2ac4-126">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="d2ac4-126">OUTPUTS</span></span>

### <span data-ttu-id="d2ac4-127">Microsoft.Azure.Commands.OperationalInsights.Models.PSUsageMetric</span><span class="sxs-lookup"><span data-stu-id="d2ac4-127">Microsoft.Azure.Commands.OperationalInsights.Models.PSUsageMetric</span></span>

## <span data-ttu-id="d2ac4-128">NOTES</span><span class="sxs-lookup"><span data-stu-id="d2ac4-128">NOTES</span></span>

## <span data-ttu-id="d2ac4-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d2ac4-129">RELATED LINKS</span></span>

[<span data-ttu-id="d2ac4-130">Cmdlets do Insights Operacionais do Azure</span><span class="sxs-lookup"><span data-stu-id="d2ac4-130">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

[<span data-ttu-id="d2ac4-131">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="d2ac4-131">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


