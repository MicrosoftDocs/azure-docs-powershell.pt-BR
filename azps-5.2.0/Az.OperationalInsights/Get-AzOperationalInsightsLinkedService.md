---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightslinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsLinkedService.md
ms.openlocfilehash: 14f1f96dd533492aedd1c4ed187e380c021a1b5f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98264090"
---
# <span data-ttu-id="68a09-101">Get-AzOperationalInsightsLinkedService</span><span class="sxs-lookup"><span data-stu-id="68a09-101">Get-AzOperationalInsightsLinkedService</span></span>

## <span data-ttu-id="68a09-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="68a09-102">SYNOPSIS</span></span>
<span data-ttu-id="68a09-103">Obter ou listar o serviço vinculado para o espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="68a09-103">Get or list linked service for workspace</span></span>

## <span data-ttu-id="68a09-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="68a09-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsLinkedService [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-LinkedServiceName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="68a09-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="68a09-105">DESCRIPTION</span></span>
<span data-ttu-id="68a09-106">Obter ou listar o serviço vinculado para o espaço de trabalho, listar quando "-LinkedServiceName" não foi fornecido</span><span class="sxs-lookup"><span data-stu-id="68a09-106">Get or list linked service for workspace, list when "-LinkedServiceName" was not provided</span></span>

## <span data-ttu-id="68a09-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="68a09-107">EXAMPLES</span></span>

### <span data-ttu-id="68a09-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="68a09-108">Example 1</span></span>
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

<span data-ttu-id="68a09-109">Obter serviço vinculado para espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="68a09-109">Get linked service for workspace</span></span>

## <span data-ttu-id="68a09-110">OS</span><span class="sxs-lookup"><span data-stu-id="68a09-110">PARAMETERS</span></span>

### <span data-ttu-id="68a09-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68a09-111">-DefaultProfile</span></span>
<span data-ttu-id="68a09-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="68a09-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="68a09-113">-LinkedServiceName</span><span class="sxs-lookup"><span data-stu-id="68a09-113">-LinkedServiceName</span></span>
<span data-ttu-id="68a09-114">O nome do serviço vinculado.</span><span class="sxs-lookup"><span data-stu-id="68a09-114">The linked service name.</span></span>

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

### <span data-ttu-id="68a09-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68a09-115">-ResourceGroupName</span></span>
<span data-ttu-id="68a09-116">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="68a09-116">The resource group name.</span></span>

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

### <span data-ttu-id="68a09-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="68a09-117">-WorkspaceName</span></span>
<span data-ttu-id="68a09-118">O nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="68a09-118">The workspace name.</span></span>

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

### <span data-ttu-id="68a09-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68a09-119">CommonParameters</span></span>
<span data-ttu-id="68a09-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68a09-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68a09-121">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="68a09-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68a09-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="68a09-122">INPUTS</span></span>

### <span data-ttu-id="68a09-123">System. String</span><span class="sxs-lookup"><span data-stu-id="68a09-123">System.String</span></span>

## <span data-ttu-id="68a09-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="68a09-124">OUTPUTS</span></span>

### <span data-ttu-id="68a09-125">Microsoft. Azure. Commands. OperationalInsights. Models. PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="68a09-125">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedService</span></span>

## <span data-ttu-id="68a09-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="68a09-126">NOTES</span></span>

## <span data-ttu-id="68a09-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="68a09-127">RELATED LINKS</span></span>
