---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsCluster.md
ms.openlocfilehash: aaa3522afb3bf021f2bf5fbff5ec6c3d9e14928f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98434576"
---
# <span data-ttu-id="2198e-101">Get-AzOperationalInsightsCluster</span><span class="sxs-lookup"><span data-stu-id="2198e-101">Get-AzOperationalInsightsCluster</span></span>

## <span data-ttu-id="2198e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2198e-102">SYNOPSIS</span></span>
<span data-ttu-id="2198e-103">Obter ou listar clusters</span><span class="sxs-lookup"><span data-stu-id="2198e-103">Get or list clusters</span></span>

## <span data-ttu-id="2198e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2198e-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsCluster [[-ResourceGroupName] <String>] [[-ClusterName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2198e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2198e-105">DESCRIPTION</span></span>
<span data-ttu-id="2198e-106">Obter ou listar clusters, listar clusters em grupo de recursos quando "-ClusterName" não foi fornecido, clusters de lista em assinatura quando "-ClusterName" e "ResourceGroupName" não foram fornecidos.</span><span class="sxs-lookup"><span data-stu-id="2198e-106">Get or list clusters, list clusters under resource group when "-ClusterName" was not provided, list clusters under subscription when "-ClusterName" and "ResourceGroupName" were not provided.</span></span>

## <span data-ttu-id="2198e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2198e-107">EXAMPLES</span></span>

### <span data-ttu-id="2198e-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2198e-108">Example 1</span></span>
```powershell
Get-AzOperationalInsightsCluster -ResourceGroupName {rg-name} -ClusterName {cluster-name}

Identity           : Microsoft.Azure.Commands.OperationalInsights.Models.PSIdentity
Sku                : Microsoft.Azure.Commands.OperationalInsights.Models.PSClusterSku
NextLink           :
ClusterId          : {cluster-id}
ProvisioningState  : Succeeded
KeyVaultProperties :
Location           : South Central US
Id                 : /subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.OperationalInsights/clusters/{cluster-name}
Name               : {cluster-name}
Type               : Microsoft.OperationalInsights/clusters
Tags               : {}
```

<span data-ttu-id="2198e-109">Obter cluster</span><span class="sxs-lookup"><span data-stu-id="2198e-109">Get cluster</span></span>

## <span data-ttu-id="2198e-110">OS</span><span class="sxs-lookup"><span data-stu-id="2198e-110">PARAMETERS</span></span>

### <span data-ttu-id="2198e-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="2198e-111">-ClusterName</span></span>
<span data-ttu-id="2198e-112">O nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="2198e-112">The cluster name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2198e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2198e-113">-DefaultProfile</span></span>
<span data-ttu-id="2198e-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2198e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2198e-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2198e-115">-ResourceGroupName</span></span>
<span data-ttu-id="2198e-116">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="2198e-116">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2198e-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2198e-117">CommonParameters</span></span>
<span data-ttu-id="2198e-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2198e-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2198e-119">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2198e-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2198e-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2198e-120">INPUTS</span></span>

### <span data-ttu-id="2198e-121">System. String</span><span class="sxs-lookup"><span data-stu-id="2198e-121">System.String</span></span>

## <span data-ttu-id="2198e-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2198e-122">OUTPUTS</span></span>

### <span data-ttu-id="2198e-123">Microsoft. Azure. Commands. OperationalInsights. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="2198e-123">Microsoft.Azure.Commands.OperationalInsights.Models.PSCluster</span></span>

## <span data-ttu-id="2198e-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2198e-124">NOTES</span></span>

## <span data-ttu-id="2198e-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2198e-125">RELATED LINKS</span></span>
