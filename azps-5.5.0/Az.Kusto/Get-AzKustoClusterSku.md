---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustoclustersku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterSku.md
ms.openlocfilehash: 42fed776d1f77211c7967dd6313d0ddd1e04b65a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113033"
---
# <span data-ttu-id="d8614-101">Get-AzKustoClusterSku</span><span class="sxs-lookup"><span data-stu-id="d8614-101">Get-AzKustoClusterSku</span></span>

## <span data-ttu-id="d8614-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d8614-102">SYNOPSIS</span></span>
<span data-ttu-id="d8614-103">Lista SKUs qualificadas para provedor de recursos de Kusto.</span><span class="sxs-lookup"><span data-stu-id="d8614-103">Lists eligible SKUs for Kusto resource provider.</span></span>

## <span data-ttu-id="d8614-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d8614-104">SYNTAX</span></span>

### <span data-ttu-id="d8614-105">Lista (Padrão)</span><span class="sxs-lookup"><span data-stu-id="d8614-105">List (Default)</span></span>
```
Get-AzKustoClusterSku [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d8614-106">Lista1</span><span class="sxs-lookup"><span data-stu-id="d8614-106">List1</span></span>
```
Get-AzKustoClusterSku -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="d8614-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="d8614-107">DESCRIPTION</span></span>
<span data-ttu-id="d8614-108">Lista SKUs qualificadas para provedor de recursos de Kusto.</span><span class="sxs-lookup"><span data-stu-id="d8614-108">Lists eligible SKUs for Kusto resource provider.</span></span>

## <span data-ttu-id="d8614-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d8614-109">EXAMPLES</span></span>

### <span data-ttu-id="d8614-110">Exemplo 1: Lista SKUs qualificadas</span><span class="sxs-lookup"><span data-stu-id="d8614-110">Example 1: Lists eligible SKUs</span></span>
```powershell
PS C:\> Get-AzKustoClusterSku

Location             Name                        ResourceType Tier
--------             ----                        ------------ ----
{eastus2}            D13_v2                      clusters     Standard
{eastus2}            D14_v2                      clusters     Standard
{eastus2}            L8                          clusters     Standard
{eastus2}            L16                         clusters     Standard
{eastus2}            D11_v2                      clusters     Standard
{eastus2}            D12_v2                      clusters     Standard
{eastus2}            L4                          clusters     Standard
{eastus2}            Standard_D13_v2             clusters     Standard
{eastus2}            Standard_D14_v2             clusters     Standard
{eastus2}            Standard_L8s                clusters     Standard
{eastus2}            Standard_L16s               clusters     Standard
{eastus2}            Standard_D11_v2             clusters     Standard
{eastus2}            Standard_D12_v2             clusters     Standard
{eastus2}            Standard_L4s                clusters     Standard
{eastus2}            Standard_DS13_v2+1TB_PS     clusters     Standard
{eastus2}            Standard_DS13_v2+2TB_PS     clusters     Standard
{eastus2}            Standard_DS14_v2+3TB_PS     clusters     Standard
{eastus2}            Standard_DS14_v2+4TB_PS     clusters     Standard
{eastus2}            Dev(No SLA)_Standard_D11_v2 clusters     Basic
{westcentralus}      D13_v2                      clusters     Standard
{westcentralus}      D14_v2                      clusters     Standard
{westcentralus}      D11_v2                      clusters     Standard
{westcentralus}      D12_v2                      clusters     Standard
{westcentralus}      Standard_D13_v2             clusters     Standard
{westcentralus}      Standard_D14_v2             clusters     Standard
{westcentralus}      Standard_D11_v2             clusters     Standard
{westcentralus}      Standard_D12_v2             clusters     Standard
{westcentralus}      Standard_DS13_v2+1TB_PS     clusters     Standard
{westcentralus}      Standard_DS13_v2+2TB_PS     clusters     Standard
{westcentralus}      Standard_DS14_v2+3TB_PS     clusters     Standard
{westcentralus}      Standard_DS14_v2+4TB_PS     clusters     Standard
...
```

<span data-ttu-id="d8614-111">O comando acima lista SKUs qualificadas.</span><span class="sxs-lookup"><span data-stu-id="d8614-111">The above command lists eligible SKUs.</span></span>

### <span data-ttu-id="d8614-112">Exemplo 2: Lista SKUs qualificadas para cluster específico</span><span class="sxs-lookup"><span data-stu-id="d8614-112">Example 2: Lists eligible SKUs for specific cluster</span></span>
```powershell
PS C:\>  Get-AzKustoClusterSku -ResourceGroupName testrg -ClusterName testnewkustocluster

ResourceType
------------
Microsoft.Kusto/clusters
Microsoft.Kusto/clusters
Microsoft.Kusto/clusters
Microsoft.Kusto/clusters
Microsoft.Kusto/clusters
Microsoft.Kusto/clusters
...
```

<span data-ttu-id="d8614-113">O comando acima lista SKUs qualificadas para cluster específico</span><span class="sxs-lookup"><span data-stu-id="d8614-113">The above command lists eligible SKUs for specific cluster</span></span>

## <span data-ttu-id="d8614-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d8614-114">PARAMETERS</span></span>

### <span data-ttu-id="d8614-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="d8614-115">-ClusterName</span></span>
<span data-ttu-id="d8614-116">O nome do cluster de Kusto.</span><span class="sxs-lookup"><span data-stu-id="d8614-116">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8614-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8614-117">-DefaultProfile</span></span>
<span data-ttu-id="d8614-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d8614-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8614-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8614-119">-ResourceGroupName</span></span>
<span data-ttu-id="d8614-120">O nome do grupo de recursos que contém o cluster de Kusto.</span><span class="sxs-lookup"><span data-stu-id="d8614-120">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8614-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d8614-121">-SubscriptionId</span></span>
<span data-ttu-id="d8614-122">Obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d8614-122">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="d8614-123">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="d8614-123">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8614-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8614-124">CommonParameters</span></span>
<span data-ttu-id="d8614-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8614-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8614-126">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d8614-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8614-127">Entradas</span><span class="sxs-lookup"><span data-stu-id="d8614-127">INPUTS</span></span>

## <span data-ttu-id="d8614-128">Saídas</span><span class="sxs-lookup"><span data-stu-id="d8614-128">OUTPUTS</span></span>

### <span data-ttu-id="d8614-129">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IAzureResourceSku</span><span class="sxs-lookup"><span data-stu-id="d8614-129">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IAzureResourceSku</span></span>

### <span data-ttu-id="d8614-130">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ISkuDescription</span><span class="sxs-lookup"><span data-stu-id="d8614-130">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ISkuDescription</span></span>

## <span data-ttu-id="d8614-131">Notas</span><span class="sxs-lookup"><span data-stu-id="d8614-131">NOTES</span></span>

<span data-ttu-id="d8614-132">Aliases</span><span class="sxs-lookup"><span data-stu-id="d8614-132">ALIASES</span></span>

## <span data-ttu-id="d8614-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d8614-133">RELATED LINKS</span></span>

