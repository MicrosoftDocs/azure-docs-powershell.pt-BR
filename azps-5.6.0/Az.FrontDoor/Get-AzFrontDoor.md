---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/get-azfrontdoor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoor.md
ms.openlocfilehash: f48fadb740fdca823c2513d68a2f77e0d34c4631
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885726"
---
# <span data-ttu-id="238b7-101">Get-AzFrontDoor</span><span class="sxs-lookup"><span data-stu-id="238b7-101">Get-AzFrontDoor</span></span>

## <span data-ttu-id="238b7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="238b7-102">SYNOPSIS</span></span>
<span data-ttu-id="238b7-103">Obter balanceador de carga da Porta Frontal</span><span class="sxs-lookup"><span data-stu-id="238b7-103">Get Front Door load balancer</span></span>

## <span data-ttu-id="238b7-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="238b7-104">SYNTAX</span></span>

```
Get-AzFrontDoor [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="238b7-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="238b7-105">DESCRIPTION</span></span>
<span data-ttu-id="238b7-106">O cmdlet **Get-AzFrontDoorGet** obtém todas as Portas Front existentes na assinatura atual que corresponde às informações fornecidas.</span><span class="sxs-lookup"><span data-stu-id="238b7-106">The **Get-AzFrontDoor** cmdletGet gets all existing Front Doors in the current subscription that matches provided information.</span></span>

## <span data-ttu-id="238b7-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="238b7-107">EXAMPLES</span></span>

### <span data-ttu-id="238b7-108">Exemplo 1: Obter todos os FrontDoors na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="238b7-108">Example 1: Get all FrontDoors in the current subscription.</span></span>
```powershell
PS C:\> Get-AzFrontDoor

FriendlyName          : frontdoor1
FrontDoorId           : {guid}
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
FrontDoorId           : {guid}
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

<span data-ttu-id="238b7-109">Obter todos os FrontDoors na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="238b7-109">Get all FrontDoors in the current subscription.</span></span>

### <span data-ttu-id="238b7-110">Exemplo 2: Obter todos os FrontDoors no grupo de recursos "rg1" na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="238b7-110">Example 2: Get all FrontDoors in resource group "rg1" in the current subscription.</span></span>
```powershell
PS C:\> Get-AzFrontDoor -ResourceGroupName "rg1"

FriendlyName          : frontdoor1
FrontDoorId           : {guid}
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
FrontDoorId           : {guid}
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

<span data-ttu-id="238b7-111">Obter todos os FrontDoors no grupo de recursos "rg1" na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="238b7-111">Get all FrontDoors in resource group "rg1" in the current subscription.</span></span>

### <span data-ttu-id="238b7-112">Exemplo 3: Obter os FrontDoors no grupo de recursos "rg1" com o nome "frontDoor1" na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="238b7-112">Example 3: Get the FrontDoors in resource group "rg1" with name "frontDoor1" in the current subscription.</span></span>
```powershell
PS C:\> Get-AzFrontDoor -ResourceGroupName "rg1" -Name "frontDoor1"

FriendlyName          : frontdoor1
FrontDoorId           : {guid}
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

<span data-ttu-id="238b7-113">Obter o FrontDoors no grupo de recursos "rg1" com o nome "frontDoor1" na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="238b7-113">Get the FrontDoors in resource group "rg1" with name "frontDoor1" in the current subscription.</span></span>

## <span data-ttu-id="238b7-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="238b7-114">PARAMETERS</span></span>

### <span data-ttu-id="238b7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="238b7-115">-DefaultProfile</span></span>
<span data-ttu-id="238b7-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="238b7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="238b7-117">-Name</span><span class="sxs-lookup"><span data-stu-id="238b7-117">-Name</span></span>
<span data-ttu-id="238b7-118">Nome da porta frontal.</span><span class="sxs-lookup"><span data-stu-id="238b7-118">Front Door name.</span></span>

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

### <span data-ttu-id="238b7-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="238b7-119">-ResourceGroupName</span></span>
<span data-ttu-id="238b7-120">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="238b7-120">The resource group name.</span></span>

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

### <span data-ttu-id="238b7-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="238b7-121">CommonParameters</span></span>
<span data-ttu-id="238b7-122">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="238b7-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="238b7-123">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="238b7-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="238b7-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="238b7-124">INPUTS</span></span>

### <span data-ttu-id="238b7-125">Nenhum</span><span class="sxs-lookup"><span data-stu-id="238b7-125">None</span></span>

## <span data-ttu-id="238b7-126">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="238b7-126">OUTPUTS</span></span>

### <span data-ttu-id="238b7-127">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span><span class="sxs-lookup"><span data-stu-id="238b7-127">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>

## <span data-ttu-id="238b7-128">NOTES</span><span class="sxs-lookup"><span data-stu-id="238b7-128">NOTES</span></span>

## <span data-ttu-id="238b7-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="238b7-129">RELATED LINKS</span></span>

<span data-ttu-id="238b7-130">[New-AzFrontDoor](./New-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md) 
 [Remove-AzFrontDoor](./Remove-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="238b7-130">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)
[Remove-AzFrontDoor](./Remove-AzFrontDoor.md)</span></span>
