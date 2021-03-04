---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/get-azoperationalinsightslinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsLinkedService.md
ms.openlocfilehash: 71a715386a4d5646f1c9015244ad8a096313bb64
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887086"
---
# <span data-ttu-id="fe9ee-101">Get-AzOperationalInsightsLinkedService</span><span class="sxs-lookup"><span data-stu-id="fe9ee-101">Get-AzOperationalInsightsLinkedService</span></span>

## <span data-ttu-id="fe9ee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fe9ee-102">SYNOPSIS</span></span>
<span data-ttu-id="fe9ee-103">Obter ou listar serviço vinculado para espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="fe9ee-103">Get or list linked service for workspace</span></span>

## <span data-ttu-id="fe9ee-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="fe9ee-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsLinkedService [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-LinkedServiceName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fe9ee-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="fe9ee-105">DESCRIPTION</span></span>
<span data-ttu-id="fe9ee-106">Obter ou listar serviço vinculado para espaço de trabalho, lista quando "-LinkedServiceName" não foi fornecido</span><span class="sxs-lookup"><span data-stu-id="fe9ee-106">Get or list linked service for workspace, list when "-LinkedServiceName" was not provided</span></span>

## <span data-ttu-id="fe9ee-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fe9ee-107">EXAMPLES</span></span>

### <span data-ttu-id="fe9ee-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="fe9ee-108">Example 1</span></span>
```powershell
Get-AzOperationalInsightsLinkedService -ResourceGroupName {rg-name} -WorkspaceName {workspace-name} -LinkedServiceName cluster

Id                    : /subscriptions/{subscription}/resourcegroups/{rg-name}/providers/microsoft.operationalinsights/workspaces/{workspace-name}/linkedservices/cluster
Name                  : {cluster-name}/Cluster
Type                  : Microsoft.OperationalInsights/workspaces/linkedServices
ResourceId            :
WriteAccessResourceId : /subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.OperationalInsights/clusters/{cluster-name}
ProvisioningState     : ProvisioningAccount
Tags                  :
```

<span data-ttu-id="fe9ee-109">Obter serviço vinculado para espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="fe9ee-109">Get linked service for workspace</span></span>

## <span data-ttu-id="fe9ee-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="fe9ee-110">PARAMETERS</span></span>

### <span data-ttu-id="fe9ee-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe9ee-111">-DefaultProfile</span></span>
<span data-ttu-id="fe9ee-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fe9ee-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe9ee-113">-LinkedServiceName</span><span class="sxs-lookup"><span data-stu-id="fe9ee-113">-LinkedServiceName</span></span>
<span data-ttu-id="fe9ee-114">O nome do serviço vinculado.</span><span class="sxs-lookup"><span data-stu-id="fe9ee-114">The linked service name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe9ee-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe9ee-115">-ResourceGroupName</span></span>
<span data-ttu-id="fe9ee-116">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="fe9ee-116">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe9ee-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="fe9ee-117">-WorkspaceName</span></span>
<span data-ttu-id="fe9ee-118">O nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="fe9ee-118">The workspace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe9ee-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe9ee-119">CommonParameters</span></span>
<span data-ttu-id="fe9ee-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe9ee-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe9ee-121">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fe9ee-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe9ee-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fe9ee-122">INPUTS</span></span>

### <span data-ttu-id="fe9ee-123">System.String</span><span class="sxs-lookup"><span data-stu-id="fe9ee-123">System.String</span></span>

## <span data-ttu-id="fe9ee-124">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="fe9ee-124">OUTPUTS</span></span>

### <span data-ttu-id="fe9ee-125">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="fe9ee-125">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedService</span></span>

## <span data-ttu-id="fe9ee-126">NOTES</span><span class="sxs-lookup"><span data-stu-id="fe9ee-126">NOTES</span></span>

## <span data-ttu-id="fe9ee-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fe9ee-127">RELATED LINKS</span></span>
