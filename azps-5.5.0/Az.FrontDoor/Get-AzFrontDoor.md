---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/get-azfrontdoor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoor.md
ms.openlocfilehash: 6cc7de36f51bc2fcb61950aa112c2f426358a506
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100126963"
---
# <span data-ttu-id="663a6-101">Get-AzFrontDoor</span><span class="sxs-lookup"><span data-stu-id="663a6-101">Get-AzFrontDoor</span></span>

## <span data-ttu-id="663a6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="663a6-102">SYNOPSIS</span></span>
<span data-ttu-id="663a6-103">Balanceador de carga da porta da frente</span><span class="sxs-lookup"><span data-stu-id="663a6-103">Get Front Door load balancer</span></span>

## <span data-ttu-id="663a6-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="663a6-104">SYNTAX</span></span>

```
Get-AzFrontDoor [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="663a6-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="663a6-105">DESCRIPTION</span></span>
<span data-ttu-id="663a6-106">O **cmdlet Get-AzFrontDoorGet** obtém todas as Portas Front existentes na assinatura atual que corresponde às informações fornecidas.</span><span class="sxs-lookup"><span data-stu-id="663a6-106">The **Get-AzFrontDoor** cmdletGet gets all existing Front Doors in the current subscription that matches provided information.</span></span>

## <span data-ttu-id="663a6-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="663a6-107">EXAMPLES</span></span>

### <span data-ttu-id="663a6-108">Exemplo 1: Obter todos os FrontDoors na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="663a6-108">Example 1: Get all FrontDoors in the current subscription.</span></span>
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

<span data-ttu-id="663a6-109">Obter todos os FrontDoors na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="663a6-109">Get all FrontDoors in the current subscription.</span></span>

### <span data-ttu-id="663a6-110">Exemplo 2: Obter todos os FrontDoors no grupo de recursos "rg1" na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="663a6-110">Example 2: Get all FrontDoors in resource group "rg1" in the current subscription.</span></span>
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

<span data-ttu-id="663a6-111">Obter todos os FrontDoors no grupo de recursos "rg1" na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="663a6-111">Get all FrontDoors in resource group "rg1" in the current subscription.</span></span>

### <span data-ttu-id="663a6-112">Exemplo 3: Obter o FrontDoors no grupo de recursos "rg1" com o nome "frontDoor1" na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="663a6-112">Example 3: Get the FrontDoors in resource group "rg1" with name "frontDoor1" in the current subscription.</span></span>
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

<span data-ttu-id="663a6-113">Obter o FrontDoors no grupo de recursos "rg1" com o nome "frontDoor1" na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="663a6-113">Get the FrontDoors in resource group "rg1" with name "frontDoor1" in the current subscription.</span></span>

## <span data-ttu-id="663a6-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="663a6-114">PARAMETERS</span></span>

### <span data-ttu-id="663a6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="663a6-115">-DefaultProfile</span></span>
<span data-ttu-id="663a6-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="663a6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="663a6-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="663a6-117">-Name</span></span>
<span data-ttu-id="663a6-118">Nome da porta da frente.</span><span class="sxs-lookup"><span data-stu-id="663a6-118">Front Door name.</span></span>

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

### <span data-ttu-id="663a6-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="663a6-119">-ResourceGroupName</span></span>
<span data-ttu-id="663a6-120">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="663a6-120">The resource group name.</span></span>

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

### <span data-ttu-id="663a6-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="663a6-121">CommonParameters</span></span>
<span data-ttu-id="663a6-122">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="663a6-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="663a6-123">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="663a6-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="663a6-124">Entradas</span><span class="sxs-lookup"><span data-stu-id="663a6-124">INPUTS</span></span>

### <span data-ttu-id="663a6-125">Nenhum</span><span class="sxs-lookup"><span data-stu-id="663a6-125">None</span></span>

## <span data-ttu-id="663a6-126">Saídas</span><span class="sxs-lookup"><span data-stu-id="663a6-126">OUTPUTS</span></span>

### <span data-ttu-id="663a6-127">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span><span class="sxs-lookup"><span data-stu-id="663a6-127">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>

## <span data-ttu-id="663a6-128">Notas</span><span class="sxs-lookup"><span data-stu-id="663a6-128">NOTES</span></span>

## <span data-ttu-id="663a6-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="663a6-129">RELATED LINKS</span></span>

<span data-ttu-id="663a6-130">[Novo-AzFrontDoor](./New-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md) 
 [Remove-AzFrontDoor](./Remove-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="663a6-130">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)
[Remove-AzFrontDoor](./Remove-AzFrontDoor.md)</span></span>
