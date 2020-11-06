---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 818A048F-7CBE-4845-BBC2-6420CE48199A
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsworkspaceusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceUsage.md
ms.openlocfilehash: 04a62f4929e89dd4bff4d088d84325b0bdbb140b
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/13/2020
ms.locfileid: "93601932"
---
# <span data-ttu-id="2609a-101">Get-AzOperationalInsightsWorkspaceUsage</span><span class="sxs-lookup"><span data-stu-id="2609a-101">Get-AzOperationalInsightsWorkspaceUsage</span></span>

## <span data-ttu-id="2609a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2609a-102">SYNOPSIS</span></span>
<span data-ttu-id="2609a-103">Obtém os dados de uso de um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="2609a-103">Gets the usage data for a workspace.</span></span>

## <span data-ttu-id="2609a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2609a-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsWorkspaceUsage [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2609a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2609a-105">DESCRIPTION</span></span>
<span data-ttu-id="2609a-106">O cmdlet **Get-AzOperationalInsightsWorkspaceUsage** recupera os dados de uso de um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="2609a-106">The **Get-AzOperationalInsightsWorkspaceUsage** cmdlet retrieves the usage data for a workspace.</span></span>
<span data-ttu-id="2609a-107">Isso expõe quantos dados foram analisados pelo espaço de trabalho em um determinado período.</span><span class="sxs-lookup"><span data-stu-id="2609a-107">This exposes how much data has been analyzed by the workspace over a certain period.</span></span>

## <span data-ttu-id="2609a-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2609a-108">EXAMPLES</span></span>

### <span data-ttu-id="2609a-109">Exemplo 1: obter dados de uso por nome do espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="2609a-109">Example 1: Get usage data by workspace name</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspaceUsage -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
```

<span data-ttu-id="2609a-110">Esse comando obtém os detalhes de uso do espaço de trabalho chamado MyWorkspace no grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="2609a-110">This command gets the usage details for the workspace named MyWorkspace in the specified resource group.</span></span>

### <span data-ttu-id="2609a-111">Exemplo 2: obter dados de uso usando o pipeline</span><span class="sxs-lookup"><span data-stu-id="2609a-111">Example 2: Get usage data using the pipeline</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Get-AzOperationalInsightsWorkspaceUsage
```

<span data-ttu-id="2609a-112">Esse comando obtém o espaço de trabalho chamado MyWorkspace usando o cmdlet Get-AzOperationalInsightsWorkspace e, em seguida, passa o espaço de trabalho para o cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="2609a-112">This command gets the workspace named MyWorkSpace using the Get-AzOperationalInsightsWorkspace cmdlet, and then passes the workspace to the current cmdlet.</span></span>
<span data-ttu-id="2609a-113">O comando obtém os detalhes de uso para esse espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="2609a-113">The command gets the usage details for that workspace.</span></span>

## <span data-ttu-id="2609a-114">OS</span><span class="sxs-lookup"><span data-stu-id="2609a-114">PARAMETERS</span></span>

### <span data-ttu-id="2609a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2609a-115">-DefaultProfile</span></span>
<span data-ttu-id="2609a-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="2609a-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2609a-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="2609a-117">-Name</span></span>
<span data-ttu-id="2609a-118">Especifica o nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="2609a-118">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="2609a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2609a-119">-ResourceGroupName</span></span>
<span data-ttu-id="2609a-120">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="2609a-120">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="2609a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2609a-121">CommonParameters</span></span>
<span data-ttu-id="2609a-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2609a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2609a-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2609a-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2609a-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2609a-124">INPUTS</span></span>

### <span data-ttu-id="2609a-125">System. String</span><span class="sxs-lookup"><span data-stu-id="2609a-125">System.String</span></span>

## <span data-ttu-id="2609a-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2609a-126">OUTPUTS</span></span>

### <span data-ttu-id="2609a-127">Microsoft. Azure. Commands. OperationalInsights. Models. PSUsageMetric</span><span class="sxs-lookup"><span data-stu-id="2609a-127">Microsoft.Azure.Commands.OperationalInsights.Models.PSUsageMetric</span></span>

## <span data-ttu-id="2609a-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2609a-128">NOTES</span></span>

## <span data-ttu-id="2609a-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2609a-129">RELATED LINKS</span></span>

[<span data-ttu-id="2609a-130">Cmdlets do Azure Operational insights</span><span class="sxs-lookup"><span data-stu-id="2609a-130">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)

[<span data-ttu-id="2609a-131">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="2609a-131">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


