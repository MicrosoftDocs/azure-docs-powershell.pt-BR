---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustoclustersku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterSku.md
ms.openlocfilehash: 88b3104512b1cad4cddf98f521b44c6b638c05b0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98264212"
---
# <span data-ttu-id="d4e61-101">Get-AzKustoClusterSku</span><span class="sxs-lookup"><span data-stu-id="d4e61-101">Get-AzKustoClusterSku</span></span>

## <span data-ttu-id="d4e61-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d4e61-102">SYNOPSIS</span></span>
<span data-ttu-id="d4e61-103">Lista SKUs qualificados para o provedor de recursos Kusto.</span><span class="sxs-lookup"><span data-stu-id="d4e61-103">Lists eligible SKUs for Kusto resource provider.</span></span>

## <span data-ttu-id="d4e61-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d4e61-104">SYNTAX</span></span>

### <span data-ttu-id="d4e61-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="d4e61-105">List (Default)</span></span>
```
Get-AzKustoClusterSku [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d4e61-106">List1</span><span class="sxs-lookup"><span data-stu-id="d4e61-106">List1</span></span>
```
Get-AzKustoClusterSku -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="d4e61-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d4e61-107">DESCRIPTION</span></span>
<span data-ttu-id="d4e61-108">Lista SKUs qualificados para o provedor de recursos Kusto.</span><span class="sxs-lookup"><span data-stu-id="d4e61-108">Lists eligible SKUs for Kusto resource provider.</span></span>

## <span data-ttu-id="d4e61-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d4e61-109">EXAMPLES</span></span>

### <span data-ttu-id="d4e61-110">Exemplo 1: lista SKUs qualificados</span><span class="sxs-lookup"><span data-stu-id="d4e61-110">Example 1: Lists eligible SKUs</span></span>
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

<span data-ttu-id="d4e61-111">O comando acima lista os SKUs qualificados.</span><span class="sxs-lookup"><span data-stu-id="d4e61-111">The above command lists eligible SKUs.</span></span>

### <span data-ttu-id="d4e61-112">Exemplo 2: lista SKUs qualificados para um cluster específico</span><span class="sxs-lookup"><span data-stu-id="d4e61-112">Example 2: Lists eligible SKUs for specific cluster</span></span>
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

<span data-ttu-id="d4e61-113">O comando acima lista os SKUs qualificados para um cluster específico</span><span class="sxs-lookup"><span data-stu-id="d4e61-113">The above command lists eligible SKUs for specific cluster</span></span>

## <span data-ttu-id="d4e61-114">OS</span><span class="sxs-lookup"><span data-stu-id="d4e61-114">PARAMETERS</span></span>

### <span data-ttu-id="d4e61-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="d4e61-115">-ClusterName</span></span>
<span data-ttu-id="d4e61-116">O nome do cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="d4e61-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="d4e61-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4e61-117">-DefaultProfile</span></span>
<span data-ttu-id="d4e61-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d4e61-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d4e61-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4e61-119">-ResourceGroupName</span></span>
<span data-ttu-id="d4e61-120">O nome do grupo de recursos que contém o cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="d4e61-120">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="d4e61-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d4e61-121">-SubscriptionId</span></span>
<span data-ttu-id="d4e61-122">Obtém as credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d4e61-122">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="d4e61-123">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="d4e61-123">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="d4e61-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4e61-124">CommonParameters</span></span>
<span data-ttu-id="d4e61-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4e61-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4e61-126">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d4e61-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4e61-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d4e61-127">INPUTS</span></span>

## <span data-ttu-id="d4e61-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d4e61-128">OUTPUTS</span></span>

### <span data-ttu-id="d4e61-129">Microsoft. Azure. PowerShell. cmdlets. Kusto. Models. Api20200614. IAzureResourceSku</span><span class="sxs-lookup"><span data-stu-id="d4e61-129">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IAzureResourceSku</span></span>

### <span data-ttu-id="d4e61-130">Microsoft. Azure. PowerShell. cmdlets. Kusto. Models. Api20200614. ISkuDescription</span><span class="sxs-lookup"><span data-stu-id="d4e61-130">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ISkuDescription</span></span>

## <span data-ttu-id="d4e61-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d4e61-131">NOTES</span></span>

<span data-ttu-id="d4e61-132">ALIASES</span><span class="sxs-lookup"><span data-stu-id="d4e61-132">ALIASES</span></span>

## <span data-ttu-id="d4e61-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d4e61-133">RELATED LINKS</span></span>

