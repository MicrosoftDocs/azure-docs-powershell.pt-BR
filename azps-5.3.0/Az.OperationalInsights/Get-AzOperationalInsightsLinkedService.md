---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightslinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsLinkedService.md
ms.openlocfilehash: 14f1f96dd533492aedd1c4ed187e380c021a1b5f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98434563"
---
# <span data-ttu-id="294eb-101">Get-AzOperationalInsightsLinkedService</span><span class="sxs-lookup"><span data-stu-id="294eb-101">Get-AzOperationalInsightsLinkedService</span></span>

## <span data-ttu-id="294eb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="294eb-102">SYNOPSIS</span></span>
<span data-ttu-id="294eb-103">Obter ou listar o serviço vinculado para o espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="294eb-103">Get or list linked service for workspace</span></span>

## <span data-ttu-id="294eb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="294eb-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsLinkedService [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-LinkedServiceName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="294eb-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="294eb-105">DESCRIPTION</span></span>
<span data-ttu-id="294eb-106">Obter ou listar o serviço vinculado para o espaço de trabalho, listar quando "-LinkedServiceName" não foi fornecido</span><span class="sxs-lookup"><span data-stu-id="294eb-106">Get or list linked service for workspace, list when "-LinkedServiceName" was not provided</span></span>

## <span data-ttu-id="294eb-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="294eb-107">EXAMPLES</span></span>

### <span data-ttu-id="294eb-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="294eb-108">Example 1</span></span>
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

<span data-ttu-id="294eb-109">Obter serviço vinculado para espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="294eb-109">Get linked service for workspace</span></span>

## <span data-ttu-id="294eb-110">OS</span><span class="sxs-lookup"><span data-stu-id="294eb-110">PARAMETERS</span></span>

### <span data-ttu-id="294eb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="294eb-111">-DefaultProfile</span></span>
<span data-ttu-id="294eb-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="294eb-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="294eb-113">-LinkedServiceName</span><span class="sxs-lookup"><span data-stu-id="294eb-113">-LinkedServiceName</span></span>
<span data-ttu-id="294eb-114">O nome do serviço vinculado.</span><span class="sxs-lookup"><span data-stu-id="294eb-114">The linked service name.</span></span>

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

### <span data-ttu-id="294eb-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="294eb-115">-ResourceGroupName</span></span>
<span data-ttu-id="294eb-116">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="294eb-116">The resource group name.</span></span>

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

### <span data-ttu-id="294eb-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="294eb-117">-WorkspaceName</span></span>
<span data-ttu-id="294eb-118">O nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="294eb-118">The workspace name.</span></span>

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

### <span data-ttu-id="294eb-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="294eb-119">CommonParameters</span></span>
<span data-ttu-id="294eb-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="294eb-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="294eb-121">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="294eb-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="294eb-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="294eb-122">INPUTS</span></span>

### <span data-ttu-id="294eb-123">System. String</span><span class="sxs-lookup"><span data-stu-id="294eb-123">System.String</span></span>

## <span data-ttu-id="294eb-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="294eb-124">OUTPUTS</span></span>

### <span data-ttu-id="294eb-125">Microsoft. Azure. Commands. OperationalInsights. Models. PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="294eb-125">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedService</span></span>

## <span data-ttu-id="294eb-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="294eb-126">NOTES</span></span>

## <span data-ttu-id="294eb-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="294eb-127">RELATED LINKS</span></span>
