---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/get-azfrontdoor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoor.md
ms.openlocfilehash: 6dd40ff6bdf94d95b9fe31ead7ce6bde53c7042b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93596436"
---
# <span data-ttu-id="0d9d8-101">Get-AzFrontDoor</span><span class="sxs-lookup"><span data-stu-id="0d9d8-101">Get-AzFrontDoor</span></span>

## <span data-ttu-id="0d9d8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0d9d8-102">SYNOPSIS</span></span>
<span data-ttu-id="0d9d8-103">Obter balanceador de carga de porta frontal</span><span class="sxs-lookup"><span data-stu-id="0d9d8-103">Get Front Door load balancer</span></span>

## <span data-ttu-id="0d9d8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0d9d8-104">SYNTAX</span></span>

```
Get-AzFrontDoor [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0d9d8-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0d9d8-105">DESCRIPTION</span></span>
<span data-ttu-id="0d9d8-106">O cmdletGet **Get-AzFrontDoor** obtém todas as portas frontais existentes na assinatura atual que corresponde às informações fornecidas.</span><span class="sxs-lookup"><span data-stu-id="0d9d8-106">The **Get-AzFrontDoor** cmdletGet gets all existing Front Doors in the current subscription that matches provided information.</span></span>

## <span data-ttu-id="0d9d8-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0d9d8-107">EXAMPLES</span></span>

### <span data-ttu-id="0d9d8-108">Exemplo 1: obter todos os FrontDoors na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="0d9d8-108">Example 1: Get all FrontDoors in the current subscription.</span></span>
```powershell
PS C:\> Get-AzFrontDoor

FriendlyName          : frontdoor1
RoutingRules          : {routingrule1}
BackendPools          : {backendpool1}
HealthProbeSettings   : {healthProbeSetting1}
LoadBalancingSettings : {loadbalancingsetting1}
FrontendEndpoints     : {frontendendpoint1}
EnabledState          : Enabled
ResourceState         : Enabled
ProvisioningState     : Succeeded
Cname                 :
Tags                  : {tag1, tag2}
Id                    : /subscriptions/{guid}/resourcegroups/{guid1}/providers/M
                        icrosoft.Network/frontdoors/frontdoor1
Name                  : frontdoor1
Type                  : Microsoft.Network/frontdoor1

FriendlyName          : frontdoor1
RoutingRules          : {routingrule1}
BackendPools          : {backendpool1}
HealthProbeSettings   : {healthProbeSetting1}
LoadBalancingSettings : {loadbalancingsetting1}
FrontendEndpoints     : {frontendendpoint1}
EnabledState          : Enabled
ResourceState         : Enabled
ProvisioningState     : Succeeded
Cname                 :
Tags                  : {tag1, tag2}
Id                    : /subscriptions/{guid}/resourcegroups/{guid2}/providers/M
                        icrosoft.Network/frontdoors/frontdoor1
Name                  : frontdoor1
Type                  : Microsoft.Network/frontdoor1
```

<span data-ttu-id="0d9d8-109">Obtenha todos os FrontDoors na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="0d9d8-109">Get all FrontDoors in the current subscription.</span></span>

### <span data-ttu-id="0d9d8-110">Exemplo 2: obter todos os FrontDoors no grupo de recursos "Rg1" na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="0d9d8-110">Example 2: Get all FrontDoors in resource group "rg1" in the current subscription.</span></span>
```powershell
PS C:\> Get-AzFrontDoor -ResourceGroupName "rg1"

FriendlyName          : frontdoor1
RoutingRules          : {routingrule1}
BackendPools          : {backendpool1}
HealthProbeSettings   : {healthProbeSetting1}
LoadBalancingSettings : {loadbalancingsetting1}
FrontendEndpoints     : {frontendendpoint1}
EnabledState          : Enabled
ResourceState         : Enabled
ProvisioningState     : Succeeded
Cname                 :
Tags                  : {tag1, tag2}
Id                    : /subscriptions/{guid}/resourcegroups/rg1/providers/M
                        icrosoft.Network/frontdoors/frontdoor1
Name                  : frontdoor1
Type                  : Microsoft.Network/frontdoor1

FriendlyName          : frontdoor2
RoutingRules          : {routingrule1}
BackendPools          : {backendpool1}
HealthProbeSettings   : {healthProbeSetting1}
LoadBalancingSettings : {loadbalancingsetting1}
FrontendEndpoints     : {frontendendpoint1}
EnabledState          : Enabled
ResourceState         : Enabled
ProvisioningState     : Succeeded
Cname                 :
Tags                  : {tag1, tag2}
Id                    : /subscriptions/{guid}/resourcegroups/rg1/providers/M
                        icrosoft.Network/frontdoors/frontdoor1
Name                  : frontdoor1
Type                  : Microsoft.Network/frontdoor1
```

<span data-ttu-id="0d9d8-111">Obtenha todos os FrontDoors no grupo de recursos "Rg1" na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="0d9d8-111">Get all FrontDoors in resource group "rg1" in the current subscription.</span></span>

### <span data-ttu-id="0d9d8-112">Exemplo 3: obter o FrontDoors no grupo de recursos "Rg1" com nome "frontDoor1" na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="0d9d8-112">Example 3: Get the FrontDoors in resource group "rg1" with name "frontDoor1" in the current subscription.</span></span>
```powershell
PS C:\> Get-AzFrontDoor -ResourceGroupName "rg1" -Name "frontDoor1"

FriendlyName          : frontdoor1
RoutingRules          : {routingrule1}
BackendPools          : {backendpool1}
HealthProbeSettings   : {healthProbeSetting1}
LoadBalancingSettings : {loadbalancingsetting1}
FrontendEndpoints     : {frontendendpoint1}
EnabledState          : Enabled
ResourceState         : Enabled
ProvisioningState     : Succeeded
Cname                 :
Tags                  : {tag1, tag2}
Id                    : /subscriptions/{guid}/resourcegroups/rg1/providers/M
                        icrosoft.Network/frontdoors/frontdoor1
Name                  : frontdoor1
Type                  : Microsoft.Network/frontdoor1
```

<span data-ttu-id="0d9d8-113">Obtenha o FrontDoors no grupo de recursos "Rg1" com o nome "frontDoor1" na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="0d9d8-113">Get the FrontDoors in resource group "rg1" with name "frontDoor1" in the current subscription.</span></span>

## <span data-ttu-id="0d9d8-114">OS</span><span class="sxs-lookup"><span data-stu-id="0d9d8-114">PARAMETERS</span></span>

### <span data-ttu-id="0d9d8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d9d8-115">-DefaultProfile</span></span>
<span data-ttu-id="0d9d8-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0d9d8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0d9d8-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="0d9d8-117">-Name</span></span>
<span data-ttu-id="0d9d8-118">Nome da porta frontal.</span><span class="sxs-lookup"><span data-stu-id="0d9d8-118">Front Door name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d9d8-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d9d8-119">-ResourceGroupName</span></span>
<span data-ttu-id="0d9d8-120">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0d9d8-120">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d9d8-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d9d8-121">CommonParameters</span></span>
<span data-ttu-id="0d9d8-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d9d8-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d9d8-123">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0d9d8-123">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d9d8-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0d9d8-124">INPUTS</span></span>

### <span data-ttu-id="0d9d8-125">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="0d9d8-125">None</span></span>

## <span data-ttu-id="0d9d8-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0d9d8-126">OUTPUTS</span></span>

### <span data-ttu-id="0d9d8-127">Microsoft. Azure. Commands. FrontDoor. Models. PSFrontDoor</span><span class="sxs-lookup"><span data-stu-id="0d9d8-127">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>

## <span data-ttu-id="0d9d8-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0d9d8-128">NOTES</span></span>

## <span data-ttu-id="0d9d8-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0d9d8-129">RELATED LINKS</span></span>

<span data-ttu-id="0d9d8-130">[New-AzFrontDoor](./New-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md) 
 [Remove-AzFrontDoor](./Remove-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="0d9d8-130">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)
[Remove-AzFrontDoor](./Remove-AzFrontDoor.md)</span></span>
